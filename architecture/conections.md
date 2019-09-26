# Sign In Canada

## Network Connections

|Client|Server|Node Local?|Protocol|Encryption|Server Authentication|Client Authentication|
|------|------|----------|---------|----------|---------------------|---------------------|
|User Web Browser|Web Application Firewall|No|HTTP|TLS|Yes|No|
|Relying Party Application|Web Application Firewall|No|HTTP|TLS|Yes|No|
|Trusted Identity Provider|Web Application Firewall|No|HTTP|TLS|Yes|No|
|Credential Service Provider|Web Application Firewall|No|HTTP|TLS|Yes|No|
|Web Application Firewall|HTTP Reverse Proxy|No|HTTP|TLS|Yes|??|
|HTTP Reverse Proxy|Inbound Authentication Framework|Yes|HTTP|?|?|?|
|HTTP Reverse Proxy|OpenID Provider|Yes|HTTP|?|?|?|
|HTTP Reverse Proxy|SAML Identity Provider|Yes|HTTP|?|?|?|
|Inbound Authentication Framework|HTTP Forward Proxy|No|HTTP|TLS|?|?|
|OpenID Provider|HTTP Forward Proxy|No|HTTP|TLS|?|?|
|SAML Identity Provider|HTTP Forward Proxy|No|HTTP|TLS|?|?|
|Inbound Authentication Framework|Distributed Session Cache|No|RESP|TLS|Yes|Certificate|
|OpenID Provider|Distributed Session Cache|No|RESP|TLS|Yes|Certificate|
|SAML Identity Provider|Distributed Session Cache|No|RESP|TLS|Yes|Certificate|
|Inbound Authentication Framework|NoSQL Database|No|memcached|?|?|?|
|OpenID Provider|NoSQL Database|No|memcached|?|?|?|
|SAML Identity Provider|NoSQL Database|No|memcached|?|?|?|
|Distributed Session Cache|Distributed Session Cache|No|CBP|TLS|Yes|Certificate|
|NoSQL Database|NoSQL Database|No|DCP|?|?|?|

### Notes

TLS encryption and client certificate authentication for Distributed Session
Cache replication (CBP) is implemented using [stunnel](https://www.stunnel.org).

### Protocol References

* HTTP <https://tools.ietf.org/html/rfc2616>
* memcached <https://raw.githubusercontent.com/memcached/memcached/master/doc/protocol.txt>
* DCP <https://developer.couchbase.com/documentation/server/3.x/admin/Concepts/dcp.html>
* CBP <https://redis.io/topics/cluster-spec#clients-and-servers-roles-in-the-redis-cluster-protocol>
