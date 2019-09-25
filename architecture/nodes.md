# Sign In Canada

## Compute Nodes

### Cloud Security Appliance - Inbound

Network Zone: Public Access Zone (PAZ)

Hosted Componennts:

* Web Application Firewall

### Cloud Security Appliance - Outbound

Network Zone: Public Access Zone (PAZ)

Hosted Componennts:

* HTTP Forward Proxy

### Application Server

Network Zone: Application Tier Internet Services Restricted Zone (ARZ)

Hosted Componennts:

* HTTP Reverse Proxy
* Inbound Authentication Framework
* OpenID Provider
* SAML Identity Provider

### Session Cache Server

Network Zone: Application Tier Internet Services Restricted Zone (ARZ)

Hosted Componennts:

* Distributed Session Cache

### Database Server

Network Zone: Data Tier Internet Services Restricted Zone (DRZ)

### Management Server

Network Zone: Management Restricted Zone (MZ)

Hosted Components:

* HTTP Reverse Proxy
* Administration Web Interface
