# Sign In Canada

## Data Flows

|Source|Destination|Data Element|
|------|-----------|---------------|
|User Web Browser|Web Application Firewall|Web Content Request|
|User Web Browser|Web Application Firewall|Chosen Credential or Trusted Idetnity Provider|
|Web Application Firewall|User Web Browser|Web Content|
|User Web Browser|Web Application Firewall|Authentication Request|
|Web Application Firewall|User Web Browser|Authorization Code|
|Web Application Firewall|User Web Browser|SAML Assertion|
|User Web Browser|Web Application Firewall|Logout Request|
|Web Application Firewall|User Web Browser|Logout Request|
|User Web Browser|Web Application Firewall|Logout Response|
|Web Application Firewall|User Web Browser|Logout Response|
|Web Application Firewall|Credential Service Provider|Authentication Request|
|HTTP Forward Proxy|Credential Service Provider|ID Token Request|
|Credential Service Provider|HTTP Forward Proxy|ID Token|
|HTTP Forward Proxy|Trusted Digital Identitty Provider|ID Token Request|
|HTTP Forward Proxy|Trusted Digital Identitty Provider|ID Token|
|HTTP Forward Proxy|Trusted Digital Identitty Provider|Claims Request|
|Trusted Digital Identitty Provider|HTTP Forward Proxy|Claims Response|
