# Sign In Canada

## Inbound Data Flows

An inbound data flow is an HTTP request/response initiated by an External System and service by one of the Sign in Canada application components.


|Data Element|Source(s)|Destination(s)|HTTP Message|
|------------|---------|--------------|------------|
|Web Content Request|User Web Browser|OpenId Provider, SAML Identity Provider, Acceptance Framework|Request|
|Web Content|OpenId Provider, SAML IDP, Acceptance Framework|User Web Browser|Response|
|Chosen Credential or Trusted Identity Provider|User Web Browser|OpenId Provider|Request|
|Authentication Request|User Web Browser|OpenId Provider, SAML Identity Provider|Request|
|Authentication Request|Acceptance Framework|User Web Browser|Response|
|Authorization Code|User Web Browser|Acceptance Framework|Request|
|Authorization Code|OpenId Provider|User Web Browser|Response|
|SAML Assertion|SAML Identity Provider|User Web Browser|Response|
|SAML Assertion|User Web Browser|Acceptance Framework|Request|
|Logout Request|User Web Browser|Acceptance Framework, OpenId Provider, SAML Identity Provider|Request|
|Logout Response|Acceptance Framework, OpenId Provider, SAML Identity Provider|User Browser|Response|
|Logout Request|OpenId Provider, SAML Identity Provider, Acceptance Framework|User Web Browser|Response|
|Logout Response|User Web Browser|OpenId Provider, SAML Identity Provider, Acceptance Framework|Request|
|Token Request|Relying Party Application|OpenId Provider|Request|
|ID Token|OpenId Provider|Relying Party Application|Response|
|Access Token|OpenId Provider|Relying Party Application|Response|
|Claims Request|Relying Party Application|OpenId Provider|Request|
|Identity Claims|OpenId Provider|Relying Party Application|Response|
|Metadata Request|Relying Party Application|OpenId Provider|Request|
|Federation Metadata|OpenId Provider|Relying Party Application|Response|
|JSON Web Key Set|OpenId Provider|Relying Party Application|Response|

## Outbound Data Flows

An outbound data flow is an HTTP request/response initiated by one of the Sign in Canada application components and serviced by an External System.

|Data Element|Source(s)|Destination(s)|HTTP Message|
|------------|---------|--------------|------------|
|Logout Request|OpenId Provider, SAML Identity Provider|Relying Party Application|Request|
|Logout Response|Relying Party Application|OpenId Provider, SAML Identity Provider|Response|
|ID Token Request|Acceptance Framework|Credential Service Provider, Trusted Digital Identity Provider|Request|
|ID Token|Credential Service Provider, Trusted Digital Identity Provider|Acceptance Framework|Response|
|Claims Request|Acceptance Framework|Credential Service Provider, Trusted Digital Identity Provider|Request|
|Identity Claims|Credential Service Provider, Trusted Digital Identity Provider|Acceptance Framework|Response|
|Metadata Request|OpenId Provider, SAML Identity Provider|Federation Metadata Site|Request|
|Federation Metadata|Federation Metadata Site|OpenId Provider, SAML Identity Provider|Response|
|Metadata Request|Acceptance Framework|Credential Service Provider, Trusted Digital Identity Provider|Request|
|Federation Metadata|Credential Service Provider, Trusted Digital Identity Provider|Acceptance Framework|Response|
|JSON Web Key Set|Credential Service Provider, Trusted Digital Identity Provider|Acceptance Framework|Response|

## Internal Data Flows

An internal data flow is an HTTP request/response initiated by one of the Sign in Canada application components and serviced by another Sign in Canada application component.

|Data Element|Source(s)|Destination(s)|
|------------|---------|--------------|
|Session Cache Request|Acceptance Framework, OpenID Provider, SAML Identity Provider|NoSQL Database|
|Session Data|NoSQL Database|Acceptance Framework, OpenID Provider, SAML Identity Provider|
|Session Data|Acceptance Framework, OpenID Provider, SAML Identity Provider|NoSQL Database|
|Database Request|Acceptance Framework, OpenID Provider, SAML Identity Provider|NoSQL Database|
|User Account|NoSQL Database|OpenID Provider, SAML Identity Provider|
|User Account|Acceptance Framework|OpenID Provider|
|User Account|OpenID Provider|NoSQL Database|
