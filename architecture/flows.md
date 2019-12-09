# Sign In Canada

## Inbound Data Flows

An inbound data flow is an HTTP request/response initiated by an Extenal System and service by one of the Sign in Canada application components.


|Data Element|Source(s)|Destination(s)|HTTP Message|
|------------|---------|--------------|------------|
|Web Content Request|User Web Browser|OpenId Provider, SAML Identity Provider, Inbound Authentication Framework|Request|
|Web Content|OpenId Provider, SAML IDP, Inbound Authentication Framework|User Web Browser|Response|
|Chosen Credential or Trusted Identity Provider|User Web Browser|Inbound Authentication Framework|Request|
|Authentication Request|User Web Browser|OpenId Provider, SAML Identity Provider|Request|
|Authentication Request|Inbound Authentication Framework|User Web Browser|Response|
|Authorization Code|OpenId Provider|User Web Browser|Response|
|Authorization Code|Credential Service Provider, Trusted Digital Identitty Provider|Inbound Authentication Framework|Request|
|SAML Assertion|SAML Identity Provider|User Web Browser|Response|
|SAML Assertion|User Web Browser|Inbound Authentication Framework|Request|
|Logout Request|User Web Browser|Inbound Authentication Framework, OpenId Provider, SAML Identity Provider|Request|
|Logout Response|Inbound Authentication Framework, OpenId Provider, SAML Identity Provider|User Browser|Response|
|Logout Request|OpenId Provider, SAML Identity Provider, Inbound Authentication Framework|User Web Browser|Response|
|Logout Response|User Web Browser|OpenId Provider, SAML Identity Provider, Inbound Authentication Framework|Request|
|ID Token Request|Relying Party Application|OpenId Provider|Request|
|ID Token|OpenId Provider|Relying Party Application|Response|
|Metadata Request|Relying Party Application|OpenId Provider|Request|
|Federation Metadata|OpenId Provider|Relying Party Application|Response|
|JSON Web Key Set|OpenId Provider|Relying Party Application|Response|

## Outbound Data Flows

An outbound data flow is an HTTP request/response initiated by one of the Sign in Canada application components and serviced by an Extenal System.

|Data Element|Source(s)|Destination(s)|HTTP Message|
|------------|---------|--------------|------------|
|Logout Request|OpenId Provider, SAML Identity Provider|Relying Party Application|Request|
|Logout Response|Relying Party Application|OpenId Provider, SAML Identity Provider|Response|
|ID Token Request|Inbound Authentication Framework|Credential Service Provider, Trusted Digital Identitty Provider|Request|
|ID Token|Credential Service Provider, Trusted Digital Identitty Provider|Inbound Authentication Framework|Response|
|Claims Request|Inbound Authentication Framework|Credential Service Provider, Trusted Digital Identitty Provider|Request|
|Identity Claims|Credential Service Provider, Trusted Digital Identitty Provider|Inbound Authentication Framework|Response|
|Metadata Request|OpenId Provider, SAML Identity Provider|Federation Metadata Site|Request|
|Federation Metadata|Federation Metadata Site|OpenId Provider, SAML Identity Provider|Response|
|Metadata Request|Inbound Authentication Framework|Credential Service Provider, Trusted Digital Identitty Provider|Request|
|Federation Metadata|Credential Service Provider, Trusted Digital Identitty Provider|Inbound Authentication Framework|Response|
|JSON Web Key Set|Credential Service Provider, Trusted Digital Identitty Provider|Inbound Authentication Framework|Response|

## Internal Data Flows

An internal data flow is an HTTP request/response initiated by one of the Sign in Canada application components and serviced by another Sign in Canada application component.

|Data Element|Source(s)|Destination(s)|
|------------|---------|--------------|
|Session Cache Request|Inbound Authentication Framework, OpenID Provider, SAML Identity Provider|NoSQL Database|
|Session Data|Distributed Session Cache|Inbound Authentication Framework, OpenID Provider, SAML Identity Provider|
|Session Data|Inbound Authentication Framework, OpenID Provider, SAML Identity Provider|NoSQL Database|
|Database Request|Inbound Authentication Framework, OpenID Provider, SAML Identity Provider|NoSQL Database|
|User Account|NoSQL Database|Inbound Authentication Framework, OpenID Provider, SAML Identity Provider|
|User Account|Inbound Authentication Framework, OpenID Provider|NoSQL Database|
