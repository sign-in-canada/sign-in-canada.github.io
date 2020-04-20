## OpenID Provider Conformance tests
[OpenID Connect Provider Certification](https://op.certification.openid.net:60000/) provides a self service portal where you can configure your environment to run certain conformance profile tests. Some of the conformance profiles are:

- Basic OP
- Implicit OP
- Hybrid OP
- Config OP
- Dynamic OP

More details can be found about the above profile testing on official [OpenID Certification Testing site](https://openid.net/certification/testing/)

Below are number of conformance tests that were configured with the one of the non corporate (public cloud provider) test environment. [For now this can be seen here as well.](https://op.certification.openid.net:62183/)

|                                | Name                               | Description                                                                                                        |  |
|--------------------------------|------------------------------------|--------------------------------------------------------------------------------------------------------------------|--|
| Response Type                  |                                    |                                                                                                                    |  |
|                                | (OP-Response-Missing)              | Authorization request missing the response_type parameter                                                          |  |
|                                | (OP-Response-code+id_token+token)  | Request with response_type=code id_token token                                                                     |  |
| Discovery                      |                                    |                                                                                                                    |  |
|                                | (OP-Discovery-Config)              | Publishes openid-configuration discovery information                                                               |  |
|                                | (OP-Discovery-JWKs)                | Keys in OP JWKs well formed                                                                                        |  |
|                                | (OP-Discovery-claims_supported)    | Verify that claims_supported is published                                                                          |  |
| Dynamic Client Registration    |                                    |                                                                                                                    |  |
|                                | (OP-Registration-Dynamic)          | Client registration request                                                                                        |  |
|                                | (OP-Registration-Endpoint)         | Verify that registration_endpoint is published                                                                     |  |
|                                | (OP-Registration-Sector-Bad)       | Incorrect registration of sector_identifier_uri                                                                    |  |
|                                | (OP-Registration-jwks)             | Uses keys registered with jwks value                                                                               |  |
|                                | (OP-Registration-jwks_uri)         | Uses keys registered with jwks_uri value                                                                           |  |
|                                | (OP-Registration-logo_uri)         | Registration with logo_uri                                                                                         |  |
|                                | (OP-Registration-policy_uri)       | Registration with policy_uri                                                                                       |  |
|                                | (OP-Registration-tos_uri)          | Registration with tos_uri                                                                                          |  |
| ID Token                       |                                    |                                                                                                                    |  |
|                                | (OP-IDToken-C-Signature)           | Does the OP sign the ID Token and with what                                                                        |  |
|                                | (OP-IDToken-at_hash)               | ID Token has at_hash when ID Token and Access Token are returned from the Authorization Endpoint                   |  |
|                                | (OP-IDToken-c_hash)                | ID Token has c_hash when ID Token and Authorization Code returned from Authorization Endpoint [Hybrid]             |  |
| Client Authentication          |                                    |                                                                                                                    |  |
|                                | (OP-ClientAuth-Basic-Dynamic)      | Access token request with client_secret_basic authentication                                                       |  |
|                                | (OP-ClientAuth-SecretPost-Dynamic) | Access token request with client_secret_post authentication                                                        |  |
| Userinfo Endpoint              |                                    |                                                                                                                    |  |
|                                | (OP-UserInfo-Body)                 | UserInfo Endpoint access with POST and bearer body                                                                 |  |
|                                | (OP-UserInfo-Endpoint)             | UserInfo Endpoint access with GET and bearer header                                                                |  |
|                                | (OP-UserInfo-Header)               | UserInfo Endpoint access with POST and bearer header                                                               |  |
| claims Request Parameter       |                                    |                                                                                                                    |  |
|                                | (OP-claims-essential)              | Claims request with essential name claim                                                                           |  |
| display Request Parameter      |                                    |                                                                                                                    |  |
|                                | (OP-display-page)                  | Request with display=page                                                                                          |  |
|                                | (OP-display-popup)                 | Request with display=popup                                                                                         |  |
| nonce Request Parameter        |                                    |                                                                                                                    |  |
|                                | (OP-nonce-NoReq-noncode)           | Reject requests without nonce unless using the 'code' or 'code token' flow                                         |  |
|                                | (OP-nonce-noncode)                 | Request with nonce, verifies it was returned in ID Token [Implicit, Hybrid]                                        |  |
| prompt Request Parameter       |                                    |                                                                                                                    |  |
|                                | (OP-prompt-login)                  | Request with prompt=login                                                                                          |  |
|                                | (OP-prompt-none-LoggedIn)          | Request with prompt=none when logged in [Basic, Implicit, Hybrid]                                                  |  |
|                                | (OP-prompt-none-NotLoggedIn)       | Request with prompt=none when not logged in                                                                        |  |
| redirect_uri Request Parameter |                                    |                                                                                                                    |  |
|                                | (OP-redirect_uri-Missing)          | Reject request without redirect_uri when multiple registered                                                       |  |
|                                | (OP-redirect_uri-NotReg)           | Sent redirect_uri does not match a registered redirect_uri                                                         |  |
|                                | (OP-redirect_uri-Query-Added)      | Request with redirect_uri with query component when registered redirect_uri has no query component                 |  |
|                                | (OP-redirect_uri-Query-Mismatch)   | Rejects redirect_uri when query parameter does not match what is registered                                        |  |
|                                | (OP-redirect_uri-Query-OK)         | Request with a redirect_uri with a query component when a redirect_uri with the same query component is registered |  |
|                                | (OP-redirect_uri-RegFrag)          | Reject registration where a redirect_uri has a fragment                                                            |  |
| request Request Parameter      |                                    |                                                                                                                    |  |
|                                | (OP-request-Unsigned)              | Support request request parameter with unsigned request                                                            |  |
| request_uri Request Parameter  |                                    |                                                                                                                    |  |
|                                | (OP-request_uri-Unsigned)          | Support request_uri request parameter with unsigned request                                                        |  |
| scope Request Parameter        |                                    |                                                                                                                    |  |
|                                | (OP-scope-All)                     | Scope requesting all claims                                                                                        |  |
|                                | (OP-scope-address)                 | Scope requesting address claims                                                                                    |  |
|                                | (OP-scope-email)                   | Scope requesting email claims                                                                                      |  |
|                                | (OP-scope-phone)                   | Scope requesting phone claims                                                                                      |  |
|                                | (OP-scope-profile)                 | Scope requesting profile claims                                                                                    |  |
| Misc Request Parameters        |                                    |                                                                                                                    |  |
|                                | (OP-Req-NotUnderstood)             | Request with extra query component                                                                                 |  |
|                                | (OP-Req-acr_values)                | Providing acr_values                                                                                               |  |
|                                | (OP-Req-claims_locales)            | Providing claims_locales                                                                                           |  |
|                                | (OP-Req-id_token_hint)             | Using prompt=none with user hint through id_token_hint                                                             |  |
|                                | (OP-Req-login_hint)                | Providing login_hint                                                                                               |  |
|                                | (OP-Req-max_age=1)                 | Requesting ID Token with max_age=1 seconds restriction                                                             |  |
|                                | (OP-Req-max_age=10000)             | Requesting ID Token with max_age=10000 seconds restriction                                                         |  |
|                                | (OP-Req-ui_locales)                | Providing ui_locales                                                                                               |  |
| OAuth behaviors                |                                    |                                                                                                                    |  |
|                                | (OP-OAuth-2nd)                     | Trying to use authorization code twice should result in an error                                                   |  |
|                                | (OP-OAuth-2nd-30s)                 | Trying to use authorization code twice with 30 seconds in between uses must result in an error                     |  |
|                                | (OP-OAuth-2nd-Revokes)             | Trying to use authorization code twice should result in revoking previously issued access tokens                   |  |