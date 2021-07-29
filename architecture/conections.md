# Sign In Canada

## Acceptance Platform Connections

The table below lists all of the network connections that support communication
between the various components of the Acceptance Platform. Connections listed as
"External" support communication between the Acceptance Platform and external
systems. Connections listed as "Internal" support communication between
components of the Acceptance platform running on different compute nodes.
Connections listed as "local" support communication between components of the
Acceptance platform running on the same compute node (i.e. via the the localhost
loopback network interface).

|Client|Server|Type|Protocol|Encryption|Server Authentication|Client Authentication|
|------|------|----------|---------|----------|---------------------|---------------------|
|User Web Browser|HTTP Reverse Proxy|External|HTTP|TLS|Yes|No|
|Relying Party Application|HTTP Reverse Proxy|External|HTTP|TLS|Yes|Yes<sup>1</sup>|
|HTTP Reverse Proxy|Inbound Authentication Framework|Local|HTTP|No|No|No|
|HTTP Reverse Proxy|OpenID Provider|Local|HTTP|No|No|No|
|HTTP Reverse Proxy|SAML Identity Provider|Local|HTTP|No|No|No|
|Acceptance Framework|Trusted Identity Provider|External|HTTP|TLS|Yes|Yes<sup>2</sup>|
|Acceptance Framework|Credential Service Provider|External|HTTP|TLS|Yes|Yes<sup>2</sup>|
|OpenID Provider|NoSQL Database|Internal|HTTP, memcached|TLS|Yes<sup>3</sup>|Yes|
|SAML Identity Provider|NoSQL Database|Internal|HTTP|TLS|Yes<sup>3</sup>|Yes|
|Acceptance Framework|Azure Monitor (Application Insights)|External|HTTP|TLS|Yes|Yes<sup>4</sup>|
|OpenID Provider|Azure Monitor (Application Insights)|External|HTTP|TLS|Yes|Yes<sup>4</sup>|
|SAML Identity Provider|Azure Monitor (Application Insights)|External|HTTP|TLS|Yes|Yes<sup>4</sup>|
|Administration Web Interface|Azure Monitor (Application Insights)|External|HTTP|TLS|Yes|Yes<sup>4</sup>|
|SAML Identity Provider|Azure Storage|External|HTTP|TLS|Yes|No|
|NoSQL Database|Azure Storage|External|HTTP|TLS|Yes|Yes<sup>5</sup>|
|OpenID Provider|Azure Key Vault|External|HTTP|TLS|Yes|Yes<sup>5</sup>|
|Acceptance Framework|Azure Key Vault|External|HTTP|TLS|Yes|Yes<sup>5</sup>|
|SAML Identity Provider|Azure Key Vault|External|HTTP|TLS|Yes|Yes<sup>5</sup>|

### Notes

1. Relying Party access to the Acceptance Platform's public [OpenID
   Connect](https://openid.net/specs/openid-connect-discovery-1_0.html) and
   [SAML](https://www.oasis-open.org/committees/download.php/56785/sstc-saml-metadata-errata-2.0-wd-05.pdf)
   metadata is not authenticated, however access to the OpenID Connect
   [Token](https://openid.net/specs/openid-connect-core-1_0.html#TokenEndpoint)
   endpoint requires authentication using either a [JWT
   Assertion](https://tools.ietf.org/html/rfc7523#section-2.2) (recommended) or
   [client secret](https://tools.ietf.org/html/rfc6749#section-2.3.1). Connections to the
   [UserInfo](https://openid.net/specs/openid-connect-core-1_0.html#UserInfo) endpoint require an OAuth2 [access token](https://tools.ietf.org/html/rfc6750).
2. Connections to the public metadata of credential service and trusted identity
   provider APIs are not normally authenticated. Connections to APIs are
   authenticated as supported by the provider.
3. Clients authenticate the database server using a self-signed certificate
   issued by the database and trusted by the client.
4. Clients authenticate to Azure Monitor using an Application Insights instrumentation key which is managed in Azure Key Vault.
5. Clients authenticate to Azure Key Vault and Azure Storage using an Azure
   Active Directory [managed
   identity](https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/overview).


### Protocol References

* HTTP <https://tools.ietf.org/html/rfc2616>
* memcached <https://raw.githubusercontent.com/memcached/memcached/master/doc/protocol.txt>
