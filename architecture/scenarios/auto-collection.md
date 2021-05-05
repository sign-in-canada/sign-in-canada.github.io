# Pairwise Identifier Auto-Collection

One of the primary goals of the Sign In Canada Acceptance platform is to
facilitate the replacement of old credential service provider systems, in
particular, the outsourced legacy GCKey and Credential Broker Service systems
that have been in use since 2011.

One of the key prerequisites for decommissioning or replacing these old systems
is to move the pairwise identifier mappings currently held by these older
services to the Acceptance Platform, so that users' enrolments with relying
parties are not impacted when relying parties move to the Sign In Canada
platform. This also reduces the need to "bulk transfer" all of this data from
the older systems prior to their decommissioning/replacement.

The Sign In Canada Acceptance Platform implements a feature that is able to
automatically copy a user's pairwise identified mappings from a legacy
credential service to the Acceptance Platform the first time they are used.
These are then stored by the Acceptance Platform for future use, so that the
mapping stored by the credential service is no longer required. This reduces the
risk and effort required to move this data. Over time the mapping data of active
users is gradually "collected" by the Acceptance Platform, reducing the need to
copy the data manually.

## How it works

The Acceptance Platform accomplishes the automatic collection of pairwise
identifier mappings as part of the normal user login process, by sending a second
SAML authentication request to the legacy credential service providers when
required.

1. The process begins when a relying party sends an authentication request to
   the Acceptance Platform, using either OpenID Connect or SAML.
2. The Acceptance Platform then sends an authentication request to the CSP on
   its own behalf. Requesting the pairwise identifier that the CSP has created
   for Sign In Canada.
3. Upon receiving the SAML Assertion from the CSP, the Acceptance Platform looks
   the user up in its own user profile repository.
4. The Acceptance Platform then checks to see if it already has a pairwise
   identifier mapping for the authenticated user with the requesting relying
   party. If so, then collection is not required, the login flow completes
   normally, and the Acceptance platform returns the appropriate pairwise
   identifier to the relying party (RP).
5. If however, the Acceptance Platform does not have a pairwise identifier
   mapping for the authenticated user with the requesting relying party, then it
   sends a second authentication request to the CSP on the relying party's
   behalf.
6. If the CSP has an existing pairwise identifier for the user with the
   requesting RP, it returns that identifier in an Assertion and the Acceptance
   platform adds it to its own user repository. At this point, the identifier
   has been "collected" by the Acceptance platform, and will be used whenever
   the user logs into that RP in the future (as per step 4 above).
7. If the CSP does not have an existing pairwise identifier for the user with
   the requesting RP then there is nothing to "collect", so the Acceptance
   Platform creates a new identifier for the user with the requesting RP, and
   that identifier is used for all future logins.

## Technical Details

When sending a second authentication request to the CSP on behalf or the relying
party, the Acceptance Platform makes use of the `<NameIDPolicy>` element of the
SAML `<AuthnRequest>` message. Specifically, it uses the following two
attributes of the `<NameIDPolicy>` element:

* The value of the `SPNameQualifier` attribute is populated with the old SAML
  Entity Id of the requesting relying party, to indicate that the Acceptance
  Platform is requesting the RP's pairwise identifier instead of its own.
* The value of the `AllowCreate` attribute is set to `"false"`, to indicate to
  the CSP that it should not create a new pairwise identifier for the RP if is
  does not already have one.

Here is an example of an authentication request issued by the Acceptance
Platform on behalf of itself:

```xml
<samlp:AuthnRequest xmlns:samlp="urn:oasis:names:tc:SAML:2.0:protocol" ID="_f8e30829f6f60061c46e"
                    Version="2.0" IssueInstant="2021-05-05T17:17:02.583Z"
                    ProtocolBinding="urn:oasis:names:tc:SAML:2.0:bindings:HTTP-POST"
                    Destination="https://clegc-gckey.gc.ca/j/SSORedirect/metaAlias/GCKey/idp"
                    AssertionConsumerServiceURL="https://auth.id.canada.ca/passport/auth/saml/gckey/callback">
   <saml:Issuer xmlns:saml="urn:oasis:names:tc:SAML:2.0:assertion">
      https://auth.id.canada.ca
   </saml:Issuer>
   <samlp:NameIDPolicy xmlns:samlp="urn:oasis:names:tc:SAML:2.0:protocol"
                       Format="urn:oasis:names:tc:SAML:2.0:nameid-format:persistent"
                       AllowCreate="true"
                       SPNameQualifier="https://auth.id.canada.ca"/>
   <samlp:RequestedAuthnContext xmlns:samlp="urn:oasis:names:tc:SAML:2.0:protocol" Comparison="exact">
      <saml:AuthnContextClassRef xmlns:saml="urn:oasis:names:tc:SAML:2.0:assertion">
         urn:gc-ca:cyber-auth:assurance:loa2
      </saml:AuthnContextClassRef>
   </samlp:RequestedAuthnContext>
</samlp:AuthnRequest>
```

Here is an example of an authentication request issued by the Acceptance
Platform on behalf of a relying party:

```xml
<samlp:AuthnRequest xmlns:samlp="urn:oasis:names:tc:SAML:2.0:protocol" ID="_f8e30829f6f60061c46f"
                    Version="2.0" IssueInstant="2021-05-05T17:20:02.583Z"
                    ProtocolBinding="urn:oasis:names:tc:SAML:2.0:bindings:HTTP-POST"
                    Destination="https://clegc-gckey.gc.ca/j/SSORedirect/metaAlias/GCKey/idp"
                    AssertionConsumerServiceURL="https://auth.id.canada.ca/passport/auth/saml/gckey/callback">
   <saml:Issuer xmlns:saml="urn:oasis:names:tc:SAML:2.0:assertion">
      https://auth.id.canada.ca
   </saml:Issuer>
   <samlp:NameIDPolicy xmlns:samlp="urn:oasis:names:tc:SAML:2.0:protocol"
                       Format="urn:oasis:names:tc:SAML:2.0:nameid-format:persistent"
                       AllowCreate="false"
                       SPNameQualifier="https://relyingparty.department.gc.ca"/>
   <samlp:RequestedAuthnContext xmlns:samlp="urn:oasis:names:tc:SAML:2.0:protocol" Comparison="exact">
      <saml:AuthnContextClassRef xmlns:saml="urn:oasis:names:tc:SAML:2.0:assertion">
         urn:gc-ca:cyber-auth:assurance:loa2
      </saml:AuthnContextClassRef>
   </samlp:RequestedAuthnContext>
</samlp:AuthnRequest>
```

## Frequently Asked Questions

### What does the user experience? Do they need to enter their password twice?

This process takes advantage of the Single Sign On features inherent in SAML, so
that the user will not have to authenticate more than once, if at all:

* If the user is not already logged in to the CSP, or if they are logged in
  but the single sign-on (SSO) window (20 minutes with the GCCF CSPs) has
  expired, they will be prompted to authenticate after the first SAML
  authentication request. After they successfully log in to the CSP, the the
  Acceptance Platform then sends the second authentication request a fraction of
  a second later, well within the SSO window, so they will not be prompted to
  login a second time.
* In the unlikely case where the user is already logged in to the CSP, but the
  SSO window expires within the fraction of a second between the two
  authentication requests, then SSO will apply to the first request, but not to
  the second. Again, the user only needs to provide their credentials once.
* If the user is already logged in to the CSP, and both authentication requests
  are processed within the SSO window, then the CSP will not prompt the user to
  re-enter their credentials at all. The relying party can override this
  behaviour by specifying `prompt="login"` (for OpenID Connect) or
  `forceAuthn="true"` (in SAML) in their authentication request to Sign In
  Canada, in which case the Acceptance Platform will specify
  `forceAuthn="true"` on it's first request to the CSP, but not the second.

### What if the user at the keyboard changes? Is there a risk that the Acceptance Platform could collect the wrong identifier belonging to the wrong person?

This possible scenario can arise in cases where multiple people are sharing the
same device, and one of them has left the device unattended while they were
still logged in to the CSP. For example:

Consider two users, Alice and Bob, who both have access to the same shared computer:

* Alice logs into a GCCF relying party using her GCKey, but then walks away from
  the computer without logging off.
* Bob then sits down at the same computer and attempts to log in to a Sign In
  Canada relying party, just a few seconds before Alice's 20 minute single-sign
  on window expires.
* The Acceptance platform sends the first authentication request to GCKey, and
  receives Alice's pairwise identifier in return.
* Alice's SSO window then expires in the fraction of a second before the
  Acceptance Platform sends the second authentication request. GCKey prompts Bob
  to enter his GCKey credentials and then returns Bob's pairwise identifier to
  the Acceptance Platform.
* The Acceptance platform then associates Bob's GCKey identifier with Alice's
  user profile.

In order to safeguard against this, the Acceptance Platform checks the
`SessionIndex` of both SAML Assertions, and makes sure that they match before
accepting the collected identifier.

### SAML Pairwise identifiers issued by an identity provider (IDP) are supposed to be specific to a SAML service provider (SP). How is Sign In Canada allowed to obtain the identifiers generated for another SAML SP?

The SAML specifications allow for the existence of *Affiliations*: groups of one or more SPs that share the same pairwise identifier for a given user. When a relying party moves from the GCCF to Sign In Canada, a new SAML Affiliation is defined, via SAML metadata, that allows the Acceptance Platform to obtain the pairwise identifiers that were originally created for the RP.
