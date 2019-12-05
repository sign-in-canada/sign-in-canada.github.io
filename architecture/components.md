# Sign In Canada

## Internal Application Components

### Web Application Firewall

Product: F5 BigIP

Version:

Website: https://www.f5.com/products/security/advanced-waf/

### HTTP Forward Proxy

Product: Fortigate Unified Threat Management

Version:

Website: https://www.fortinet.com/products/smallbusiness/utm.html

### HTTP Reverse Proxy

Product: Apache HTTP Server

Version: 2.4.6

Website: https://httpd.apache.org/

Source code: https://github.com/apache/httpd

### Inbound Authentication Framework

Product: Gluu Passport

Gluu Passport is a [Node.JS](https://nodejs.org/en/about/) web application based
on the [Express](https://expressjs.com/) web application framework and the
[Passport.JS](http://www.passportjs.org/) authentication middleware.

This is the "Acceptance" component of the Acceptance Platform. It integrates
with credential providers and trusted identity providers in order to accept
assurances of credential and identity on behalf of GC relying parties.

Version: 4.0

Website: https://www.passportjs.org/

Source code: https://github.com/GluuFederation/gluu-passport

### OpenID Provider

Product: oxAuth

oxAuth is an open source [OpenID Connect](https://openid.net/connect/) Provider
(OP) and [UMA](https://kantarainitiative.org/confluence/display/uma/Home)
Authorization Server (AS).

oxAuth is the core component of the Acceptance Platform, responsible for the
user interface and business logic. As an [OpenID
Connect](https://openid.net/connect/) Provider, it also provides the application
programming inteface used by GC relying parties that integrate using [OpenID
Connect](https://openid.net/connect/).

Version: 4.0

Website: https://www.gluu.org/

Source code: https://github.com/GluuFederation/oxAuth

### SAML Identity Provider

Product: Shibboleth IDP

Shibboleth is a [SAML](https://wiki.oasis-open.org/security/FrontPage) Identity
Provider (IDP) that provides the application programming inteface used by GC
relying parties that integrate using [SAML](https://wiki.oasis-open.org/security/FrontPage).

Version: 3.4.4

Website: https://www.shibboleth.net/products/identity-provider/

Source code: https://wiki.shibboleth.net/confluence/display/DEV/Source+Code+Access

### NoSQL Database

Product: Couchbase Enterprise Server

Couchbase Server is an open-source, distributed, multi-model NoSQL
document-oriented database software package that is optimized for interactive
applications.


Version: 6.0.3

Website: https://www.couchbase.com/

### Memcached Proxy

Product: Moxi


Version: 5.0

Website/ Source code: https://github.com/couchbase/moxi

### Administration Web Interface

Product: oxTrust

oxTrust is a Weld based web application for Gluu Server administration.

oxTrust enables administrators to manage what information about people is being
exposed to partner websites. oxTrust is also the local management interface that
handles other server instance specific configurations, and provides a mechanism
for IT administrators to support people at the organization who are having
trouble accessing a website or network resource.

Version: 4.0

Website: https://www.gluu.org/

Source code: https://github.com/GluuFederation/oxTrust
