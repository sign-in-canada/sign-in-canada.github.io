# Sign In Canada

## Compute Nodes

### Cloud Security Appliance - Inbound

Network Zone: Public Access Zone (PAZ)

Product: F5 Virtual Big IP <https://www.f5.com/products/cloud-editions/big-ip-cloud-edition>

Hosted Componennts:

* Web Application Firewall

### Cloud Security Appliance - Outbound

Network Zone: Public Access Zone (PAZ)

Product: Fortinet UTM ????

Hosted Componennts:

* HTTP Forward Proxy

### Application Server

Network Zone: Application Tier Internet Services Restricted Zone (ARZ)

Opertating System: RedHat Enterprise Linux 7 <https://access.redhat.com/products/red-hat-enterprise-linux>

Software: Gluu Server 4.0 <https://gluu.org>

Hosted Componennts:

* HTTP Reverse Proxy
* Inbound Authentication Framework
* OpenID Provider
* SAML Identity Provider

### Database Server

Network Zone: Data Tier Internet Services Restricted Zone (DRZ)

Opertating System: RedHat Enterprise Linux 7 <https://access.redhat.com/products/red-hat-enterprise-linux>

Software: Couchbase Server Enterprise <https://couchbase.com>

### Management Server

Network Zone: Management Restricted Zone (MZ)

Hosted Components:

* HTTP Reverse Proxy
* Administration Web Interface
