## HTTP Flows (Request, Response Headers and Form Data)
Below are network captures from one of the test enviroment which displays detail HTTP flows. Signin Canada Acceptance Platform (SICAP) flow starts from a Relying party/simulator which simulator sends a SAML request to shiboleth which then converts the request into OIDC for oxauth to display chooser page UI and sends the request to passport which generates a SAML request for authentication to the CPSIM (Credential Provider Simulator) /CBS (Credential Broker Service). 

### Relying Party Simulator landing/home page
```
General
---
Request URL: https://rp1.tbstest.catslab.ca/RPSimulator/
Request Method: GET
Status Code: 200 OK
Remote Address: 52.232.135.10:443
Referrer Policy: no-referrer-when-downgrade
---
Response Headers
---
Cache-Control: private
Content-Type: text/html;charset=utf8
Date: Wed, 18 Mar 2020 13:39:42 GMT
Expires: Wed, 31 Dec 1969 19:00:00 EST
Server: Apache-Coyote/1.1
Set-Cookie: JSESSIONID=F0B6BE5C429142418447715E32D7094E; Path=/RPSimulator; Secure; HttpOnly
Transfer-Encoding: chunked
---
Request Headers
---
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Accept-Encoding: gzip, deflate, br
Accept-Language: en-US,en;q=0.9
Connection: keep-alive
DNT: 1
Host: rp1.tbstest.catslab.ca
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: none
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.132 Safari/537.36
```
### setCookie?lang=eng
```
General
---
Request URL: https://rp1.tbstest.catslab.ca/RPSimulator/setCookie?lang=eng&return=https://rp1.tbstest.catslab.ca/RPSimulator/home-eng.jsp
Request Method: GET
Status Code: 302 Found
Remote Address: 52.232.135.10:443
Referrer Policy: no-referrer-when-downgrade
---
Response Headers
---
Content-Length: 0
Date: Wed, 18 Mar 2020 13:39:45 GMT
Location: https://rp1.tbstest.catslab.ca/RPSimulator/home-eng.jsp?_gc_lang=eng
Server: Apache-Coyote/1.1
Set-Cookie: _gc_lang=eng; Domain=.fjgc-gccf.gc.ca; Path=/; Secure
---
Request Headers
---
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Accept-Encoding: gzip, deflate, br
Accept-Language: en-US,en;q=0.9
Connection: keep-alive
Cookie: JSESSIONID=F0B6BE5C429142418447715E32D7094E
DNT: 1
Host: rp1.tbstest.catslab.ca
Referer: https://rp1.tbstest.catslab.ca/RPSimulator/
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: same-origin
Sec-Fetch-User: ?1
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.132 Safari/537.36
---
Query String Parameters
---
lang: eng
return: https://rp1.tbstest.catslab.ca/RPSimulator/home-eng.jsp
```
### home-eng.jsp?_gc_lang=eng (Relying Party language selection)
```
General
---
Request URL: https://rp1.tbstest.catslab.ca/RPSimulator/home-eng.jsp?_gc_lang=eng
Request Method: GET
Status Code: 200 OK
Remote Address: 52.232.135.10:443
Referrer Policy: no-referrer-when-downgrade
---
Response Headers
---
Cache-Control: private
Content-Type: text/html;charset=utf8
Date: Wed, 18 Mar 2020 13:39:45 GMT
Expires: Wed, 31 Dec 1969 19:00:00 EST
Server: Apache-Coyote/1.1
Transfer-Encoding: chunked
---
Request Headers
---
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Accept-Encoding: gzip, deflate, br
Accept-Language: en-US,en;q=0.9
Connection: keep-alive
Cookie: JSESSIONID=F0B6BE5C429142418447715E32D7094E
DNT: 1
Host: rp1.tbstest.catslab.ca
Referer: https://rp1.tbstest.catslab.ca/RPSimulator/
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: same-origin
Sec-Fetch-User: ?1
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.132 Safari/537.36
---
Query String Parameters
---
_gc_lang: eng
```
### setReq (relying party)
```
---
General
---
Request URL: https://rp1.tbstest.catslab.ca/RPSimulator/setReq
Request Method: POST
Status Code: 200 OK
Remote Address: 52.232.135.10:443
Referrer Policy: no-referrer-when-downgrade
---
Response Headers
---
Content-Type: text/html;charset=utf8
Date: Wed, 18 Mar 2020 13:39:48 GMT
Server: Apache-Coyote/1.1
Transfer-Encoding: chunked
---
Request Headers
---
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Accept-Encoding: gzip, deflate, br
Accept-Language: en-US,en;q=0.9
Cache-Control: max-age=0
Connection: keep-alive
Content-Length: 7
Content-Type: application/x-www-form-urlencoded
Cookie: JSESSIONID=F0B6BE5C429142418447715E32D7094E
DNT: 1
Host: rp1.tbstest.catslab.ca
Origin: https://rp1.tbstest.catslab.ca
Referer: https://rp1.tbstest.catslab.ca/RPSimulator/home-eng.jsp?_gc_lang=eng
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: same-origin
Sec-Fetch-User: ?1
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.132 Safari/537.36
---
Form Data
---
loa2: on
```
### choose-eng.jsp
```
---
General
---
Request URL: https://rp1.tbstest.catslab.ca/RPSimulator/choose-eng.jsp
Request Method: GET
Status Code: 200 OK
Remote Address: 52.232.135.10:443
Referrer Policy: no-referrer-when-downgrade
---
Response Headers
---
Cache-Control: private
Content-Type: text/html;charset=utf8
Date: Wed, 18 Mar 2020 13:39:50 GMT
Expires: Wed, 31 Dec 1969 19:00:00 EST
Server: Apache-Coyote/1.1
Transfer-Encoding: chunked
---
Request Headers
---
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Accept-Encoding: gzip, deflate, br
Accept-Language: en-US,en;q=0.9
Connection: keep-alive
Cookie: JSESSIONID=F0B6BE5C429142418447715E32D7094E
DNT: 1
Host: rp1.tbstest.catslab.ca
Referer: https://rp1.tbstest.catslab.ca/RPSimulator/setReq
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: same-origin
Sec-Fetch-User: ?1
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.132 Safari/537.36
```
### fedletSSOInit.jsp?idpEntityID
```
---
General
---
Request URL: https://rp1.tbstest.catslab.ca/RPSimulator/saml2/jsp/fedletSSOInit.jsp?idpEntityID=https%3A%2F%2Fgluuserver-cc-01.canadacentral.cloudapp.azure.com&AuthnContextClassRef=urn%3Agc-ca%3Acyber-auth%3Aassurance%3Aloa2
Request Method: GET
Status Code: 302 Found
Remote Address: 52.232.135.10:443
Referrer Policy: no-referrer-when-downgrade
---
Response Headers
---
Cache-Control: private
Content-Length: 0
Content-Type: text/html;charset=ISO-8859-1
Date: Wed, 18 Mar 2020 13:39:52 GMT
Expires: Wed, 31 Dec 1969 19:00:00 EST
Location: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/idp/profile/SAML2/Redirect/SSO?SAMLRequest=nZTLbtswEEX3%2BQqBe70b1CZsA66NogbSRrXcLLobUUOHAEWqfKROv76U4rouEriAVwKo0cw99w41s9DJni69e1Rb%2FOHRuig6dFJZOr6ZE28U1WCFpQo6tNQxWi8%2F39EiyWhvtNNMS3KzWc%2BJLZDlUNyyCeAUS8xYy3k7xYZn%2FB0vWz7JmzLn5fsJiR7QWKHVnIQ2JNpY63GjrAPlwlFWZHFWxvlkl5e0nNLb4juJ1kGaUODGrx6d6y1N07303qJ5QhMzFmd5wkBBCwyVMyATJrVvoe8T%2BOUNJkx3qWj7NMjmQmI6cBTpFlthkLm0ru9J9FEbhqMdc8JBWhzUVWCteMLTSXXk%2FiBUK9T%2BsknNS5Gln3a7Kq7u6x2JljaoHlBWWlnfoakDhGD4bXv3F870eeIa6wJ44HJWQhOe6baqReclOG1Sjq1EFwilYKM1ZHEzG4Kjo6XmLMrLIuGPILK4PH6WnrU%2FDuvpl9Bws650kPF8zf4MtnfgLlcPJ6KN%2BVhK%2B2GDgjrlSFRXg4CvHqTgAs3%2FLAz%2BS6l%2FrgyCC6E645EsXsD%2BRTnxHa8GtuNmhNAcHtw1nCvd9WCEHZYYD8BcGDwaet54JUMcW%2BTXpDeU7VnMgLLnJlwLCH2H996AYkilhuIY4VsTTy68CRzsSF%2F%2FLxa%2FAQ%3D%3D&SigAlg=http%3A%2F%2Fwww.w3.org%2F2001%2F04%2Fxmldsig-more%23rsa-sha256&Signature=GF6GqgitpmuWW5%2BmRGAjNaico5T9MMd2oyW0tCtryWAZwK0%2F5nhmAqiIjRnHEzoHBK%2F6KBQsiZ00yJPC%2Fi%2B4xkWdxyb048Xs4nk%2BxSsGntCuRzJjFcQPtaO1ifz%2FrW7LoMH9TauqHluZoy03bI0ys3n76Speol%2BXG4wObv4PnnVNA4klSqpYGOBPk46LlqAdCk7kFJp8wiY7qe8alFpQs%2BPFziIsn04fe%2B5rBYzDDYbaRFmSo00h8Qo6wNiGm6n52okOuQKznk%2FzxDi6t5QobM1ibmoxY2kms%2FAIDY75R3UDGBg5NW%2BOGEJzOahUAvJaZp9Xhrmrl%2BpVIflGCY4HAw%3D%3D
Server: Apache-Coyote/1.1
---
Request Headers
---
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Accept-Encoding: gzip, deflate, br
Accept-Language: en-US,en;q=0.9
Connection: keep-alive
Cookie: JSESSIONID=F0B6BE5C429142418447715E32D7094E
DNT: 1
Host: rp1.tbstest.catslab.ca
Referer: https://rp1.tbstest.catslab.ca/RPSimulator/choose-eng.jsp
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: same-origin
Sec-Fetch-User: ?1
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.132 Safari/537.36
---
Query String Parameters
---
idpEntityID: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com
AuthnContextClassRef: urn:gc-ca:cyber-auth:assurance:loa2
```
### SSO?SAMLRequest
```
General
---
Request URL: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/idp/profile/SAML2/Redirect/SSO?SAMLRequest=nZTLbtswEEX3%2BQqBe70b1CZsA66NogbSRrXcLLobUUOHAEWqfKROv76U4rouEriAVwKo0cw99w41s9DJni69e1Rb%2FOHRuig6dFJZOr6ZE28U1WCFpQo6tNQxWi8%2F39EiyWhvtNNMS3KzWc%2BJLZDlUNyyCeAUS8xYy3k7xYZn%2FB0vWz7JmzLn5fsJiR7QWKHVnIQ2JNpY63GjrAPlwlFWZHFWxvlkl5e0nNLb4juJ1kGaUODGrx6d6y1N07303qJ5QhMzFmd5wkBBCwyVMyATJrVvoe8T%2BOUNJkx3qWj7NMjmQmI6cBTpFlthkLm0ru9J9FEbhqMdc8JBWhzUVWCteMLTSXXk%2FiBUK9T%2BsknNS5Gln3a7Kq7u6x2JljaoHlBWWlnfoakDhGD4bXv3F870eeIa6wJ44HJWQhOe6baqReclOG1Sjq1EFwilYKM1ZHEzG4Kjo6XmLMrLIuGPILK4PH6WnrU%2FDuvpl9Bws650kPF8zf4MtnfgLlcPJ6KN%2BVhK%2B2GDgjrlSFRXg4CvHqTgAs3%2FLAz%2BS6l%2FrgyCC6E645EsXsD%2BRTnxHa8GtuNmhNAcHtw1nCvd9WCEHZYYD8BcGDwaet54JUMcW%2BTXpDeU7VnMgLLnJlwLCH2H996AYkilhuIY4VsTTy68CRzsSF%2F%2FLxa%2FAQ%3D%3D&SigAlg=http%3A%2F%2Fwww.w3.org%2F2001%2F04%2Fxmldsig-more%23rsa-sha256&Signature=GF6GqgitpmuWW5%2BmRGAjNaico5T9MMd2oyW0tCtryWAZwK0%2F5nhmAqiIjRnHEzoHBK%2F6KBQsiZ00yJPC%2Fi%2B4xkWdxyb048Xs4nk%2BxSsGntCuRzJjFcQPtaO1ifz%2FrW7LoMH9TauqHluZoy03bI0ys3n76Speol%2BXG4wObv4PnnVNA4klSqpYGOBPk46LlqAdCk7kFJp8wiY7qe8alFpQs%2BPFziIsn04fe%2B5rBYzDDYbaRFmSo00h8Qo6wNiGm6n52okOuQKznk%2FzxDi6t5QobM1ibmoxY2kms%2FAIDY75R3UDGBg5NW%2BOGEJzOahUAvJaZp9Xhrmrl%2BpVIflGCY4HAw%3D%3D
Request Method: GET
Status Code: 302 Found
Remote Address: 52.228.62.155:443
Referrer Policy: no-referrer-when-downgrade
---
Response Headers
---
Cache-Control: no-store
Connection: Keep-Alive
Content-Length: 0
Content-Security-Policy: connect-src 'self' https://gluuserver-cc-01.canadacentral.cloudapp.azure.com https://www.canada.ca https://ajax.googleapis.com https://use.fontawesome.com https://lang-canada.fjgc-gccf.gc.ca https://cdn.canada.ca
Content-Security-Policy: frame-ancestors 'none';
Date: Wed, 18 Mar 2020 13:39:52 GMT
Expires: 
Keep-Alive: timeout=15, max=100
Location: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/idp/profile/SAML2/Redirect/SSO?execution=e1s1
Server: Jetty(9.4.19.v20190610)
Set-Cookie: JSESSIONID=node014324my2nzksb4ms3fjyylnvh0.node0; Path=/idp; Secure; HttpOnly;HttpOnly
Strict-Transport-Security: max-age=600; includeSubDomains
Strict-Transport-Security: max-age=0
X-Content-Type-Options: nosniff
X-Frame-Options: DENY
X-Xss-Protection: 1; mode=block
---
Request Headers
---
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Accept-Encoding: gzip, deflate, br
Accept-Language: en-US,en;q=0.9
Connection: keep-alive
DNT: 1
Host: gluuserver-cc-01.canadacentral.cloudapp.azure.com
Referer: https://rp1.tbstest.catslab.ca/RPSimulator/choose-eng.jsp
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: cross-site
Sec-Fetch-User: ?1
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.132 Safari/537.36
---
Query String Parameters
---
SAMLRequest: nZTLbtswEEX3+QqBe70b1CZsA66NogbSRrXcLLobUUOHAEWqfKROv76U4rouEriAVwKo0cw99w41s9DJni69e1Rb/OHRuig6dFJZOr6ZE28U1WCFpQo6tNQxWi8/39EiyWhvtNNMS3KzWc+JLZDlUNyyCeAUS8xYy3k7xYZn/B0vWz7JmzLn5fsJiR7QWKHVnIQ2JNpY63GjrAPlwlFWZHFWxvlkl5e0nNLb4juJ1kGaUODGrx6d6y1N07303qJ5QhMzFmd5wkBBCwyVMyATJrVvoe8T+OUNJkx3qWj7NMjmQmI6cBTpFlthkLm0ru9J9FEbhqMdc8JBWhzUVWCteMLTSXXk/iBUK9T+sknNS5Gln3a7Kq7u6x2JljaoHlBWWlnfoakDhGD4bXv3F870eeIa6wJ44HJWQhOe6baqReclOG1Sjq1EFwilYKM1ZHEzG4Kjo6XmLMrLIuGPILK4PH6WnrU/Duvpl9Bws650kPF8zf4MtnfgLlcPJ6KN+VhK+2GDgjrlSFRXg4CvHqTgAs3/LAz+S6l/rgyCC6E645EsXsD+RTnxHa8GtuNmhNAcHtw1nCvd9WCEHZYYD8BcGDwaet54JUMcW+TXpDeU7VnMgLLnJlwLCH2H996AYkilhuIY4VsTTy68CRzsSF//Lxa/AQ==
SigAlg: http://www.w3.org/2001/04/xmldsig-more#rsa-sha256
Signature: GF6GqgitpmuWW5+mRGAjNaico5T9MMd2oyW0tCtryWAZwK0/5nhmAqiIjRnHEzoHBK/6KBQsiZ00yJPC/i+4xkWdxyb048Xs4nk+xSsGntCuRzJjFcQPtaO1ifz/rW7LoMH9TauqHluZoy03bI0ys3n76Speol+XG4wObv4PnnVNA4klSqpYGOBPk46LlqAdCk7kFJp8wiY7qe8alFpQs+PFziIsn04fe+5rBYzDDYbaRFmSo00h8Qo6wNiGm6n52okOuQKznk/zxDi6t5QobM1ibmoxY2kms/AIDY75R3UDGBg5NW+OGEJzOahUAvJaZp9Xhrmrl+pVIflGCY4HAw==
```
### SSO?execution
```
General
---
Request URL: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/idp/profile/SAML2/Redirect/SSO?execution=e1s1
Request Method: GET
Status Code: 302 Found
Remote Address: 52.228.62.155:443
Referrer Policy: no-referrer-when-downgrade
---
Response Headers
---
Cache-Control: no-store
Connection: Keep-Alive
Content-Length: 0
Content-Security-Policy: connect-src 'self' https://gluuserver-cc-01.canadacentral.cloudapp.azure.com https://www.canada.ca https://ajax.googleapis.com https://use.fontawesome.com https://lang-canada.fjgc-gccf.gc.ca https://cdn.canada.ca
Content-Security-Policy: frame-ancestors 'none';
Date: Wed, 18 Mar 2020 13:39:56 GMT
Keep-Alive: timeout=15, max=99
Location: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/idp/Authn/oxAuth?conversation=e1s1
Request-Context: appId=cid-v1:28ed79ce-6df8-41d0-b78c-f1466b0e7d96
Server: Jetty(9.4.19.v20190610)
Strict-Transport-Security: max-age=600; includeSubDomains
Strict-Transport-Security: max-age=0
X-Content-Type-Options: nosniff
X-Frame-Options: DENY
X-Xss-Protection: 1; mode=block
---
Request Headers
---
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Accept-Encoding: gzip, deflate, br
Accept-Language: en-US,en;q=0.9
Connection: keep-alive
Cookie: JSESSIONID=node014324my2nzksb4ms3fjyylnvh0.node0
DNT: 1
Host: gluuserver-cc-01.canadacentral.cloudapp.azure.com
Referer: https://rp1.tbstest.catslab.ca/RPSimulator/choose-eng.jsp
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: cross-site
Sec-Fetch-User: ?1
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.132 Safari/537.36
---
Query String Parameter
---
execution: e1s1
```
### oxAuth?conversation=e1s1
```
General
---
Request URL: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/idp/Authn/oxAuth?conversation=e1s1
Request Method: GET
Status Code: 302 Found
Remote Address: 52.228.62.155:443
Referrer Policy: no-referrer-when-downgrade
---
Response Headers
---
Connection: Keep-Alive
Content-Length: 0
Content-Security-Policy: connect-src 'self' https://gluuserver-cc-01.canadacentral.cloudapp.azure.com https://www.canada.ca https://ajax.googleapis.com https://use.fontawesome.com https://lang-canada.fjgc-gccf.gc.ca https://cdn.canada.ca
Content-Security-Policy: frame-ancestors 'none';
Date: Wed, 18 Mar 2020 13:39:56 GMT
Keep-Alive: timeout=15, max=98
Location: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/oxauth/restv1/authorize?response_type=code&client_id=1101.2eb78fce-15c2-4faf-86ea-e86a6504e547&scope=openid+email+user_name&redirect_uri=https%3A%2F%2Fgluuserver-cc-01.canadacentral.cloudapp.azure.com%2Fidp%2FAuthn%2FoxAuth&state=eyJ0eXAiOiJKV1QiLCJhbGciOiJub25lIn0.eyJzdGF0ZSI6IkM2c0gycFE2VHEiLCJjb252ZXJzYXRpb24iOiJlMXMxIn0.&nonce=PQOtpccU1v&acr_values=urn:gc-ca:cyber-auth:assurance:loa2&entityId=https://rp1.tbstest.catslab.ca&spNameQualifier=https://rp1.tbstest.catslab.ca
Request-Context: appId=cid-v1:28ed79ce-6df8-41d0-b78c-f1466b0e7d96
Server: Jetty(9.4.19.v20190610)
Strict-Transport-Security: max-age=600; includeSubDomains
Strict-Transport-Security: max-age=0
X-Content-Type-Options: nosniff
X-Frame-Options: DENY
X-Xss-Protection: 1; mode=block
---
Request Headers
---
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Accept-Encoding: gzip, deflate, br
Accept-Language: en-US,en;q=0.9
Connection: keep-alive
Cookie: JSESSIONID=node014324my2nzksb4ms3fjyylnvh0.node0
DNT: 1
Host: gluuserver-cc-01.canadacentral.cloudapp.azure.com
Referer: https://rp1.tbstest.catslab.ca/RPSimulator/choose-eng.jsp
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: cross-site
Sec-Fetch-User: ?1
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.132 Safari/537.36
---
Query String Parameters
---
conversation: e1s1
```
### authorize?response_type=code
```
General
---
Request URL: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/oxauth/restv1/authorize?response_type=code&client_id=1101.2eb78fce-15c2-4faf-86ea-e86a6504e547&scope=openid+email+user_name&redirect_uri=https%3A%2F%2Fgluuserver-cc-01.canadacentral.cloudapp.azure.com%2Fidp%2FAuthn%2FoxAuth&state=eyJ0eXAiOiJKV1QiLCJhbGciOiJub25lIn0.eyJzdGF0ZSI6IkM2c0gycFE2VHEiLCJjb252ZXJzYXRpb24iOiJlMXMxIn0.&nonce=PQOtpccU1v&acr_values=urn:gc-ca:cyber-auth:assurance:loa2&entityId=https://rp1.tbstest.catslab.ca&spNameQualifier=https://rp1.tbstest.catslab.ca
Request Method: GET
Status Code: 302 Found
Remote Address: 52.228.62.155:443
Referrer Policy: no-referrer-when-downgrade
---
Response Headers
---
Connection: Keep-Alive
Content-Length: 0
Content-Security-Policy: connect-src 'self' https://gluuserver-cc-01.canadacentral.cloudapp.azure.com https://www.canada.ca https://ajax.googleapis.com https://use.fontawesome.com https://lang-canada.fjgc-gccf.gc.ca https://cdn.canada.ca
Date: Wed, 18 Mar 2020 13:40:00 GMT
Keep-Alive: timeout=15, max=97
Location: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/oxauth/authorize.htm?scope=openid+email+user_name&acr_values=urn%3Agc-ca%3Acyber-auth%3Aassurance%3Aloa2&response_type=code&entityId=https%3A%2F%2Frp1.tbstest.catslab.ca&redirect_uri=https%3A%2F%2Fgluuserver-cc-01.canadacentral.cloudapp.azure.com%2Fidp%2FAuthn%2FoxAuth&state=eyJ0eXAiOiJKV1QiLCJhbGciOiJub25lIn0.eyJzdGF0ZSI6IkM2c0gycFE2VHEiLCJjb252ZXJzYXRpb24iOiJlMXMxIn0.&spNameQualifier=https%3A%2F%2Frp1.tbstest.catslab.ca&nonce=PQOtpccU1v&client_id=1101.2eb78fce-15c2-4faf-86ea-e86a6504e547
Request-Context: appId=cid-v1:28ed79ce-6df8-41d0-b78c-f1466b0e7d96
Server: Apache
Strict-Transport-Security: max-age=600; includeSubDomains
X-Content-Type-Options: nosniff
X-Xss-Protection: 1; mode=block
---
Request Headers
---
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Accept-Encoding: gzip, deflate, br
Accept-Language: en-US,en;q=0.9
Connection: keep-alive
DNT: 1
Host: gluuserver-cc-01.canadacentral.cloudapp.azure.com
Referer: https://rp1.tbstest.catslab.ca/RPSimulator/choose-eng.jsp
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: cross-site
Sec-Fetch-User: ?1
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.132 Safari/537.36
---
Query String Parameters
---
response_type: code
client_id: 1101.2eb78fce-15c2-4faf-86ea-e86a6504e547
scope: openid email user_name
redirect_uri: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/idp/Authn/oxAuth
state: eyJ0eXAiOiJKV1QiLCJhbGciOiJub25lIn0.eyJzdGF0ZSI6IkM2c0gycFE2VHEiLCJjb252ZXJzYXRpb24iOiJlMXMxIn0.
nonce: PQOtpccU1v
acr_values: urn:gc-ca:cyber-auth:assurance:loa2
entityId: https://rp1.tbstest.catslab.ca
spNameQualifier: https://rp1.tbstest.catslab.ca
```
### authoize.htm?scope=openid (redirect)
```
General
---
Request URL: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/oxauth/authorize.htm?scope=openid+email+user_name&acr_values=urn%3Agc-ca%3Acyber-auth%3Aassurance%3Aloa2&response_type=code&entityId=https%3A%2F%2Frp1.tbstest.catslab.ca&redirect_uri=https%3A%2F%2Fgluuserver-cc-01.canadacentral.cloudapp.azure.com%2Fidp%2FAuthn%2FoxAuth&state=eyJ0eXAiOiJKV1QiLCJhbGciOiJub25lIn0.eyJzdGF0ZSI6IkM2c0gycFE2VHEiLCJjb252ZXJzYXRpb24iOiJlMXMxIn0.&spNameQualifier=https%3A%2F%2Frp1.tbstest.catslab.ca&nonce=PQOtpccU1v&client_id=1101.2eb78fce-15c2-4faf-86ea-e86a6504e547
Request Method: GET
Status Code: 302 Found
Remote Address: 52.228.62.155:443
Referrer Policy: no-referrer-when-downgrade
---
Response Headers
---
Connection: Keep-Alive
Content-Length: 0
Content-Security-Policy: connect-src 'self' https://gluuserver-cc-01.canadacentral.cloudapp.azure.com https://www.canada.ca https://ajax.googleapis.com https://use.fontawesome.com https://lang-canada.fjgc-gccf.gc.ca https://cdn.canada.ca
Content-Type: text/html
Date: Wed, 18 Mar 2020 13:40:00 GMT
Expires: Thu, 01 Jan 1970 00:00:00 GMT
Keep-Alive: timeout=15, max=96
Location: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/oxauth/select.htm
Request-Context: appId=cid-v1:28ed79ce-6df8-41d0-b78c-f1466b0e7d96
Server: Apache
Set-Cookie: org.gluu.i18n.Locale=en; Path=/; Expires=Thu, 18-Mar-2021 13:40:00 GMT; Max-Age=31536000; Secure;HttpOnly
Set-Cookie: session_id=811511ea-6d9f-4685-8155-4635cd9d53c3; Path=/; Secure; HttpOnly;HttpOnly
Set-Cookie: session_state=ad5af2be832439c29d62ebd287dee49cf8a773d43c77e01be60f70989e531125.36d0b57c-92d0-4649-b1cb-c69261ed71bc; Path=/; Secure
Set-Cookie: opbs=c96733cb-c78e-4fec-afac-86cf1efc4516; Path=/; Secure;HttpOnly
Set-Cookie: rp_origin_id=https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/idp/Authn/oxAuth; Path=/oxauth; Secure; HttpOnly;HttpOnly
Strict-Transport-Security: max-age=600; includeSubDomains
X-Content-Type-Options: nosniff
X-Xss-Protection: 1; mode=block
---
Request Headers
---
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Accept-Encoding: gzip, deflate, br
Accept-Language: en-US,en;q=0.9
Connection: keep-alive
DNT: 1
Host: gluuserver-cc-01.canadacentral.cloudapp.azure.com
Referer: https://rp1.tbstest.catslab.ca/RPSimulator/choose-eng.jsp
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: cross-site
Sec-Fetch-User: ?1
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.132 Safari/537.36
---
Query String Parameters
---
scope: openid email user_name
acr_values: urn:gc-ca:cyber-auth:assurance:loa2
response_type: code
entityId: https://rp1.tbstest.catslab.ca
redirect_uri: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/idp/Authn/oxAuth
state: eyJ0eXAiOiJKV1QiLCJhbGciOiJub25lIn0.eyJzdGF0ZSI6IkM2c0gycFE2VHEiLCJjb252ZXJzYXRpb24iOiJlMXMxIn0.
spNameQualifier: https://rp1.tbstest.catslab.ca
nonce: PQOtpccU1v
client_id: 1101.2eb78fce-15c2-4faf-86ea-e86a6504e547
```
### Select.htm (chooser page)
```
General
---
Request URL: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/oxauth/select.htm
Request Method: GET
Status Code: 200 OK
Remote Address: 52.228.62.155:443
Referrer Policy: no-referrer-when-downgrade
---
Response Headers
---
Connection: Keep-Alive
Content-Length: 25891
Content-Security-Policy: connect-src 'self' https://gluuserver-cc-01.canadacentral.cloudapp.azure.com https://www.canada.ca https://ajax.googleapis.com https://use.fontawesome.com https://lang-canada.fjgc-gccf.gc.ca https://cdn.canada.ca
Content-Type: text/html;charset=utf-8
Date: Wed, 18 Mar 2020 13:40:00 GMT
Expires: Thu, 01 Jan 1970 00:00:00 GMT
Keep-Alive: timeout=15, max=95
Request-Context: appId=cid-v1:28ed79ce-6df8-41d0-b78c-f1466b0e7d96
Server: Apache
Set-Cookie: org.gluu.i18n.Locale=en; Path=/; Expires=Thu, 18-Mar-2021 13:40:00 GMT; Max-Age=31536000; Secure;HttpOnly
Set-Cookie: JSESSIONID=node01doxw8mqznx8a1lndiaq3q6iaz1.node0; Path=/oxauth; Secure;HttpOnly
Strict-Transport-Security: max-age=600; includeSubDomains
X-Content-Type-Options: nosniff
X-Xss-Protection: 1; mode=block
---
Request Headers
---
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Accept-Encoding: gzip, deflate, br
Accept-Language: en-US,en;q=0.9
Connection: keep-alive
Cookie: rp_origin_id=https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/idp/Authn/oxAuth; org.gluu.i18n.Locale=en; session_id=811511ea-6d9f-4685-8155-4635cd9d53c3; session_state=ad5af2be832439c29d62ebd287dee49cf8a773d43c77e01be60f70989e531125.36d0b57c-92d0-4649-b1cb-c69261ed71bc; opbs=c96733cb-c78e-4fec-afac-86cf1efc4516
DNT: 1
Host: gluuserver-cc-01.canadacentral.cloudapp.azure.com
Referer: https://rp1.tbstest.catslab.ca/RPSimulator/choose-eng.jsp
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: cross-site
Sec-Fetch-User: ?1
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.132 Safari/537.36
```
### language header
```
General
---
Request URL: https://lang-canada.fjgc-gccf.gc.ca/v1/lang
Referrer Policy: no-referrer-when-downgrade
---
Request Headers
---
Provisional headers are shown
Accept: */*
Content-Type: application/json
DNT: 1
Referer: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/oxauth/select.htm
Sec-Fetch-Dest: empty
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.132 Safari/537.36
---
Request Payload
---
{lang: "eng"}
lang: "eng"
```
### sitemenu-v5-en.html 
```
General
---
Request URL: https://cdn.canada.ca/gcweb-cdn-live/sitemenu/sitemenu-v5-en.html
Request Method: GET
Status Code: 200 
Remote Address: 198.103.198.76:443
Referrer Policy: no-referrer-when-downgrade
---
Response Headers
---
accept-ranges: bytes
access-control-allow-origin: *
content-encoding: gzip
content-length: 7028
content-type: text/html
date: Wed, 18 Mar 2020 13:40:00 GMT
etag: "081136994d51:0"
last-modified: Tue, 05 Nov 2019 18:45:36 GMT
server: Microsoft-IIS/10.0
status: 200
strict-transport-security: max-age=31536000; includeSubDomains; preload
vary: Accept-Encoding
---
Request Headers
---
:authority: cdn.canada.ca
:method: GET
:path: /gcweb-cdn-live/sitemenu/sitemenu-v5-en.html
:scheme: https
accept: */*
accept-encoding: gzip, deflate, br
accept-language: en-US,en;q=0.9
dnt: 1
origin: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com
referer: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/oxauth/select.htm
sec-fetch-dest: empty
sec-fetch-mode: cors
sec-fetch-site: cross-site
user-agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.132 Safari/537.36
```
### select.htm (POST Requst) redirect
```
General
---
Request URL: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/oxauth/select.htm
Request Method: POST
Status Code: 302 Found
Remote Address: 52.228.62.155:443
Referrer Policy: no-referrer-when-downgrade
---
Response Headers
---
Connection: Keep-Alive
Content-Length: 0
Content-Security-Policy: connect-src 'self' https://gluuserver-cc-01.canadacentral.cloudapp.azure.com https://www.canada.ca https://ajax.googleapis.com https://use.fontawesome.com https://lang-canada.fjgc-gccf.gc.ca https://cdn.canada.ca
Content-Type: text/html
Date: Wed, 18 Mar 2020 13:40:07 GMT
Expires: Thu, 01 Jan 1970 00:00:00 GMT
Keep-Alive: timeout=15, max=94
Location: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/oxauth/select.htm
Request-Context: appId=cid-v1:28ed79ce-6df8-41d0-b78c-f1466b0e7d96
Server: Apache
Set-Cookie: org.gluu.i18n.Locale=en; Path=/; Expires=Thu, 18-Mar-2021 13:40:07 GMT; Max-Age=31536000; Secure;HttpOnly
Strict-Transport-Security: max-age=600; includeSubDomains
X-Content-Type-Options: nosniff
X-Xss-Protection: 1; mode=block
---
Request Headers
---
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Accept-Encoding: gzip, deflate, br
Accept-Language: en-US,en;q=0.9
Cache-Control: max-age=0
Connection: keep-alive
Content-Length: 588
Content-Type: application/x-www-form-urlencoded
Cookie: rp_origin_id=https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/idp/Authn/oxAuth; JSESSIONID=node01doxw8mqznx8a1lndiaq3q6iaz1.node0; org.gluu.i18n.Locale=en; session_id=811511ea-6d9f-4685-8155-4635cd9d53c3; session_state=ad5af2be832439c29d62ebd287dee49cf8a773d43c77e01be60f70989e531125.36d0b57c-92d0-4649-b1cb-c69261ed71bc; opbs=c96733cb-c78e-4fec-afac-86cf1efc4516
DNT: 1
Host: gluuserver-cc-01.canadacentral.cloudapp.azure.com
Origin: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com
Referer: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/oxauth/select.htm
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: same-origin
Sec-Fetch-User: ?1
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.132 Safari/537.36
---
Form Data
---
loginForm: loginForm
loginForm:acrname: passport_saml:gckey
loginForm:switchCredentialBox: off
loginForm:loginButton1: Sign in with GCKey
javax.faces.ViewState: GxxCHIiG9DKlTDP9wRBov3hErJQNU6B+Xk5J3m8z6iO5b7M43ugFkp68pPEFEZkBMwoFLP7RjRQJU5R8rvUcrYCZvNjmt1TjNG/xQ74EQsPIxYsiKWSjBK5xBScBtP2SSyrx4HZkqOQFa6qIKJkKohsQxFD5060rDhhwgWnW38rHZgHc7zdkTfH4UYx3TyipGTGuTBmwvMFU3s13X/928q64G6hLJXCVoSSTDGFGqaaVmEizRxK0twoVViTyDK6hpwSXNew7vNPdJi23JmtZXxMPtZfhnUWVY4HjZKdQlZOtQTnXJsWCyV1PMTlhkBg2s1+xftHsduPoTH0MKf/QTvlpiXaVMHuME79Z+yAeWAjLB8oqCJG1vy85TIc5Q91jdKHdcSc8NOx8GffQ3HLOdw==
```
### select.htm (GET Requst) redirect
```
General
---
Request URL: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/oxauth/select.htm
Request Method: GET
Status Code: 302 Found
Remote Address: 52.228.62.155:443
Referrer Policy: no-referrer-when-downgrade
---
Response Headers
---
Connection: Keep-Alive
Content-Length: 0
Content-Security-Policy: connect-src 'self' https://gluuserver-cc-01.canadacentral.cloudapp.azure.com https://www.canada.ca https://ajax.googleapis.com https://use.fontawesome.com https://lang-canada.fjgc-gccf.gc.ca https://cdn.canada.ca
Content-Type: text/html
Date: Wed, 18 Mar 2020 13:40:07 GMT
Keep-Alive: timeout=15, max=93
Location: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/oxauth/auth/passport/passportpostlogin.htm
Request-Context: appId=cid-v1:28ed79ce-6df8-41d0-b78c-f1466b0e7d96
Server: Apache
Strict-Transport-Security: max-age=600; includeSubDomains
X-Content-Type-Options: nosniff
X-Xss-Protection: 1; mode=block
---
Request Headers
---
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Accept-Encoding: gzip, deflate, br
Accept-Language: en-US,en;q=0.9
Cache-Control: max-age=0
Connection: keep-alive
Cookie: rp_origin_id=https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/idp/Authn/oxAuth; JSESSIONID=node01doxw8mqznx8a1lndiaq3q6iaz1.node0; org.gluu.i18n.Locale=en; session_id=811511ea-6d9f-4685-8155-4635cd9d53c3; session_state=ad5af2be832439c29d62ebd287dee49cf8a773d43c77e01be60f70989e531125.36d0b57c-92d0-4649-b1cb-c69261ed71bc; opbs=c96733cb-c78e-4fec-afac-86cf1efc4516
DNT: 1
Host: gluuserver-cc-01.canadacentral.cloudapp.azure.com
Referer: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/oxauth/select.htm
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: same-origin
Sec-Fetch-User: ?1
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.132 Safari/537.36
```
### passportpostlogin.htm (redirect)
```
General
---
Request URL: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/oxauth/auth/passport/passportpostlogin.htm
Request Method: GET
Status Code: 302 Found
Remote Address: 52.228.62.155:443
Referrer Policy: no-referrer-when-downgrade
---
Response Headers
---
Connection: Keep-Alive
Content-Length: 0
Content-Security-Policy: connect-src 'self' https://gluuserver-cc-01.canadacentral.cloudapp.azure.com https://www.canada.ca https://ajax.googleapis.com https://use.fontawesome.com https://lang-canada.fjgc-gccf.gc.ca https://cdn.canada.ca
Content-Type: text/html
Date: Wed, 18 Mar 2020 13:40:07 GMT
Keep-Alive: timeout=15, max=92
Location: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/passport/auth/gckey/eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJqd3QiOiJmNDBkNzcxYi1lNTk2LTQzZWUtYWE4Mi0zMGY5ODdiZTczNmQiLCJpYXQiOjE1ODQ1Mzg4MDgsImV4cCI6MTU4NDUzODkyOH0.6Lgj_sY_V-g_m5geL6cY3iVYh-YvE0HVCXTHRgO067s
Request-Context: appId=cid-v1:28ed79ce-6df8-41d0-b78c-f1466b0e7d96
Server: Apache
Strict-Transport-Security: max-age=600; includeSubDomains
X-Content-Type-Options: nosniff
X-Xss-Protection: 1; mode=block
---
Request Headers
---
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Accept-Encoding: gzip, deflate, br
Accept-Language: en-US,en;q=0.9
Cache-Control: max-age=0
Connection: keep-alive
Cookie: rp_origin_id=https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/idp/Authn/oxAuth; JSESSIONID=node01doxw8mqznx8a1lndiaq3q6iaz1.node0; org.gluu.i18n.Locale=en; session_id=811511ea-6d9f-4685-8155-4635cd9d53c3; session_state=ad5af2be832439c29d62ebd287dee49cf8a773d43c77e01be60f70989e531125.36d0b57c-92d0-4649-b1cb-c69261ed71bc; opbs=c96733cb-c78e-4fec-afac-86cf1efc4516
DNT: 1
Host: gluuserver-cc-01.canadacentral.cloudapp.azure.com
Referer: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/oxauth/select.htm
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: same-origin
Sec-Fetch-User: ?1
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.132 Safari/537.36
```
### passport gckey redirect
```
General
---
Request URL: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/passport/auth/gckey/eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJqd3QiOiJmNDBkNzcxYi1lNTk2LTQzZWUtYWE4Mi0zMGY5ODdiZTczNmQiLCJpYXQiOjE1ODQ1Mzg4MDgsImV4cCI6MTU4NDUzODkyOH0.6Lgj_sY_V-g_m5geL6cY3iVYh-YvE0HVCXTHRgO067s
Request Method: GET
Status Code: 302 Found
Remote Address: 52.228.62.155:443
Referrer Policy: no-referrer-when-downgrade
---
Response Headers
---
Connection: Keep-Alive
Content-Length: 0
Content-Security-Policy: connect-src 'self' https://gluuserver-cc-01.canadacentral.cloudapp.azure.com https://www.canada.ca https://ajax.googleapis.com https://use.fontawesome.com https://lang-canada.fjgc-gccf.gc.ca https://cdn.canada.ca
Date: Wed, 18 Mar 2020 13:40:08 GMT
Keep-Alive: timeout=15, max=91
Location: https://cpsim1.catslab.ca/openam/SSORedirect/metaAlias/idp?SAMLRequest=nVNNj9owFPwrke%2BJw0eXXQtYUVBVpG0XAe2hl%2BrFebDWOrbr52yhv75OIC2HlgOnSH7jN%2BOZyfjxUOnkDT0payasl%2BXscTomqLQTszq8mDX%2BqJFCEmGGRDuYsNobYYEUCQMVkghSbGafnkQ%2Fy4XzNlhpNUuWiwn7Lne7u%2FLh3ag%2FKkZQ5PlwV9yx5GtHGG9EIFGNS0MBTIhHeT9P80Hau9%2F2BmKYi%2Fw%2BexgMv7FkdV79XplSmf11HcUJROLjdrtKV8%2BbLUsW8SXKQGipX0JwJDiXjlTVyyQE0lDEL7cO4z6%2B2TyvsVQeZeAVBphpBcRV6VjywXqJrT8TFnyNLJkRoW8Wz62hukK%2FQf%2BmJH5ZP%2F2l2uu6jrBodyplmjekBkqQaIIHnUlt6xKcy%2BBX7TGTtuIOiJz1gUMk4439fC9f8cglaF2AfGWntETrob%2BI6bo70Mll05vFjfkFc1eaz5FquVhZreTxltJEZysI19HNiSrTXQsVrukShSgzpqC1%2FTn3CAHPwfBO2LnIWLaxxZQCHm6q9dxWDryipkN4ABm6CC4Xz3V0eI27WwJpYHuZShDyWMQ0muibee3BSBTaQv9s%2Fb8Yp6fZfx78Z3r5c09%2FAw%3D%3D&SigAlg=http%3A%2F%2Fwww.w3.org%2F2001%2F04%2Fxmldsig-more%23rsa-sha256&Signature=J6ZGowOmcG9LMRsgIuUY1PNKwrwQL%2FbeUtl3z3uVIaK4zyAHgOsldkk7%2F5Gfms5qOdLYJSGem07Hgl0b6fIX8IgUh7%2FMaQ%2FNv4i1kHZCMzXU%2FQhw1YwSxTEtslIplTK9H%2FNkyYcoezm7ZBgUFptkYWJoqTs35K16CxoORZ9tS0vo6zyst1%2BTArKf52hF9LI%2Bb4bQF%2Bu58UYdmS88Hf44gNji0TuMIjOS%2B3WkgJ%2Fz%2Fv4EAyuM8LbZRldrGZ00SVpeUNL9DzYBNsAkyZx3wqHMBBXNV3l2Ie9O%2BUeYD438VlD2uT%2BhWEgJr2bZpp4rCu8woWHjQyg9DUMT6NG0C%2FGbxg%3D%3D
Server: Apache
Strict-Transport-Security: max-age=600; includeSubDomains
X-Content-Type-Options: nosniff
X-Powered-By: Express
X-Xss-Protection: 1; mode=block
---
Request Headers
---
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Accept-Encoding: gzip, deflate, br
Accept-Language: en-US,en;q=0.9
Cache-Control: max-age=0
Connection: keep-alive
Cookie: org.gluu.i18n.Locale=en; session_id=811511ea-6d9f-4685-8155-4635cd9d53c3; session_state=ad5af2be832439c29d62ebd287dee49cf8a773d43c77e01be60f70989e531125.36d0b57c-92d0-4649-b1cb-c69261ed71bc; opbs=c96733cb-c78e-4fec-afac-86cf1efc4516
DNT: 1
Host: gluuserver-cc-01.canadacentral.cloudapp.azure.com
Referer: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/oxauth/select.htm
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: same-origin
Sec-Fetch-User: ?1
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.132 Safari/537.36
```
### idp?SAMLRequst
```
General 
---
Request URL: https://cpsim1.catslab.ca/openam/SSORedirect/metaAlias/idp?SAMLRequest=nVNNj9owFPwrke%2BJw0eXXQtYUVBVpG0XAe2hl%2BrFebDWOrbr52yhv75OIC2HlgOnSH7jN%2BOZyfjxUOnkDT0payasl%2BXscTomqLQTszq8mDX%2BqJFCEmGGRDuYsNobYYEUCQMVkghSbGafnkQ%2Fy4XzNlhpNUuWiwn7Lne7u%2FLh3ag%2FKkZQ5PlwV9yx5GtHGG9EIFGNS0MBTIhHeT9P80Hau9%2F2BmKYi%2Fw%2BexgMv7FkdV79XplSmf11HcUJROLjdrtKV8%2BbLUsW8SXKQGipX0JwJDiXjlTVyyQE0lDEL7cO4z6%2B2TyvsVQeZeAVBphpBcRV6VjywXqJrT8TFnyNLJkRoW8Wz62hukK%2FQf%2BmJH5ZP%2F2l2uu6jrBodyplmjekBkqQaIIHnUlt6xKcy%2BBX7TGTtuIOiJz1gUMk4439fC9f8cglaF2AfGWntETrob%2BI6bo70Mll05vFjfkFc1eaz5FquVhZreTxltJEZysI19HNiSrTXQsVrukShSgzpqC1%2FTn3CAHPwfBO2LnIWLaxxZQCHm6q9dxWDryipkN4ABm6CC4Xz3V0eI27WwJpYHuZShDyWMQ0muibee3BSBTaQv9s%2Fb8Yp6fZfx78Z3r5c09%2FAw%3D%3D&SigAlg=http%3A%2F%2Fwww.w3.org%2F2001%2F04%2Fxmldsig-more%23rsa-sha256&Signature=J6ZGowOmcG9LMRsgIuUY1PNKwrwQL%2FbeUtl3z3uVIaK4zyAHgOsldkk7%2F5Gfms5qOdLYJSGem07Hgl0b6fIX8IgUh7%2FMaQ%2FNv4i1kHZCMzXU%2FQhw1YwSxTEtslIplTK9H%2FNkyYcoezm7ZBgUFptkYWJoqTs35K16CxoORZ9tS0vo6zyst1%2BTArKf52hF9LI%2Bb4bQF%2Bu58UYdmS88Hf44gNji0TuMIjOS%2B3WkgJ%2Fz%2Fv4EAyuM8LbZRldrGZ00SVpeUNL9DzYBNsAkyZx3wqHMBBXNV3l2Ie9O%2BUeYD438VlD2uT%2BhWEgJr2bZpp4rCu8woWHjQyg9DUMT6NG0C%2FGbxg%3D%3D
Request Method: GET
Status Code: 200 OK
Remote Address: 52.235.25.50:443
Referrer Policy: no-referrer-when-downgrade
---
Response Headers
---
AM_CLIENT_TYPE: genericHTML
Cache-Control: private
Content-Type: text/html;charset=UTF-8
Date: Wed, 18 Mar 2020 13:40:09 GMT
Expires: 0
Pragma: no-cache
Server: Apache-Coyote/1.1
Set-Cookie: JSESSIONID=4302CA40B401F6FCD2EFE674AA211312; Path=/openam; Secure; HttpOnly
Set-Cookie: AMAuthCookie=AQIC5wM2LY4SfcztbE04ygajFxpJaWHScFrRQyE1EpHBmM4.*AAJTSQACMDEAAlNLABQtNDY1MzM5Nzk5MjY0NzcyMjIwNg..*; Domain=cpsim1.catslab.ca; Path=/; Secure
Set-Cookie: amlbcookie=01; Domain=cpsim1.catslab.ca; Path=/; Secure
Transfer-Encoding: chunked
---
Request Headers
---
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Accept-Encoding: gzip, deflate, br
Accept-Language: en-US,en;q=0.9
Cache-Control: max-age=0
Connection: keep-alive
DNT: 1
Host: cpsim1.catslab.ca
Referer: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/oxauth/select.htm
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: cross-site
Sec-Fetch-User: ?1
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.132 Safari/537.36
---
Query String Parameters
---
SAMLRequest: nVNNj9owFPwrke+Jw0eXXQtYUVBVpG0XAe2hl+rFebDWOrbr52yhv75OIC2HlgOnSH7jN+OZyfjxUOnkDT0payasl+XscTomqLQTszq8mDX+qJFCEmGGRDuYsNobYYEUCQMVkghSbGafnkQ/y4XzNlhpNUuWiwn7Lne7u/Lh3ag/KkZQ5PlwV9yx5GtHGG9EIFGNS0MBTIhHeT9P80Hau9/2BmKYi/w+exgMv7FkdV79XplSmf11HcUJROLjdrtKV8+bLUsW8SXKQGipX0JwJDiXjlTVyyQE0lDEL7cO4z6+2TyvsVQeZeAVBphpBcRV6VjywXqJrT8TFnyNLJkRoW8Wz62hukK/Qf+mJH5ZP/2l2uu6jrBodyplmjekBkqQaIIHnUlt6xKcy+BX7TGTtuIOiJz1gUMk4439fC9f8cglaF2AfGWntETrob+I6bo70Mll05vFjfkFc1eaz5FquVhZreTxltJEZysI19HNiSrTXQsVrukShSgzpqC1/Tn3CAHPwfBO2LnIWLaxxZQCHm6q9dxWDryipkN4ABm6CC4Xz3V0eI27WwJpYHuZShDyWMQ0muibee3BSBTaQv9s/b8Yp6fZfx78Z3r5c09/Aw==
SigAlg: http://www.w3.org/2001/04/xmldsig-more#rsa-sha256
Signature: J6ZGowOmcG9LMRsgIuUY1PNKwrwQL/beUtl3z3uVIaK4zyAHgOsldkk7/5Gfms5qOdLYJSGem07Hgl0b6fIX8IgUh7/MaQ/Nv4i1kHZCMzXU/Qhw1YwSxTEtslIplTK9H/NkyYcoezm7ZBgUFptkYWJoqTs35K16CxoORZ9tS0vo6zyst1+TArKf52hF9LI+b4bQF+u58UYdmS88Hf44gNji0TuMIjOS+3WkgJ/z/v4EAyuM8LbZRldrGZ00SVpeUNL9DzYBNsAkyZx3wqHMBBXNV3l2Ie9O+UeYD438VlD2uT+hWEgJr2bZpp4rCu8woWHjQyg9DUMT6NG0C/Gbxg==
```
### wmms.svg (Credential provider)
```
General
---
Request URL: https://cpsim1.catslab.ca/openam/theme-gcwu-fegc/assets/wmms.svg
Request Method: GET
Status Code: 200 OK
Remote Address: 52.235.25.50:443
Referrer Policy: no-referrer-when-downgrade
---
Response Headers
---
Accept-Ranges: bytes
Content-Length: 4819
Content-Type: image/svg+xml
Date: Wed, 18 Mar 2020 13:40:09 GMT
ETag: W/"4819-1502813050000"
Last-Modified: Tue, 15 Aug 2017 16:04:10 GMT
Server: Apache-Coyote/1.1
---
Request Headers
---
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Accept-Encoding: gzip, deflate, br
Accept-Language: en-US,en;q=0.9
Connection: keep-alive
Cookie: JSESSIONID=4302CA40B401F6FCD2EFE674AA211312; AMAuthCookie=AQIC5wM2LY4SfcztbE04ygajFxpJaWHScFrRQyE1EpHBmM4.*AAJTSQACMDEAAlNLABQtNDY1MzM5Nzk5MjY0NzcyMjIwNg..*; amlbcookie=01
DNT: 1
Host: cpsim1.catslab.ca
Referer: https://cpsim1.catslab.ca/openam/SSORedirect/metaAlias/idp?SAMLRequest=nVNNj9owFPwrke%2BJw0eXXQtYUVBVpG0XAe2hl%2BrFebDWOrbr52yhv75OIC2HlgOnSH7jN%2BOZyfjxUOnkDT0payasl%2BXscTomqLQTszq8mDX%2BqJFCEmGGRDuYsNobYYEUCQMVkghSbGafnkQ%2Fy4XzNlhpNUuWiwn7Lne7u%2FLh3ag%2FKkZQ5PlwV9yx5GtHGG9EIFGNS0MBTIhHeT9P80Hau9%2F2BmKYi%2Fw%2BexgMv7FkdV79XplSmf11HcUJROLjdrtKV8%2BbLUsW8SXKQGipX0JwJDiXjlTVyyQE0lDEL7cO4z6%2B2TyvsVQeZeAVBphpBcRV6VjywXqJrT8TFnyNLJkRoW8Wz62hukK%2FQf%2BmJH5ZP%2F2l2uu6jrBodyplmjekBkqQaIIHnUlt6xKcy%2BBX7TGTtuIOiJz1gUMk4439fC9f8cglaF2AfGWntETrob%2BI6bo70Mll05vFjfkFc1eaz5FquVhZreTxltJEZysI19HNiSrTXQsVrukShSgzpqC1%2FTn3CAHPwfBO2LnIWLaxxZQCHm6q9dxWDryipkN4ABm6CC4Xz3V0eI27WwJpYHuZShDyWMQ0muibee3BSBTaQv9s%2Fb8Yp6fZfx78Z3r5c09%2FAw%3D%3D&SigAlg=http%3A%2F%2Fwww.w3.org%2F2001%2F04%2Fxmldsig-more%23rsa-sha256&Signature=J6ZGowOmcG9LMRsgIuUY1PNKwrwQL%2FbeUtl3z3uVIaK4zyAHgOsldkk7%2F5Gfms5qOdLYJSGem07Hgl0b6fIX8IgUh7%2FMaQ%2FNv4i1kHZCMzXU%2FQhw1YwSxTEtslIplTK9H%2FNkyYcoezm7ZBgUFptkYWJoqTs35K16CxoORZ9tS0vo6zyst1%2BTArKf52hF9LI%2Bb4bQF%2Bu58UYdmS88Hf44gNji0TuMIjOS%2B3WkgJ%2Fz%2Fv4EAyuM8LbZRldrGZ00SVpeUNL9DzYBNsAkyZx3wqHMBBXNV3l2Ie9O%2BUeYD438VlD2uT%2BhWEgJr2bZpp4rCu8woWHjQyg9DUMT6NG0C%2FGbxg%3D%3D
Sec-Fetch-Dest: object
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: same-origin
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.132 Safari/537.36
```
### login (Credential provider simulator)
```
General
---
Request URL: https://cpsim1.catslab.ca/openam/UI/Login
Request Method: POST
Status Code: 302 Found
Remote Address: 52.235.25.50:443
Referrer Policy: no-referrer-when-downgrade
---
Response Headers
---
AM_CLIENT_TYPE: genericHTML
Cache-Control: private
Content-Length: 0
Content-Type: text/html;charset=ISO-8859-1
Date: Wed, 18 Mar 2020 13:40:18 GMT
Expires: 0
Location: https://cpsim1.catslab.ca:443/idpdiscovery/saml2writer?_saml_idp=https://cpsim1.catslab.ca&RelayState=https%3A%2F%2Fcpsim1.catslab.ca%3A443%2Fopenam%2FSSORedirect%2FmetaAlias%2Fidp%3FresInfoID%3Ds21023ca378ff0f99db67d8a9bd1d280dfbe2cf201
Pragma: no-cache
Server: Apache-Coyote/1.1
Set-Cookie: IDPSimulator=AQIC5wM2LY4SfcxVT3UASH74SY7jqd02SxCU3jv7yDsTSoY.*AAJTSQACMDEAAlNLABM1MzU3NDgwMTQzMjUxODI5ODAz*; Domain=cpsim1.catslab.ca; Path=/; Secure
Set-Cookie: AMAuthCookie=LOGOUT; Domain=cpsim1.catslab.ca; Expires=Thu, 01-Jan-1970 00:00:10 GMT; Path=/; Secure
X-AuthErrorCode: 0
---
Request Headers
---
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Accept-Encoding: gzip, deflate, br
Accept-Language: en-US,en;q=0.9
Cache-Control: max-age=0
Connection: keep-alive
Content-Length: 2052
Content-Type: application/x-www-form-urlencoded
Cookie: JSESSIONID=4302CA40B401F6FCD2EFE674AA211312; AMAuthCookie=AQIC5wM2LY4SfcztbE04ygajFxpJaWHScFrRQyE1EpHBmM4.*AAJTSQACMDEAAlNLABQtNDY1MzM5Nzk5MjY0NzcyMjIwNg..*; amlbcookie=01
DNT: 1
Host: cpsim1.catslab.ca
Origin: https://cpsim1.catslab.ca
Referer: https://cpsim1.catslab.ca/openam/SSORedirect/metaAlias/idp?SAMLRequest=nVNNj9owFPwrke%2BJw0eXXQtYUVBVpG0XAe2hl%2BrFebDWOrbr52yhv75OIC2HlgOnSH7jN%2BOZyfjxUOnkDT0payasl%2BXscTomqLQTszq8mDX%2BqJFCEmGGRDuYsNobYYEUCQMVkghSbGafnkQ%2Fy4XzNlhpNUuWiwn7Lne7u%2FLh3ag%2FKkZQ5PlwV9yx5GtHGG9EIFGNS0MBTIhHeT9P80Hau9%2F2BmKYi%2Fw%2BexgMv7FkdV79XplSmf11HcUJROLjdrtKV8%2BbLUsW8SXKQGipX0JwJDiXjlTVyyQE0lDEL7cO4z6%2B2TyvsVQeZeAVBphpBcRV6VjywXqJrT8TFnyNLJkRoW8Wz62hukK%2FQf%2BmJH5ZP%2F2l2uu6jrBodyplmjekBkqQaIIHnUlt6xKcy%2BBX7TGTtuIOiJz1gUMk4439fC9f8cglaF2AfGWntETrob%2BI6bo70Mll05vFjfkFc1eaz5FquVhZreTxltJEZysI19HNiSrTXQsVrukShSgzpqC1%2FTn3CAHPwfBO2LnIWLaxxZQCHm6q9dxWDryipkN4ABm6CC4Xz3V0eI27WwJpYHuZShDyWMQ0muibee3BSBTaQv9s%2Fb8Yp6fZfx78Z3r5c09%2FAw%3D%3D&SigAlg=http%3A%2F%2Fwww.w3.org%2F2001%2F04%2Fxmldsig-more%23rsa-sha256&Signature=J6ZGowOmcG9LMRsgIuUY1PNKwrwQL%2FbeUtl3z3uVIaK4zyAHgOsldkk7%2F5Gfms5qOdLYJSGem07Hgl0b6fIX8IgUh7%2FMaQ%2FNv4i1kHZCMzXU%2FQhw1YwSxTEtslIplTK9H%2FNkyYcoezm7ZBgUFptkYWJoqTs35K16CxoORZ9tS0vo6zyst1%2BTArKf52hF9LI%2Bb4bQF%2Bu58UYdmS88Hf44gNji0TuMIjOS%2B3WkgJ%2Fz%2Fv4EAyuM8LbZRldrGZ00SVpeUNL9DzYBNsAkyZx3wqHMBBXNV3l2Ie9O%2BUeYD438VlD2uT%2BhWEgJr2bZpp4rCu8woWHjQyg9DUMT6NG0C%2FGbxg%3D%3D
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: same-origin
Sec-Fetch-User: ?1
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.132 Safari/537.36
---
Form Data
---
IDToken1: user.1
IDToken2: password
IDButton: Login
goto: L1NTT1JlZGlyZWN0L21ldGFBbGlhcy9pZHA/UmVxSUQ9X2NmZjZkOTU3MjdiN2FiMDA0ZmI2JmluZGV4PW51bGwmYWNzVVJMPWh0dHBzJTNBJTJGJTJGZ2x1dXNlcnZlci1jYy0wMS5jYW5hZGFjZW50cmFsLmNsb3VkYXBwLmF6dXJlLmNvbSUyRnBhc3Nwb3J0JTJGYXV0aCUyRnNhbWwlMkZnY2tleSUyRmNhbGxiYWNrJnNwRW50aXR5SUQ9aHR0cHMlM0ElMkYlMkZnbHV1c2VydmVyLWNjLTAxLmNhbmFkYWNlbnRyYWwuY2xvdWRhcHAuYXp1cmUuY29tJmJpbmRpbmc9dXJuJTNBb2FzaXMlM0FuYW1lcyUzQXRjJTNBU0FNTCUzQTIuMCUzQWJpbmRpbmdzJTNBSFRUUC1QT1NU
SunQueryParamsString: Zm9yd2FyZD10cnVlJnJlYWxtPS8mU2lnQWxnPWh0dHA6Ly93d3cudzMub3JnLzIwMDEvMDQveG1sZHNpZy1tb3JlI3JzYS1zaGEyNTYmU0FNTFJlcXVlc3Q9blZOTmo5b3dGUHdya2UrSncwZVhYUXRZVVZCVnBHMFhBZTJobCtyRmViRFdPcmJyNTJ5aHY3NU9JQzJIbGdPblNIN2pOK09aeWZqeFVPbmtEVDBwYXlhc2wrWHNjVG9tcUxRVHN6cThtRFgrcUpGQ0VtR0dSRHVZc05vYllZRVVDUU1Wa2doU2JHYWZua1EveTRYek5saHBOVXVXaXduN0xuZTd1L0xoM2FnL0trWlE1UGx3Vjl5eDVHdEhHRzlFSUZHTlMwTUJUSWhIZVQ5UDgwSGF1OS8yQm1LWWkvdytleGdNdjdGa2RWNzlYcGxTbWYxMUhjVUpST0xqZHJ0S1Y4K2JMVXNXOFNYS1FHaXBYMEp3SkRpWGpsVFZ5eVFFMGxERUw3Y080ejYrMlR5dnNWUWVaZUFWQnBocEJjUlY2Vmp5d1hxSnJUOFRGbnlOTEprUm9XOFd6NjJodWtLL1FmK21KSDVaUC8ybDJ1dTZqckJvZHlwbG1qZWtCa3FRYUlJSG5VbHQ2eEtjeStCWDdUR1R0dUlPaUp6MWdVTWs0NDM5ZkM5ZjhjZ2xhRjJBZkdXbnRFVHJvYitJNmJvNzBNbGwwNXZGamZrRmMxZWF6NUZxdVZoWnJlVHhsdEpFWnlzSTE5SE5pU3JUWFFzVnJ1a1NoU2d6cHFDMS9UbjNDQUhQd2ZCTzJMbklXTGF4eFpRQ0htNnE5ZHhXRHJ5aXBrTjRBQm02Q0M0WHozVjBlSTI3V3dKcFlIdVpTaER5V01RMG11aWJlZTNCU0JUYVF2OXMvYjhZcDZmWmZ4NzhaM3I1YzA5L0F3PT0mU2lnbmF0dXJlPUo2Wkdvd09tY0c5TE1Sc2dJdVVZMVBOS3dyd1FML2JlVXRsM3ozdVZJYUs0enlBSGdPc2xka2s3LzVHZm1zNXFPZExZSlNHZW0wN0hnbDBiNmZJWDhJZ1VoNy9NYVEvTnY0aTFrSFpDTXpYVS9RaHcxWXdTeFRFdHNsSXBsVEs5SC9Oa3lZY29lem03WkJnVUZwdGtZV0pvcVRzMzVLMTZDeG9PUlo5dFMwdm82enlzdDErVEFyS2Y1MmhGOUxJK2I0YlFGK3U1OFVZZG1TODhIZjQ0Z05qaTBUdU1Jak9TKzNXa2dKL3ovdjRFQXl1TThMYlpSbGRyR1owMFNWcGVVTkw5RHpZQk5zQWt5Wngzd3FITUJCWE5WM2wySWU5TytVZVlENDM4VmxEMnVUK2hXRWdKcjJiWnBwNHJDdTh3b1dIalF5ZzlEVU1UNk5HMEMvR2J4Zz09JnNwRW50aXR5SUQ9aHR0cHM6Ly9nbHV1c2VydmVyLWNjLTAxLmNhbmFkYWNlbnRyYWwuY2xvdWRhcHAuYXp1cmUuY29t
encoded: true
gx_charset: UTF-8
```
### saml2writer?_saml_idp
```
General
---
Request URL: https://cpsim1.catslab.ca/idpdiscovery/saml2writer?_saml_idp=https://cpsim1.catslab.ca&RelayState=https%3A%2F%2Fcpsim1.catslab.ca%3A443%2Fopenam%2FSSORedirect%2FmetaAlias%2Fidp%3FresInfoID%3Ds21023ca378ff0f99db67d8a9bd1d280dfbe2cf201
Request Method: GET
Status Code: 302 Found
Remote Address: 52.235.25.50:443
Referrer Policy: no-referrer-when-downgrade
---
Response Headers
---
Content-Length: 0
Date: Wed, 18 Mar 2020 13:40:18 GMT
Location: https://cpsim1.catslab.ca:443/openam/SSORedirect/metaAlias/idp?resInfoID=s21023ca378ff0f99db67d8a9bd1d280dfbe2cf201
Server: Apache-Coyote/1.1
SET-COOKIE: _saml_idp=aHR0cHM6Ly9jcHNpbTEuY2F0c2xhYi5jYQ%3D%3D;path=/;domain=.catslab.ca;secure;httponly
---
Request Headers
---
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Accept-Encoding: gzip, deflate, br
Accept-Language: en-US,en;q=0.9
Cache-Control: max-age=0
Connection: keep-alive
Cookie: amlbcookie=01; IDPSimulator=AQIC5wM2LY4SfcxVT3UASH74SY7jqd02SxCU3jv7yDsTSoY.*AAJTSQACMDEAAlNLABM1MzU3NDgwMTQzMjUxODI5ODAz*
DNT: 1
Host: cpsim1.catslab.ca
Referer: https://cpsim1.catslab.ca/openam/SSORedirect/metaAlias/idp?SAMLRequest=nVNNj9owFPwrke%2BJw0eXXQtYUVBVpG0XAe2hl%2BrFebDWOrbr52yhv75OIC2HlgOnSH7jN%2BOZyfjxUOnkDT0payasl%2BXscTomqLQTszq8mDX%2BqJFCEmGGRDuYsNobYYEUCQMVkghSbGafnkQ%2Fy4XzNlhpNUuWiwn7Lne7u%2FLh3ag%2FKkZQ5PlwV9yx5GtHGG9EIFGNS0MBTIhHeT9P80Hau9%2F2BmKYi%2Fw%2BexgMv7FkdV79XplSmf11HcUJROLjdrtKV8%2BbLUsW8SXKQGipX0JwJDiXjlTVyyQE0lDEL7cO4z6%2B2TyvsVQeZeAVBphpBcRV6VjywXqJrT8TFnyNLJkRoW8Wz62hukK%2FQf%2BmJH5ZP%2F2l2uu6jrBodyplmjekBkqQaIIHnUlt6xKcy%2BBX7TGTtuIOiJz1gUMk4439fC9f8cglaF2AfGWntETrob%2BI6bo70Mll05vFjfkFc1eaz5FquVhZreTxltJEZysI19HNiSrTXQsVrukShSgzpqC1%2FTn3CAHPwfBO2LnIWLaxxZQCHm6q9dxWDryipkN4ABm6CC4Xz3V0eI27WwJpYHuZShDyWMQ0muibee3BSBTaQv9s%2Fb8Yp6fZfx78Z3r5c09%2FAw%3D%3D&SigAlg=http%3A%2F%2Fwww.w3.org%2F2001%2F04%2Fxmldsig-more%23rsa-sha256&Signature=J6ZGowOmcG9LMRsgIuUY1PNKwrwQL%2FbeUtl3z3uVIaK4zyAHgOsldkk7%2F5Gfms5qOdLYJSGem07Hgl0b6fIX8IgUh7%2FMaQ%2FNv4i1kHZCMzXU%2FQhw1YwSxTEtslIplTK9H%2FNkyYcoezm7ZBgUFptkYWJoqTs35K16CxoORZ9tS0vo6zyst1%2BTArKf52hF9LI%2Bb4bQF%2Bu58UYdmS88Hf44gNji0TuMIjOS%2B3WkgJ%2Fz%2Fv4EAyuM8LbZRldrGZ00SVpeUNL9DzYBNsAkyZx3wqHMBBXNV3l2Ie9O%2BUeYD438VlD2uT%2BhWEgJr2bZpp4rCu8woWHjQyg9DUMT6NG0C%2FGbxg%3D%3D
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: same-origin
Sec-Fetch-User: ?1
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.132 Safari/537.36
---
Query String Parameters
---
_saml_idp: https://cpsim1.catslab.ca
RelayState: https://cpsim1.catslab.ca:443/openam/SSORedirect/metaAlias/idp?resInfoID=s21023ca378ff0f99db67d8a9bd1d280dfbe2cf201
```
### idp?resInfoID=
```
General
---
Request URL: https://cpsim1.catslab.ca/openam/SSORedirect/metaAlias/idp?resInfoID=s21023ca378ff0f99db67d8a9bd1d280dfbe2cf201
Request Method: GET
Status Code: 200 OK
Remote Address: 52.235.25.50:443
Referrer Policy: no-referrer-when-downgrade
---
Response Headers
---
Cache-Control: no-cache,no-store
Content-Type: text/html;charset=UTF-8
Date: Wed, 18 Mar 2020 13:40:18 GMT
Pragma: no-cache
Server: Apache-Coyote/1.1
Transfer-Encoding: chunked
---
Request Headers
---
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Accept-Encoding: gzip, deflate, br
Accept-Language: en-US,en;q=0.9
Cache-Control: max-age=0
Connection: keep-alive
Cookie: JSESSIONID=4302CA40B401F6FCD2EFE674AA211312; amlbcookie=01; IDPSimulator=AQIC5wM2LY4SfcxVT3UASH74SY7jqd02SxCU3jv7yDsTSoY.*AAJTSQACMDEAAlNLABM1MzU3NDgwMTQzMjUxODI5ODAz*; _saml_idp=aHR0cHM6Ly9jcHNpbTEuY2F0c2xhYi5jYQ%3D%3D
DNT: 1
Host: cpsim1.catslab.ca
Referer: https://cpsim1.catslab.ca/openam/SSORedirect/metaAlias/idp?SAMLRequest=nVNNj9owFPwrke%2BJw0eXXQtYUVBVpG0XAe2hl%2BrFebDWOrbr52yhv75OIC2HlgOnSH7jN%2BOZyfjxUOnkDT0payasl%2BXscTomqLQTszq8mDX%2BqJFCEmGGRDuYsNobYYEUCQMVkghSbGafnkQ%2Fy4XzNlhpNUuWiwn7Lne7u%2FLh3ag%2FKkZQ5PlwV9yx5GtHGG9EIFGNS0MBTIhHeT9P80Hau9%2F2BmKYi%2Fw%2BexgMv7FkdV79XplSmf11HcUJROLjdrtKV8%2BbLUsW8SXKQGipX0JwJDiXjlTVyyQE0lDEL7cO4z6%2B2TyvsVQeZeAVBphpBcRV6VjywXqJrT8TFnyNLJkRoW8Wz62hukK%2FQf%2BmJH5ZP%2F2l2uu6jrBodyplmjekBkqQaIIHnUlt6xKcy%2BBX7TGTtuIOiJz1gUMk4439fC9f8cglaF2AfGWntETrob%2BI6bo70Mll05vFjfkFc1eaz5FquVhZreTxltJEZysI19HNiSrTXQsVrukShSgzpqC1%2FTn3CAHPwfBO2LnIWLaxxZQCHm6q9dxWDryipkN4ABm6CC4Xz3V0eI27WwJpYHuZShDyWMQ0muibee3BSBTaQv9s%2Fb8Yp6fZfx78Z3r5c09%2FAw%3D%3D&SigAlg=http%3A%2F%2Fwww.w3.org%2F2001%2F04%2Fxmldsig-more%23rsa-sha256&Signature=J6ZGowOmcG9LMRsgIuUY1PNKwrwQL%2FbeUtl3z3uVIaK4zyAHgOsldkk7%2F5Gfms5qOdLYJSGem07Hgl0b6fIX8IgUh7%2FMaQ%2FNv4i1kHZCMzXU%2FQhw1YwSxTEtslIplTK9H%2FNkyYcoezm7ZBgUFptkYWJoqTs35K16CxoORZ9tS0vo6zyst1%2BTArKf52hF9LI%2Bb4bQF%2Bu58UYdmS88Hf44gNji0TuMIjOS%2B3WkgJ%2Fz%2Fv4EAyuM8LbZRldrGZ00SVpeUNL9DzYBNsAkyZx3wqHMBBXNV3l2Ie9O%2BUeYD438VlD2uT%2BhWEgJr2bZpp4rCu8woWHjQyg9DUMT6NG0C%2FGbxg%3D%3D
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: same-origin
Sec-Fetch-User: ?1
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.132 Safari/537.36
---
Query String Parameters
---
resInfoID: s21023ca378ff0f99db67d8a9bd1d280dfbe2cf201
```
### callback
```
General
---
Request URL: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/passport/auth/saml/gckey/callback
Request Method: POST
Status Code: 200 OK
Remote Address: 52.228.62.155:443
Referrer Policy: no-referrer-when-downgrade
---
Response Headers
---
Connection: Keep-Alive
Content-Length: 3969
Content-Security-Policy: connect-src 'self' https://gluuserver-cc-01.canadacentral.cloudapp.azure.com https://www.canada.ca https://ajax.googleapis.com https://use.fontawesome.com https://lang-canada.fjgc-gccf.gc.ca https://cdn.canada.ca
Content-Type: text/html; charset=utf-8
Date: Wed, 18 Mar 2020 13:40:19 GMT
Keep-Alive: timeout=15, max=90
Server: Apache
Set-Cookie: connect.sid=s%3AHSGfFHxCZUAxNmtnbjjTEEHc2354mgoa.UeV1%2FO%2F7D5HZ7fizi9OJvVIL%2F5h7tiaEi2JgEGGp1%2FA; Path=/; Expires=Thu, 19 Mar 2020 13:40:19 GMT; HttpOnly;HttpOnly
Strict-Transport-Security: max-age=600; includeSubDomains
X-Content-Type-Options: nosniff
X-Powered-By: Express
X-Xss-Protection: 1; mode=block
---
Request Headers
---
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Accept-Encoding: gzip, deflate, br
Accept-Language: en-US,en;q=0.9
Cache-Control: max-age=0
Connection: keep-alive
Content-Length: 12331
Content-Type: application/x-www-form-urlencoded
Cookie: org.gluu.i18n.Locale=en; session_id=811511ea-6d9f-4685-8155-4635cd9d53c3; session_state=ad5af2be832439c29d62ebd287dee49cf8a773d43c77e01be60f70989e531125.36d0b57c-92d0-4649-b1cb-c69261ed71bc; opbs=c96733cb-c78e-4fec-afac-86cf1efc4516
DNT: 1
Host: gluuserver-cc-01.canadacentral.cloudapp.azure.com
Origin: https://cpsim1.catslab.ca
Referer: https://cpsim1.catslab.ca/openam/SSORedirect/metaAlias/idp?resInfoID=s21023ca378ff0f99db67d8a9bd1d280dfbe2cf201
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: cross-site
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.132 Safari/537.36
---
Form Data
---
SAMLResponse: PHNhbWxwOlJlc3BvbnNlIHhtbG5zOnNhbWxwPSJ1cm46b2FzaXM6bmFtZXM6dGM6U0FNTDoyLjA6
cHJvdG9jb2wiIElEPSJzMmRhM2JiOTI4ZTc3MDA3YTNjMWU5YmM1ODY5YzNjYWQyYmViNDllYjAi
IEluUmVzcG9uc2VUbz0iX2NmZjZkOTU3MjdiN2FiMDA0ZmI2IiBWZXJzaW9uPSIyLjAiIElzc3Vl
SW5zdGFudD0iMjAyMC0wMy0xOFQxMzo0MDoxOFoiIERlc3RpbmF0aW9uPSJodHRwczovL2dsdXVz
ZXJ2ZXItY2MtMDEuY2FuYWRhY2VudHJhbC5jbG91ZGFwcC5henVyZS5jb20vcGFzc3BvcnQvYXV0
aC9zYW1sL2dja2V5L2NhbGxiYWNrIj48c2FtbDpJc3N1ZXIgeG1sbnM6c2FtbD0idXJuOm9hc2lz
Om5hbWVzOnRjOlNBTUw6Mi4wOmFzc2VydGlvbiI+aHR0cHM6Ly9jcHNpbTEuY2F0c2xhYi5jYTwv
c2FtbDpJc3N1ZXI+PHNhbWxwOlN0YXR1cyB4bWxuczpzYW1scD0idXJuOm9hc2lzOm5hbWVzOnRj
OlNBTUw6Mi4wOnByb3RvY29sIj4KPHNhbWxwOlN0YXR1c0NvZGUgeG1sbnM6c2FtbHA9InVybjpv
YXNpczpuYW1lczp0YzpTQU1MOjIuMDpwcm90b2NvbCIgVmFsdWU9InVybjpvYXNpczpuYW1lczp0
YzpTQU1MOjIuMDpzdGF0dXM6U3VjY2VzcyI+Cjwvc2FtbHA6U3RhdHVzQ29kZT4KPC9zYW1scDpT
dGF0dXM+PHNhbWw6RW5jcnlwdGVkQXNzZXJ0aW9uIHhtbG5zOnNhbWw9InVybjpvYXNpczpuYW1l
czp0YzpTQU1MOjIuMDphc3NlcnRpb24iPjx4ZW5jOkVuY3J5cHRlZERhdGEgeG1sbnM6eGVuYz0i
aHR0cDovL3d3dy53My5vcmcvMjAwMS8wNC94bWxlbmMjIiBUeXBlPSJodHRwOi8vd3d3LnczLm9y
Zy8yMDAxLzA0L3htbGVuYyNFbGVtZW50Ij48eGVuYzpFbmNyeXB0aW9uTWV0aG9kIEFsZ29yaXRo
bT0iaHR0cDovL3d3dy53My5vcmcvMjAwMS8wNC94bWxlbmMjYWVzMTI4LWNiYyIgeG1sbnM6eGVu
Yz0iaHR0cDovL3d3dy53My5vcmcvMjAwMS8wNC94bWxlbmMjIi8+PGRzOktleUluZm8geG1sbnM6
ZHM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvMDkveG1sZHNpZyMiPjx4ZW5jOkVuY3J5cHRlZEtl
eSB4bWxuczp4ZW5jPSJodHRwOi8vd3d3LnczLm9yZy8yMDAxLzA0L3htbGVuYyMiPjx4ZW5jOkVu
Y3J5cHRpb25NZXRob2QgQWxnb3JpdGhtPSJodHRwOi8vd3d3LnczLm9yZy8yMDAxLzA0L3htbGVu
YyNyc2EtMV81IiB4bWxuczp4ZW5jPSJodHRwOi8vd3d3LnczLm9yZy8yMDAxLzA0L3htbGVuYyMi
Lz48eGVuYzpDaXBoZXJEYXRhIHhtbG5zOnhlbmM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDEvMDQv
eG1sZW5jIyI+PHhlbmM6Q2lwaGVyVmFsdWUgeG1sbnM6eGVuYz0iaHR0cDovL3d3dy53My5vcmcv
MjAwMS8wNC94bWxlbmMjIj5xeks1aER2VSt2ckFhNFh6Yy9STmVOUXdlbDlqbGVJSnh5aUJkSzB5
cmwxWkhmZUQyeURwWkRKUENpMjFDYzNIaTI0UnpnWG5zK01zClg0YSttZlNPc2RndEhVTW9JM3BI
L2Qwclo1WGtuclkzS0t3cW80dDhnL0pEVnBrUE5TRHB3UVRrblhWYTRxM25zeDhYbDdKdW9kQTcK
YWxLbGVlaXYybzBmNWx5c3Q1aDdFRFVCanBFdTY1SnVqdWdWZktkZFNSUTFuWjVqOUQ0Tk04em5F
WmIyZGkvcU1OaUxmMTZOK0crZgpnWUxCVFFjSlphV3FKcXpLc1dUSEYwakdSRnVNY0lxd2dzZmpD
QUg2T3Y2TVJwdVVyeE1DZTk3ZTBzWXdueDFhSG9KYzI1cXo3Y1hLCkNkYWRLaG82emxEM1NidDdn
Vko1WW9UbkNmUXFrRjY5djYxYkZnPT08L3hlbmM6Q2lwaGVyVmFsdWU+PC94ZW5jOkNpcGhlckRh
dGE+PC94ZW5jOkVuY3J5cHRlZEtleT48L2RzOktleUluZm8+PHhlbmM6Q2lwaGVyRGF0YSB4bWxu
czp4ZW5jPSJodHRwOi8vd3d3LnczLm9yZy8yMDAxLzA0L3htbGVuYyMiPjx4ZW5jOkNpcGhlclZh
bHVlIHhtbG5zOnhlbmM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDEvMDQveG1sZW5jIyI+MHcwazRS
Wm9VS2FlYmN0dHViQWJtaXR4YTdmeTNjVnV5a3RlRVhENEQ4Qmk2VE9PRUgxa0I3WlRQM0Q4c2dw
ZVZFWDFXenRpdlROMgp1YSthb2dzdHhSaE5LRXY1YXROaXNzb2ViYXdGN2VBZVVpYzFJY3lqVHYw
SkdHSklueWt0NERKTlpUSkE4R0ttdGluc0FzQWs1bWFOCkd1MllsbDhqTEJzVWgwbm96clhNV2Fx
OFhTL0gvdmgwWDFHUWN2TmRWc1ZOY3lxczdJLzY5Q3J5YndVWW81VGQwWUhUS1E4UEFwUTUKSkFL
bkNpVHlPQ2JPQlZZdzBCbzJMaGRHTHZTSC9nenFqWmFocTYvakFaTmlqUkNlZFUzTVcrcEZ1eWti
SE1qekFUTjhkZGcydUJQTwoxNUFTYlZpanJTV0dpQzk2R2VldG1iZlVLQVcrRndlRytVZ09zRGh3
a2RkWHJqTVcyVkVVRmw3TzFOcEJTRXpEcDV1OXYvZmRkWFRjCnQvUUp1MXUvTnFXZnRhSzNUNS9u
Nk9PcWw5WktRQnUzdFVNdmhzdFJCaC9LWmEwUitnK05Fb3pOVDJGZzZzRTBqc3VFM3ozbzhMbXEK
N05yeStTcUFiQVluak5QNk9iTWx5Q0xiMFhRLzgvMStQaHF4QWdpcTRpanQ2eE00cnJiSGZOek15
dDUySjVISWl5cEtXd2VaMmVkNApaaGMxQ0JrejZJMFhONFd2MUdlRzhyUkgzazRXNGcvdXdFMUdm
SG85cGU1WElsVFgwUHRYVFRBdG5NN0swWXJuQkRtdjJ1RnozNGZmCkpmYXo0NWk0RDRJQTBiVU10
Z3BRR3orZTVXaXJUandsQmVTV2lWYW9jeXpQS0JrVmxmaDdEY29KSUlrcEVFMStVbFhnYlRKSkNk
YkwKcTUyU251aHo1RWsyZ2VRazRzUHdwNXp0UVVkcE0rWDIzS0RqU1hrczlvdEhLbmJTU1JPTVVl
blpyajd5bi9SUnVjZHgreCs3dWcxLwpRellaemYvV0h1YXE0R1RyZjVwbXpjckU3L1VYaWp4UE93
OVhTS0d1QTBGMTBMWTlqeVluZUs4R0VXQTdPa1FiWEpZV05PYXZDcHlOCmttUmhXUG9pd0JIbXNS
ald2V1RVemlPbWtLbTNZeFIveFdaWCtERENOWS9BV21yNGxPS1AwUTVRSjMyVEdXK2VxQ2JMVGNH
RkhNVVkKTGF1S2VUTjVhSDFmWG43QVFvVjlTQlRucDJPcmtZQjAxWE5KRm5iN2FWZSsvMWdlVGxN
VkFCWWl5RUVXQmNFcks5THNCWFZVM2VZeAptQ0VsczgvUklvRG9IWnlva004Tll6MDdmZ2YyTHY3
VE5HaHRUeUF4czRtY3E1TVMweDRRelA5YkVWdGNiUlp3QkUreXNPRHF0NVVzClB1cmZoY0JvZmJB
Z3UrSG5VMzJJNWR1QWE5dENVQmZ6ZXZuVjZxb3kvQ0k1RXRSRlhLa04ycE5RZWpjQjJrZGJydGk0
RFNxRkhvdkwKYjRzNkVGODgzc1hxWDAvQ3ZhUVVzMW1aVnBtLzJKaVBYTXg2eE93V1VIQklNc0pC
WHQzMU1LMm9mbjd5MzBuc1dFcHJMUmc3KzdpUQpTMm1LMkE2WmtRbSt5V25FSmdFbjZLSmRHejdn
QytmcjZZV0tnendrWjZpMmV3N0plMXVvY2RWWVBDOE13aFMwRmYwYzM0M21icTN6Cmh5MmZleGpK
bzFubGI5TW04RzBsT3FHbXZHUTNGQURyUXRMZ2tlclpFb0FUb2dRNnltWHo1TE9xdnhSOTdlZnQ3
ZDdUQWx1bUVMa3YKNVRpZTNyTnE3YUpnbGhsbUlLRCtobVV0NEZsRWo0cURMc01oM29lZm1tZU5H
ZXRtenp5alZ2QVZ4MjdSVFFwOVZCdFJTaU9LZlhjdgpZeUtnK1hKbHB0cEpNaEF4RW5VcE03WkFZ
RW05Zmc3VWkwdG1mblNYbkZpaTNSbXZKTE1PQkc3eklLTzlZeDNuZFJad05iUkpxeCt5CkdNSGxs
SGdlaUdmc0syTWVydisxVVJrcFQreDlwMnRKeDdxdG5zaGQ3RWEyQVFBdkN6citRb25JbUxIa3gr
VlNSRW5CU0lhS2orUXIKbUVhVkhNZzhBSzgwbCtVMUp0WkZYbVgrVHJEWlArdzJwOVdUbVVrRjV3
Q3R6ZkxKODNCM2czdkdiRWtBZWFiNjVjTm1MYzJ3Z3puYQpDdXhXMDJyM0pVUFJVNWRpME5qRms0
cDNJY3VNVWlueDlqbEt3UWdLUzhuZVdOMExwdFFiZngwcUUzRFZwcW5rYWoyejBkWStVcUxoCmJW
SnZSRFd4QUdNSWx0bVpSN3BBOE9ZUUNTL01QbFJHWkh4c0tLNDMxWHBZYy9sRCtMSm1HU0hoeml5
c1hDYmxaTndPUHVSQ1MzSVYKamtiYjZkMG1pT0ZUTmZIeUR6VjFJdXBWOVRxM2U0d1UrdkpsSmhs
QktSWmE0NFpwK3BrWnZocExvUTIwYWp6Mlk1UnVNWEovWW1jOApKOS9aMkNFZEZLWTUxak80UDBx
ZkREa0xYR2FERTJwY1JLbEducTVHUXdwWkhQSjkrZE1paHlqMDY4NjZrVGQrQ013TU1BcXJuVFRl
CjVNcDIvYkxSbG1CMkNTUHN6R00wNHZRREV4OWYzOXVxM29oS2FkamNxMzVxRXpTUnlTdFhveTBj
TTFJN3pzUFFzdFB6MVZ6Qzk2akQKcDVBZmtya004bS9DcVgwejQxWFNTZ1c2WElkQU4zTndSSDJC
bklIYmlaMms0M1gzWTBMSmtwSTdySTBiRmZ4di9nMHpXY0xDTFNpQQo1M0NTNER5dkJYNUVXSkFI
b3RiQWhsdFpZMHZGcWtvZnFRdUZIb0RzVUVTczNrWVBNVlJZRm40NTg0MGx0ajRNdjE5NVp1M01w
Ynp1CnZWbHFPbWlRZWVvS05BMjR3Z1hoaXUxMjlTWGxLZkZNVWJna0ZXTTU5T3Z3RGNaa2llQWhn
ZW04QUhsbUsvd25sdi9qYWs3TVd0SkYKTlBjNjRlbk9EVktMNkxxdHhmWGs2Nm92R2VwOENkd2Zj
U2FxWEtGdVE4Qm50dEVuaHNXQ1pjMDFvMHZzSXQrUTBiYThWekpnd2lHTQpMUmhZVWJtbkdwSGZD
amx6MERnbmVmb2RpRzljK0pZRjV4amNiMWpPT2poeGlibWF5SEFlM0phMDJRVFVaSFZFbWVTc0Ey
R09kTVkxCmtHWDlVaDZobkNNbVlJR2lWbFlWWG00RUNaV1c4WWRTaXdyY3hNNGFvbWVMS2twU0d2
UXFtbUNkOFZZVDAyN3JiWGorRU8vSjlWcTIKWlF2eVJRK0tXNGU1NWJibmZjL09TRG9GSWZ3L1dV
MzYyTFEvbStMQmRaWVJtazdLVWdUWjZnemtrM1IwQkpwdDYzSWNtdThsTjBTTQpQNCsxbS8rY3pJ
eERFTVl2cHVvcGhRa0ZGNi9OakJKRGlyRmhtOXdaMHJoNCtXeVV5RjVnQmwwM05MY1N3R1dCQUxo
VGl6UzBFYjJhCnBtejdNa0hZejlLZmc0ZDdkeHYxK0FLYktmYWlaRVllRjE3c0thWDMxa3VPMXg1
WkZpbVdmTjVEYkR0WUJlazZvZEZtQllLMzNnMXcKTDZEaDB5dmNCU1BoKzBPYVpFM2JBYlpOUjNV
S1grb0JSM2RnS2pMcGVOMDJHaEIvUWNzR1l2ZVlLcUEwVmxkNWhyNk9iOEZKWThyOAovZDZtT3Vu
c1lCRHVSMjNpZHY5YWpzRDcwUStRZkJrUzUxSnpYL2toNUgyTlVRUG53R0lRYXljcU84a283Z2ZP
WE15QlNxRW5oVlRtCmFObjh5RmhVQ2Q1U1hoR3NEMk5iZ2swaDdoSEV1R0dIUDB3OGZHcCtnN2Vs
aS9rbGxSbXFyOEp2VGFzYXpKSHVyRzVySmE3b2owREQKQkhKNDZjcGlDYkYrV293dGpTSXdibUx6
RmxmaWN5ZmdZOXhER3FvUk5ybTV1dFlUN3REZDF2ZFIrL1dHRm9CSURJZFRXWlhZZStMMApSajls
UkZVMW5pSUlmNXVxVjhqMDNmK1B3NlM3MkkzM3N5bjAwZVF2L09XVUVsZXA0THN6UmZsNjNkdE5H
S0ZvNVBLWkZWcXFzYkhFClJOblhYWktSZ002REZVVzY5SjM5NUltQjZxRnZ4czZSRWlONXl0N0Fu
UVpGdkwrSXZhc0tuK2NOR2FYRFhxbjdqQnV1ZUNLenlhNEMKMm9GSlYzRW1iM1VBVWVJMGxEUXhZ
UHBKSnpwTUM3ZHZGNDl4cjN5blEzc0lzeExKUjNrbFVQQVM2czlUS0dwZ1pidUtZQTh5UDQraAoy
VUN4Z2ZBUTZHUzJpTks5UktYVGcxalh6Z05oTER4Tkl6OFd2ejR4NGYxYUpNcUdLdjhVbzNHNVZU
YjR6MW9GQ2xSN2NyTnVjNXI4CitITGJLa0RwT0pDdVh5aGZxaE9FVXRtVjJoR09pQVhtNS9qeE8z
d0JMUStBOVdpVWYzckVQR2JOVVJBTlFCZEVxWHpnNjFIdGpFeEIKaytSL0lCQUVxRm1uU2JTck5H
ZWVPMVZjem5RWEVDQ3hzQlgvemgrYkszRUpvOHhXeTJZRXUvZDdvZjlFK2trMWZKOGszUTc0d0Zh
NAp5cnJhN09HWitvZWJuQUcyem9NSDRad2VmaDJRY01nMXhQTkNCWm1LaGhMMWhxb2Y2clNvb3pL
RXk5WTNsRm15VnhPYXdjZWczaUZiCjlDcjNtdXZKYjZTenhJNnB0bVBQTnE3VWtWMXVybTI4MjRU
d2RTYjdKVUJONk5mRk13d25SRHZkNlI0akw3UkEwYlNnMXpBVmJnSkUKTXJRbEUvckp4OHlHenU1
Vk04WnRPMHBDY3Z1V081czE0Y3lSR0pMbHVvaUxuVTA5aFUvWHdUZCtWSGhBdXVUQlZtODErdndS
MURtWQovV2pXZnQyWW1GQnBTbTJUZE0zSFdHdGJCRU94YkM0MnZPWGxEWSt0RnZ2OURMajBHV3ph
TVRIZ0FDWG1BQTc5SW05ek5Ldkw4L3BTCmg1ODNuOVEzSUhqWHYrRjZ2ei85MjFYMFpxZzNEbDRR
eWRlcjcxQ0hudEJ2cHFmUUFnckxsNmhhbnBoYklrVFBkMFpkNXBRaFhtN2QKWXNsN05ieG9uakEw
MVd0bmVSdGY0ejlyRHBvcUtCdG94VkUvVWp0bDhNenVoN1Mvdi9pZXVmWFNtbklRUVo1K3FmdW5E
NjN4c3FXSQpBMzhrR3lTN1VGZVN1SzV6VmtYSVljYmphdXlWdU1XbHY2TWNoUEt2bzBIZHZyOUZm
ZUpCdnBDYXRvd0RVTXRnZCtTYTZHZnJwR0FOCkRmUVRVYTJCc1ZGYnl1SFY1MkMzNDhCa1dMYWQr
NG1ac1RNME1ZUTVkTUJ4ekJmK2liOHFnVDhwSTVqWHIzSUwvUTkxb3I5RkgvOFAKNi9ybkJIVWdv
NllndE1OUW5uMnRCNWtUSWtWNlNYUlhUS0xScmFid2FVN0ZLeW9mS3hpcDc3eFFOdmp6ZlNPdlhm
S0s3YW1YYk9qZwpYamJYT1I0MmRCY0kzTCtuY0E3aTNKSGdDa0RCN1FCNHBqL29SZTV0N1pKcGkz
VU5vdDVya1FTYmFmL2lEcTllSFVEQ0FkUHhnSjdYClg2TjJXQlhzUmRIVUxVaFZBT3JQRVlqZ3pj
RGRhSUNOSWhGM1gxa0c4NHVNZVVld1gxUWZsOS8vYjZ0QWVWbzRYaGs1VGJCanBaNUEKbkpUWWxz
YTdKL3VENEZveXNOallhQkJudklRLzYxaFJ2ZTlxbGRlNlJaK1Z2YkxtSGRBMFU4RTBBQUNaTmpT
Y0xwSWR6a1djVnFvYwpIR2ZWOUxQTzJXVmhMS2JXb3pSMlJRODhWWEF4VUNacXZ2OUo4cW9OZkZF
QnBqN291OUtIOXhXbEZoMkNzR3FjMTFKdWl6SmpUQVp1CldtZ3VFWUdRa292djFtUXFyalowSXkz
eWdzc0hNdnd1RXBmN1lJcnpkQVBJZURvalNZZDhkbVZJNEJkL2FnYzdqNmk4eFZhTUI4b3YKRE8y
SGE1SWVTMTBBazVmd0tiZ3YvUllTRCtaclVxak0rNlZiZGwyZmIyT2hqd2xldTBhY2N1QzJ2bWI1
SWExOWJ2ejdEM1lFMk5TWApZZTB0ZG5lMk5LbmNxUDIrUHRsdTM5bjRYRTR6emFjRElqLytHaWtp
WmMzNURIN2YvM0U2LzZHdTFHVUhqa1pYV05LRkJMSktsZDVkCnBLZ1Yrc281ejg1Nk5LSW1YZkRB
U25KSjJkM045UWR4cjU0UURkdFR1Um85bDRVUmNhcldxSWJQN2U0MHFvWGZYUWtrK0E0Q2REWW0K
Wlc5WndQMFhwMUUvR2xMTzNUODNTYVdZSVovMTFHVDNYalpLNTFQc21VY3Q0R1laaitsVE1XS0No
TG1IdDllajFUN2krdFpCVzZTQwpGY2FVQXVTTEtwdi9oNGFQek5HVzRVUlhoSG1lRkZJVW5RdmZs
Mk5Uc0UwbFhMVkJZaHA4cW41OEY3TFIzMWZHQU55Q3p1Q0ltSElrCitpZHhhSThTMUcwc3EvOVB0
Szc4dDdOMzltNDJoZTFqZzRyWWNRaHBsdFZyTjhVWXk2cXI3Qlc4TXZqL3RtWlF4ZEJwQU5HV1RH
R3gKZ2dzUGxyb296eEwvQ3ZzZW1PV0RKZG5ZYTZmOCtpUXZQWDJKQjJJTnNnL1RHaGNPa1krcTNp
RktleXpUajR4cTVvRW54QWd3R2NjYwp0QmJhQ3RlbndNMVJWR2lJT3M5VFAwN3ZhTCtqS3Y1anlj
MThSR3RLaHNCbGp0bXl3UFV0RmlhRHBOZEpqdUk3Ti9kcGIyblJFaGZDCjUvS0RxMFJQQ1pRNlJS
RlNWTTRFNzMwV0Y5QkplKy9YL0xKb0Qrc2htaFpGY0ZRWGRrWWRhWEZpWjlJWUhLT21yMk5oQ2hY
ZmxzNHQKYUFPV3RKM0IzNFp4eGJzYWlrOFl6eEROdENYMURWZm5jcDkvV1VzS0tTSVVzYTZIajFw
NEt4VEJrdnR4ditESldNWXdwRllyUDB4dgorZmJNRHpmSmdwMmhQQmlFcnArU3p5NG1WTHFSaU55
c09NWjNYR1lURy9hUEo4djhjSGRwUm1rVUFtTUVvb1dsbU1JSVdOQmpFRFgzCitBQU5YdWlTSDJo
ZmdrZ0ZjT3lUYlArc1hwV2lQbW81QklnOW1Xd0ZJbCtuMmZMV1pzNnZEb05EMWpTTHR2aHZjeDJC
MEdwQ0UwTGwKR1F3UGRjVFFCZS8za0x4T3ZHUnNhakd6OHFVSVd1WHBSL04xWFZRTFNSeXIrK29s
ZjQ1MjBhSTF2VzhhaWFzN3lSczlqdW1BQkZPNAoxblZNSXhxMlNYaWtEZ0htUCtKdVFRcnViL0xx
R3BVVUJ0RkkxcFNUQ29EV0RGMEYyd3UxbGZTSTZFNkxYaVVTSzZ6aVhiTEUxY3JmCi82Z2ZCT3RK
S2I4MzNHQmwxdkR5THdxVlZMbStUR2c0Uyt0QWJyWTh1T3NqYnJ5blNNS2dOREM3WlZUb252dmRL
blZMZ01aS1VrM0IKbDJjVzM4KzVFeW9ZcW12a2VUZXpJY0hPaTQ3L3ZMR2tOWVMvOTFEcU5wZzBB
MkxyU1lwZjF6Q2pRWlJlSHVCOHYyMUpTV05PbFVvbApoYmRhS0hkbk4zZnM2UVF0VndPbm9YSVZU
R1VzaUs2MW04ZmhIMm1iSVAwbFk3OTNHdjZNeGY2N3JQbk5SalVnai9GSU1XejZGZytXCld3L1hO
UkFKcm9jOG9aZXFxVUtzdG1QYnQ0aUNJdjhONURzT05iT1ZMVUxMdG1tOHQ5RlI4NlJqcjE2bkg4
bUU1Y3htdE8wTVovZUwKVll5eHllMXFKZlZXWElXNEpLLzVjVW5OK29YS0QyQ1d2TUxUWDJnNElk
VDVyV293WDJvdjRrWit1S0h2Rm5hend3R2g0NlJtdmVQVQo1NVhCcGZWY09xTEF6Z2VmYTluQUU1
TEtIR3V4dDRmeEQraHVkalBXdmtuM0NSU202VEVlT3lUOU1sRkxzdkRNU01PL0YwY1Z5RmJuCnRq
M2g2Vkt2bnNkUnllOVlqY1U3TGtlQnRIdGNiblhrRUdhRzBlWHpVWC9oczAvKy9ETzNHMVIxWnNJ
ZE5taExGVG9pQ2NjSlJKU2oKQWR4VVVBS2U2S2FEcEhpNW9CQWFEeU9zUDZaZ2VmQVpSS2VsOUZV
UjBCQmJCSjVVYlNINU9XT1BvNjQ3UEs4UTFkVkcwM1ZaVGdqaApJZTd4S05ZZ2JoSWM3T2lXZUFm
ZVNYVDVZcjdFVmJKRGY0SU5Dck9kbkZKdG1xNVlFVnJRZlZOVGwrbXBXcDVuZ3FtR0I3RlE4eWx4
CkJGRVIySEllSFN4NHZCSE1RbGtDd2YwMTJpeXVBUGNBM2o0NzVYTTBTRExxb0w1eEZzNkJhbElp
dm16clNuckQ3NWNJNlR5TnpwQmwKbnlvK0N0NXFRTzdCOElReWRsb2lDWFQxQm9aTnQ1c0pWK2lS
MjdmYUhKdlRxTXRtVXhJYU1VNHM4Uk9ua1dXbnh1TTkzdlZRSjlBdwpabU9hV2FIZzVwUmMrWXdE
ZWdQZTloU3h4UT09PC94ZW5jOkNpcGhlclZhbHVlPjwveGVuYzpDaXBoZXJEYXRhPjwveGVuYzpF
bmNyeXB0ZWREYXRhPjwvc2FtbDpFbmNyeXB0ZWRBc3NlcnRpb24+PC9zYW1scDpSZXNwb25zZT4=
```
### lang
```
General
---
Request URL: https://lang-canada.fjgc-gccf.gc.ca/v1/lang
Referrer Policy: no-referrer-when-downgrade
---
Request Headers
---
Provisional headers are shown
Accept: */*
Content-Type: application/json
DNT: 1
Referer: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/passport/auth/saml/gckey/callback
Sec-Fetch-Dest: empty
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.132 Safari/537.36
```
### postlogin.htm
```
General
---
Request URL: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/oxauth/postlogin.htm
Request Method: POST
Status Code: 302 Found
Remote Address: 52.228.62.155:443
Referrer Policy: no-referrer-when-downgrade
---
Response Headers
---
Connection: Keep-Alive
Content-Length: 0
Content-Security-Policy: connect-src 'self' https://gluuserver-cc-01.canadacentral.cloudapp.azure.com https://www.canada.ca https://ajax.googleapis.com https://use.fontawesome.com https://lang-canada.fjgc-gccf.gc.ca https://cdn.canada.ca
Content-Type: text/html
Date: Wed, 18 Mar 2020 13:40:19 GMT
Keep-Alive: timeout=15, max=88
Location: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/oxauth/authorize.htm?scope=openid+email+user_name&acr_values=urn%3Agc-ca%3Acyber-auth%3Aassurance%3Aloa2&response_type=code&entityId=https%3A%2F%2Frp1.tbstest.catslab.ca&state=eyJ0eXAiOiJKV1QiLCJhbGciOiJub25lIn0.eyJzdGF0ZSI6IkM2c0gycFE2VHEiLCJjb252ZXJzYXRpb24iOiJlMXMxIn0.&redirect_uri=https%3A%2F%2Fgluuserver-cc-01.canadacentral.cloudapp.azure.com%2Fidp%2FAuthn%2FoxAuth&spNameQualifier=https%3A%2F%2Frp1.tbstest.catslab.ca&nonce=PQOtpccU1v&client_id=1101.2eb78fce-15c2-4faf-86ea-e86a6504e547
Request-Context: appId=cid-v1:28ed79ce-6df8-41d0-b78c-f1466b0e7d96
Server: Apache
Strict-Transport-Security: max-age=600; includeSubDomains
X-Content-Type-Options: nosniff
X-Xss-Protection: 1; mode=block
---
Request Headers
---
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Accept-Encoding: gzip, deflate, br
Accept-Language: en-US,en;q=0.9
Cache-Control: max-age=0
Connection: keep-alive
Content-Length: 1084
Content-Type: application/x-www-form-urlencoded
Cookie: rp_origin_id=https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/idp/Authn/oxAuth; JSESSIONID=node01doxw8mqznx8a1lndiaq3q6iaz1.node0; org.gluu.i18n.Locale=en; session_id=811511ea-6d9f-4685-8155-4635cd9d53c3; session_state=ad5af2be832439c29d62ebd287dee49cf8a773d43c77e01be60f70989e531125.36d0b57c-92d0-4649-b1cb-c69261ed71bc; opbs=c96733cb-c78e-4fec-afac-86cf1efc4516; connect.sid=s%3AHSGfFHxCZUAxNmtnbjjTEEHc2354mgoa.UeV1%2FO%2F7D5HZ7fizi9OJvVIL%2F5h7tiaEi2JgEGGp1%2FA
DNT: 1
Host: gluuserver-cc-01.canadacentral.cloudapp.azure.com
Origin: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com
Referer: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/passport/auth/saml/gckey/callback
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: same-origin
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.132 Safari/537.36
---
Form Data
---
user: eyJhbGciOiJSUzUxMiIsInR5cCI6IkpXVCIsImtpZCI6IjU5ZTE0YzAyLWZkYTAtNDQ4Ni04ZDdhLWNmNTFjYjQ0OWIwZV9zaWdfcnM1MTIifQ.eyJpc3MiOiJodHRwczovL2dsdXVzZXJ2ZXItY2MtMDEuY2FuYWRhY2VudHJhbC5jbG91ZGFwcC5henVyZS5jb20vb3hhdXRoL3Bvc3Rsb2dpbi5odG0iLCJzdWIiOiJCNzhjbVhjMnk4Zk9RU0xqcGkwS3VPWTl6MFBOIiwiYXVkIjoiMTUwMi44NzFlN2ViZS0wMmRkLTQ5OWMtOTRlMi03MGQxMTY4MWJjMGQiLCJqdGkiOiJjZWQ1ZGExNC0xZTRlLTQ0Y2ItYjliZi04MGIzZjg0ZTc4YWYiLCJleHAiOjE1ODQ1Mzg4NDkuNjAxLCJpYXQiOjE1ODQ1Mzg4MTk2MDEsImRhdGEiOnsicHJvdmlkZXIiOiJnY2tleSIsInVpZCI6WyJCNzhjbVhjMnk4Zk9RU0xqcGkwS3VPWTl6MFBOIl0sInBlcnNpc3RlbnRJZCI6WyJodHRwczovL2dsdXVzZXJ2ZXItY2MtMDEuY2FuYWRhY2VudHJhbC5jbG91ZGFwcC5henVyZS5jb218aHR0cHM6Ly9jcHNpbTEuY2F0c2xhYi5jYXxCNzhjbVhjMnk4Zk9RU0xqcGkwS3VPWTl6MFBOIl19fQ.JmNBL1s0rcYxuvlib34vlkckEce04HkeTAq9ARmgiRgsIT2b491TywG4gtRdXqFtNHp3x8QlAfj6yXB2qFO-2RY8HEosHrbqzsyQ6_4mdkPFKJdORRgBQywPfs64WqYHVAarmHL0xTKMjrnSG4dT3V6zx-J6GSH56LUlt1IXtVesf30jUFRsjXlqNenYbP5Kph1N3C9reGDvSBeduZlhoqjZO2cdmvJkVi3GjSo5FhbV4q5rVUCZpzkysp4yucxtVFdwLVdpWCaOqJSu66-sWyKKM-oFsTFdRgtMdjN33DXLQ5o4XoPXCC78e5wm8BqvQI6k8V52ozbADr5szNURBA
ui_locale: 
```
### authorize.htm?scope=openid.. 
```
General
---
Request URL: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/oxauth/authorize.htm?scope=openid+email+user_name&acr_values=urn%3Agc-ca%3Acyber-auth%3Aassurance%3Aloa2&response_type=code&entityId=https%3A%2F%2Frp1.tbstest.catslab.ca&state=eyJ0eXAiOiJKV1QiLCJhbGciOiJub25lIn0.eyJzdGF0ZSI6IkM2c0gycFE2VHEiLCJjb252ZXJzYXRpb24iOiJlMXMxIn0.&redirect_uri=https%3A%2F%2Fgluuserver-cc-01.canadacentral.cloudapp.azure.com%2Fidp%2FAuthn%2FoxAuth&spNameQualifier=https%3A%2F%2Frp1.tbstest.catslab.ca&nonce=PQOtpccU1v&client_id=1101.2eb78fce-15c2-4faf-86ea-e86a6504e547
Request Method: GET
Status Code: 302 Found
Remote Address: 52.228.62.155:443
Referrer Policy: no-referrer-when-downgrade
---
Response Headers
---
Connection: Keep-Alive
Content-Length: 0
Content-Security-Policy: connect-src 'self' https://gluuserver-cc-01.canadacentral.cloudapp.azure.com https://www.canada.ca https://ajax.googleapis.com https://use.fontawesome.com https://lang-canada.fjgc-gccf.gc.ca https://cdn.canada.ca
Content-Type: text/html
Date: Wed, 18 Mar 2020 13:40:20 GMT
Expires: Thu, 01 Jan 1970 00:00:00 GMT
Keep-Alive: timeout=15, max=87
Location: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/oxauth/restv1/authorize?scope=openid+email+user_name&acr_values=urn%3Agc-ca%3Acyber-auth%3Aassurance%3Aloa2&response_type=code&entityId=https%3A%2F%2Frp1.tbstest.catslab.ca&state=eyJ0eXAiOiJKV1QiLCJhbGciOiJub25lIn0.eyJzdGF0ZSI6IkM2c0gycFE2VHEiLCJjb252ZXJzYXRpb24iOiJlMXMxIn0.&redirect_uri=https%3A%2F%2Fgluuserver-cc-01.canadacentral.cloudapp.azure.com%2Fidp%2FAuthn%2FoxAuth&spNameQualifier=https%3A%2F%2Frp1.tbstest.catslab.ca&nonce=PQOtpccU1v&client_id=1101.2eb78fce-15c2-4faf-86ea-e86a6504e547
Request-Context: appId=cid-v1:28ed79ce-6df8-41d0-b78c-f1466b0e7d96
Server: Apache
Set-Cookie: org.gluu.i18n.Locale=en; Path=/; Expires=Thu, 18-Mar-2021 13:40:20 GMT; Max-Age=31536000; Secure;HttpOnly
Set-Cookie: session_id=811511ea-6d9f-4685-8155-4635cd9d53c3; Path=/; Secure; HttpOnly;HttpOnly
Set-Cookie: session_state=ad5af2be832439c29d62ebd287dee49cf8a773d43c77e01be60f70989e531125.36d0b57c-92d0-4649-b1cb-c69261ed71bc; Path=/; Secure
Set-Cookie: opbs=c96733cb-c78e-4fec-afac-86cf1efc4516; Path=/; Secure;HttpOnly
Strict-Transport-Security: max-age=600; includeSubDomains
X-Content-Type-Options: nosniff
X-Xss-Protection: 1; mode=block
---
Request Headers
---
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Accept-Encoding: gzip, deflate, br
Accept-Language: en-US,en;q=0.9
Cache-Control: max-age=0
Connection: keep-alive
Cookie: rp_origin_id=https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/idp/Authn/oxAuth; JSESSIONID=node01doxw8mqznx8a1lndiaq3q6iaz1.node0; org.gluu.i18n.Locale=en; session_id=811511ea-6d9f-4685-8155-4635cd9d53c3; session_state=ad5af2be832439c29d62ebd287dee49cf8a773d43c77e01be60f70989e531125.36d0b57c-92d0-4649-b1cb-c69261ed71bc; opbs=c96733cb-c78e-4fec-afac-86cf1efc4516; connect.sid=s%3AHSGfFHxCZUAxNmtnbjjTEEHc2354mgoa.UeV1%2FO%2F7D5HZ7fizi9OJvVIL%2F5h7tiaEi2JgEGGp1%2FA
DNT: 1
Host: gluuserver-cc-01.canadacentral.cloudapp.azure.com
Referer: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/passport/auth/saml/gckey/callback
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: same-origin
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.132 Safari/537.36
---
Query String Parameters
---
scope: openid email user_name
acr_values: urn:gc-ca:cyber-auth:assurance:loa2
response_type: code
entityId: https://rp1.tbstest.catslab.ca
state: eyJ0eXAiOiJKV1QiLCJhbGciOiJub25lIn0.eyJzdGF0ZSI6IkM2c0gycFE2VHEiLCJjb252ZXJzYXRpb24iOiJlMXMxIn0.
redirect_uri: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/idp/Authn/oxAuth
spNameQualifier: https://rp1.tbstest.catslab.ca
nonce: PQOtpccU1v
client_id: 1101.2eb78fce-15c2-4faf-86ea-e86a6504e547
```
### authorize?scope=openid+email..
```
General
---
Request URL: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/oxauth/restv1/authorize?scope=openid+email+user_name&acr_values=urn%3Agc-ca%3Acyber-auth%3Aassurance%3Aloa2&response_type=code&entityId=https%3A%2F%2Frp1.tbstest.catslab.ca&state=eyJ0eXAiOiJKV1QiLCJhbGciOiJub25lIn0.eyJzdGF0ZSI6IkM2c0gycFE2VHEiLCJjb252ZXJzYXRpb24iOiJlMXMxIn0.&redirect_uri=https%3A%2F%2Fgluuserver-cc-01.canadacentral.cloudapp.azure.com%2Fidp%2FAuthn%2FoxAuth&spNameQualifier=https%3A%2F%2Frp1.tbstest.catslab.ca&nonce=PQOtpccU1v&client_id=1101.2eb78fce-15c2-4faf-86ea-e86a6504e547
Request Method: GET
Status Code: 302 Found
Remote Address: 52.228.62.155:443
Referrer Policy: no-referrer-when-downgrade
---
Response Headers
---
Connection: Keep-Alive
Content-Length: 0
Content-Security-Policy: connect-src 'self' https://gluuserver-cc-01.canadacentral.cloudapp.azure.com https://www.canada.ca https://ajax.googleapis.com https://use.fontawesome.com https://lang-canada.fjgc-gccf.gc.ca https://cdn.canada.ca
Date: Wed, 18 Mar 2020 13:40:20 GMT
Keep-Alive: timeout=15, max=86
Location: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/idp/Authn/oxAuth?code=bb2d415b-8d9d-428c-bf27-1f3e6d5a6b1d&acr_values=urn%3Agc-ca%3Acyber-auth%3Aassurance%3Aloa2&scope=openid+user_name+email&session_id=811511ea-6d9f-4685-8155-4635cd9d53c3&state=eyJ0eXAiOiJKV1QiLCJhbGciOiJub25lIn0.eyJzdGF0ZSI6IkM2c0gycFE2VHEiLCJjb252ZXJzYXRpb24iOiJlMXMxIn0.&session_state=ad5af2be832439c29d62ebd287dee49cf8a773d43c77e01be60f70989e531125.36d0b57c-92d0-4649-b1cb-c69261ed71bc
Request-Context: appId=cid-v1:28ed79ce-6df8-41d0-b78c-f1466b0e7d96
Server: Apache
Strict-Transport-Security: max-age=600; includeSubDomains
X-Content-Type-Options: nosniff
X-Xss-Protection: 1; mode=block
---
Request Headers
---
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Accept-Encoding: gzip, deflate, br
Accept-Language: en-US,en;q=0.9
Cache-Control: max-age=0
Connection: keep-alive
Cookie: rp_origin_id=https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/idp/Authn/oxAuth; JSESSIONID=node01doxw8mqznx8a1lndiaq3q6iaz1.node0; org.gluu.i18n.Locale=en; session_id=811511ea-6d9f-4685-8155-4635cd9d53c3; session_state=ad5af2be832439c29d62ebd287dee49cf8a773d43c77e01be60f70989e531125.36d0b57c-92d0-4649-b1cb-c69261ed71bc; opbs=c96733cb-c78e-4fec-afac-86cf1efc4516; connect.sid=s%3AHSGfFHxCZUAxNmtnbjjTEEHc2354mgoa.UeV1%2FO%2F7D5HZ7fizi9OJvVIL%2F5h7tiaEi2JgEGGp1%2FA
DNT: 1
Host: gluuserver-cc-01.canadacentral.cloudapp.azure.com
Referer: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/passport/auth/saml/gckey/callback
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: same-origin
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.132 Safari/537.36
---
Query String Parameters
---
scope: openid email user_name
acr_values: urn:gc-ca:cyber-auth:assurance:loa2
response_type: code
entityId: https://rp1.tbstest.catslab.ca
state: eyJ0eXAiOiJKV1QiLCJhbGciOiJub25lIn0.eyJzdGF0ZSI6IkM2c0gycFE2VHEiLCJjb252ZXJzYXRpb24iOiJlMXMxIn0.
redirect_uri: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/idp/Authn/oxAuth
spNameQualifier: https://rp1.tbstest.catslab.ca
nonce: PQOtpccU1v
client_id: 1101.2eb78fce-15c2-4faf-86ea-e86a6504e547
```
### oxAuth?code=
```
General
---
Request URL: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/idp/Authn/oxAuth?code=bb2d415b-8d9d-428c-bf27-1f3e6d5a6b1d&acr_values=urn%3Agc-ca%3Acyber-auth%3Aassurance%3Aloa2&scope=openid+user_name+email&session_id=811511ea-6d9f-4685-8155-4635cd9d53c3&state=eyJ0eXAiOiJKV1QiLCJhbGciOiJub25lIn0.eyJzdGF0ZSI6IkM2c0gycFE2VHEiLCJjb252ZXJzYXRpb24iOiJlMXMxIn0.&session_state=ad5af2be832439c29d62ebd287dee49cf8a773d43c77e01be60f70989e531125.36d0b57c-92d0-4649-b1cb-c69261ed71bc
Request Method: GET
Status Code: 302 Found
Remote Address: 52.228.62.155:443
Referrer Policy: no-referrer-when-downgrade
---
Response Headers 
---
Connection: Keep-Alive
Content-Length: 0
Content-Security-Policy: connect-src 'self' https://gluuserver-cc-01.canadacentral.cloudapp.azure.com https://www.canada.ca https://ajax.googleapis.com https://use.fontawesome.com https://lang-canada.fjgc-gccf.gc.ca https://cdn.canada.ca
Content-Security-Policy: frame-ancestors 'none';
Date: Wed, 18 Mar 2020 13:40:21 GMT
Keep-Alive: timeout=15, max=85
Location: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/idp/profile/SAML2/Redirect/SSO?execution=e1s1&_eventId_proceed=1
Request-Context: appId=cid-v1:28ed79ce-6df8-41d0-b78c-f1466b0e7d96
Server: Jetty(9.4.19.v20190610)
Strict-Transport-Security: max-age=600; includeSubDomains
Strict-Transport-Security: max-age=0
X-Content-Type-Options: nosniff
X-Frame-Options: DENY
X-Xss-Protection: 1; mode=block
---
Request Headers
---
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Accept-Encoding: gzip, deflate, br
Accept-Language: en-US,en;q=0.9
Cache-Control: max-age=0
Connection: keep-alive
Cookie: JSESSIONID=node014324my2nzksb4ms3fjyylnvh0.node0; org.gluu.i18n.Locale=en; session_id=811511ea-6d9f-4685-8155-4635cd9d53c3; session_state=ad5af2be832439c29d62ebd287dee49cf8a773d43c77e01be60f70989e531125.36d0b57c-92d0-4649-b1cb-c69261ed71bc; opbs=c96733cb-c78e-4fec-afac-86cf1efc4516; connect.sid=s%3AHSGfFHxCZUAxNmtnbjjTEEHc2354mgoa.UeV1%2FO%2F7D5HZ7fizi9OJvVIL%2F5h7tiaEi2JgEGGp1%2FA
DNT: 1
Host: gluuserver-cc-01.canadacentral.cloudapp.azure.com
Referer: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/passport/auth/saml/gckey/callback
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: same-origin
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.132 Safari/537.36
---
Query String Parameters
---
code: bb2d415b-8d9d-428c-bf27-1f3e6d5a6b1d
acr_values: urn:gc-ca:cyber-auth:assurance:loa2
scope: openid user_name email
session_id: 811511ea-6d9f-4685-8155-4635cd9d53c3
state: eyJ0eXAiOiJKV1QiLCJhbGciOiJub25lIn0.eyJzdGF0ZSI6IkM2c0gycFE2VHEiLCJjb252ZXJzYXRpb24iOiJlMXMxIn0.
session_state: ad5af2be832439c29d62ebd287dee49cf8a773d43c77e01be60f70989e531125.36d0b57c-92d0-4649-b1cb-c69261ed71bc
```
### SSO?execution
```
General
---
Request URL: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/idp/profile/SAML2/Redirect/SSO?execution=e1s1&_eventId_proceed=1
Request Method: GET
Status Code: 200 OK
Remote Address: 52.228.62.155:443
Referrer Policy: no-referrer-when-downgrade
---
Response Headers
---
Cache-Control: no-cache, no-store
Connection: Keep-Alive
Content-Security-Policy: connect-src 'self' https://gluuserver-cc-01.canadacentral.cloudapp.azure.com https://www.canada.ca https://ajax.googleapis.com https://use.fontawesome.com https://lang-canada.fjgc-gccf.gc.ca https://cdn.canada.ca
Content-Security-Policy: frame-ancestors 'none';
Content-Type: text/html;charset=utf-8
Date: Wed, 18 Mar 2020 13:40:21 GMT
Expires: Thu, 01 Jan 1970 00:00:00 GMT
Keep-Alive: timeout=15, max=84
Pragma: no-cache
Request-Context: appId=cid-v1:28ed79ce-6df8-41d0-b78c-f1466b0e7d96
Server: Jetty(9.4.19.v20190610)
Set-Cookie: shib_idp_session=2daf51993d143fa645671a59732c2cf3a36e2ebfe0ff29e04605921bcd13ef0f; Path=/idp; HttpOnly;HttpOnly
Strict-Transport-Security: max-age=600; includeSubDomains
Strict-Transport-Security: max-age=0
Transfer-Encoding: chunked
X-Content-Type-Options: nosniff
X-Frame-Options: DENY
X-Xss-Protection: 1; mode=block
---
Request Headers
---
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Accept-Encoding: gzip, deflate, br
Accept-Language: en-US,en;q=0.9
Cache-Control: max-age=0
Connection: keep-alive
Cookie: JSESSIONID=node014324my2nzksb4ms3fjyylnvh0.node0; org.gluu.i18n.Locale=en; session_id=811511ea-6d9f-4685-8155-4635cd9d53c3; session_state=ad5af2be832439c29d62ebd287dee49cf8a773d43c77e01be60f70989e531125.36d0b57c-92d0-4649-b1cb-c69261ed71bc; opbs=c96733cb-c78e-4fec-afac-86cf1efc4516; connect.sid=s%3AHSGfFHxCZUAxNmtnbjjTEEHc2354mgoa.UeV1%2FO%2F7D5HZ7fizi9OJvVIL%2F5h7tiaEi2JgEGGp1%2FA
DNT: 1
Host: gluuserver-cc-01.canadacentral.cloudapp.azure.com
Referer: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/passport/auth/saml/gckey/callback
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: same-origin
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.132 Safari/537.36
---
Query String Parameters
---
execution: e1s1
_eventId_proceed: 1
```
### fedledapplication
```
General
---
Request URL: https://rp1.tbstest.catslab.ca/RPSimulator/fedletapplication
Request Method: POST
Status Code: 302 Found
Remote Address: 52.232.135.10:443
Referrer Policy: no-referrer-when-downgrade
---
Response Headers
---
Content-Length: 0
Date: Wed, 18 Mar 2020 13:40:22 GMT
Location: https://rp1.tbstest.catslab.ca/RPSimulator/setCookie?clf=1&return=https%3A%2F%2Frp1.tbstest.catslab.ca%2FRPSimulator%2Fresponse-eng.jsp
Server: Apache-Coyote/1.1
---
Request Headers
---
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Accept-Encoding: gzip, deflate, br
Accept-Language: en-US,en;q=0.9
Cache-Control: max-age=0
Connection: keep-alive
Content-Length: 13131
Content-Type: application/x-www-form-urlencoded
Cookie: JSESSIONID=F0B6BE5C429142418447715E32D7094E; _saml_idp=aHR0cHM6Ly9jcHNpbTEuY2F0c2xhYi5jYQ%3D%3D
DNT: 1
Host: rp1.tbstest.catslab.ca
Origin: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com
Referer: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/idp/profile/SAML2/Redirect/SSO?execution=e1s1&_eventId_proceed=1
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: cross-site
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.132 Safari/537.36
---
Form Data
---
SAMLResponse: PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiPz4KPHNhbWwycDpSZXNwb25zZSBEZXN0aW5hdGlvbj0iaHR0cHM6Ly9ycDEudGJzdGVzdC5jYXRzbGFiLmNhL1JQU2ltdWxhdG9yL2ZlZGxldGFwcGxpY2F0aW9uIiBJRD0iXzAwZGRiZGQzYzRlN2Y2MWEwZmUzNmQxNzQ0N2JiNDY4IiBJblJlc3BvbnNlVG89InMyZWMxYTI1YzhhZTllM2UwY2RmZmQ5ZWJmMGY0ZjNkZjgxYjMxZjM3OCIgSXNzdWVJbnN0YW50PSIyMDIwLTAzLTE4VDEzOjQwOjIyLjA5OVoiIFZlcnNpb249IjIuMCIgeG1sbnM6c2FtbDJwPSJ1cm46b2FzaXM6bmFtZXM6dGM6U0FNTDoyLjA6cHJvdG9jb2wiPjxzYW1sMjpJc3N1ZXIgeG1sbnM6c2FtbDI9InVybjpvYXNpczpuYW1lczp0YzpTQU1MOjIuMDphc3NlcnRpb24iPmh0dHBzOi8vZ2x1dXNlcnZlci1jYy0wMS5jYW5hZGFjZW50cmFsLmNsb3VkYXBwLmF6dXJlLmNvbTwvc2FtbDI6SXNzdWVyPjxzYW1sMnA6U3RhdHVzPjxzYW1sMnA6U3RhdHVzQ29kZSBWYWx1ZT0idXJuOm9hc2lzOm5hbWVzOnRjOlNBTUw6Mi4wOnN0YXR1czpTdWNjZXNzIi8+PC9zYW1sMnA6U3RhdHVzPjxzYW1sMjpFbmNyeXB0ZWRBc3NlcnRpb24geG1sbnM6c2FtbDI9InVybjpvYXNpczpuYW1lczp0YzpTQU1MOjIuMDphc3NlcnRpb24iPjx4ZW5jOkVuY3J5cHRlZERhdGEgSWQ9Il84YzVmMDgzNGRhZjM2MmJkN2JkNDQ5MjY2ZjY0MzIwYyIgVHlwZT0iaHR0cDovL3d3dy53My5vcmcvMjAwMS8wNC94bWxlbmMjRWxlbWVudCIgeG1sbnM6eGVuYz0iaHR0cDovL3d3dy53My5vcmcvMjAwMS8wNC94bWxlbmMjIj48eGVuYzpFbmNyeXB0aW9uTWV0aG9kIEFsZ29yaXRobT0iaHR0cDovL3d3dy53My5vcmcvMjAwMS8wNC94bWxlbmMjYWVzMTI4LWNiYyIgeG1sbnM6eGVuYz0iaHR0cDovL3d3dy53My5vcmcvMjAwMS8wNC94bWxlbmMjIi8+PGRzOktleUluZm8geG1sbnM6ZHM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvMDkveG1sZHNpZyMiPjx4ZW5jOkVuY3J5cHRlZEtleSBJZD0iX2QxMjgyNDNjNDU0YmM5NWRiOTlkMzQ1ZDdmNTAwNjUxIiBSZWNpcGllbnQ9Imh0dHBzOi8vcnAxLnRic3Rlc3QuY2F0c2xhYi5jYSIgeG1sbnM6eGVuYz0iaHR0cDovL3d3dy53My5vcmcvMjAwMS8wNC94bWxlbmMjIj48eGVuYzpFbmNyeXB0aW9uTWV0aG9kIEFsZ29yaXRobT0iaHR0cDovL3d3dy53My5vcmcvMjAwMS8wNC94bWxlbmMjcnNhLW9hZXAtbWdmMXAiIHhtbG5zOnhlbmM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDEvMDQveG1sZW5jIyI+PGRzOkRpZ2VzdE1ldGhvZCBBbGdvcml0aG09Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvMDkveG1sZHNpZyNzaGExIiB4bWxuczpkcz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC8wOS94bWxkc2lnIyIvPjwveGVuYzpFbmNyeXB0aW9uTWV0aG9kPjxkczpLZXlJbmZvPjxkczpYNTA5RGF0YT48ZHM6WDUwOUNlcnRpZmljYXRlPk1JSUV3VENDQTZtZ0F3SUJBZ0lFVmFBQXZ6QU5CZ2txaGtpRzl3MEJBUXNGQURBK01Rc3dDUVlEVlFRR0V3SkRRVEVMTUFrR0ExVUUKQ2hNQ1IwTXhFREFPQmdOVkJBc1RCMGRUVXkxVFVFY3hFREFPQmdOVkJBc1RCekZEUVMxQlF6RXdIaGNOTVRrd05UQTRNVGcwT1RNNQpXaGNOTWpVd05UQTRNVGt4T1RNNVdqQkVNUXN3Q1FZRFZRUUdFd0pEUVRFTE1Ba0dBMVVFQ2hNQ1IwTXhFREFPQmdOVkJBc1RCMVJDClV5MVRRMVF4RmpBVUJnTlZCQU1URFVkRFEwWlVRbE5TVUZOcGJURXdnZ0VpTUEwR0NTcUdTSWIzRFFFQkFRVUFBNElCRHdBd2dnRUsKQW9JQkFRREJVamc3YzdGQ3d1c0dMYUdIQitrUFpRR2VFeGVtZjV2OFhYd1pTV292ai9vckZoM0JYS3UwdFB5Wm5FR2JrYmEwTmJRago4U0pTTzlzVEdyNno1TWZnV0gzNXE0L1Y1YlZxRUFuallyUHFNaEEyUGdmZFVoKzFQS1orK2hyK25GWkxIK21mT3R1SnRjcmdxblZrCnBhS1BCL1ZjM1NHc0RLdkdydXg3WjNzbjZXK1RxUDVCaVRZR1d4allHMVJDMnhoaVA1NTdXb3FPdzJ4QlgrRlpuVUVRL3c2bnVPd3YKOFNqNjFrclM0a1Q5ZE1Oc1dKNzMrWFJMazBHbCswVCtMNFBiU3FEWHlGTGQzZndEOUJNSnQ2bWZ3a0o5VE9qS0FRWmF6cGdhc3huRApSYTZtbCswRGUvYmo5Qm5OaWxnUXJtZ0pTMllPaEZiVndLdEV2V05TMHY1ekFnTUJBQUdqZ2dHL01JSUJ1ekFMQmdOVkhROEVCQU1DCkJTQXdZd1lEVlIwZ0JGd3dXakJZQmdsZ2ZHVUlCUUVCQXdRd1N6QkpCZ2dyQmdFRkJRY0NBakE5R2p0TWFXMXBkR1ZrSUV4cFlXSnAKYkdsMGVTNGdVMlZsSUVOUUlDMGdVbVZ6Y0c5dWMyRmlhV3hwZE9rZ2JHbHRhWFRwWlM0Z1ZtOXBjaUJRUXpCWUJnbGdoa2dCaHZwcgpIZ0VFU3d4SlZHaGxJSEJ5YVhaaGRHVWdhMlY1SUdOdmNuSmxjM0J2Ym1ScGJtY2dkRzhnZEdocGN5QmpaWEowYVdacFkyRjBaU0J0CllYa2dhR0YyWlNCaVpXVnVJR1Y0Y0c5eWRHVmtMakFrQmdOVkhSRUVIVEFiZ1JsRWIzVm5Ma2hoY25KcGMwQjBZbk10YzJOMExtZGoKTG1OaE1HRUdBMVVkSHdSYU1GZ3dWcUJVb0ZLa1VEQk9NUXN3Q1FZRFZRUUdFd0pEUVRFTE1Ba0dBMVVFQ2hNQ1IwTXhFREFPQmdOVgpCQXNUQjBkVFV5MVRVRWN4RURBT0JnTlZCQXNUQnpGRFFTMUJRekV4RGpBTUJnTlZCQU1UQlVOU1RESXhNQjhHQTFVZEl3UVlNQmFBCkZEQmdBRkdSUWFFeDBqdU52N1ViVTZoN1hUVTBNQjBHQTFVZERnUVdCQlRqeUdyTWJXOVcwWUx4dlNMUmhZMk5oc3B1MlRBSkJnTlYKSFJNRUFqQUFNQmtHQ1NxR1NJYjJmUWRCQUFRTU1Bb2JCRlk0TGpJREFnU3dNQTBHQ1NxR1NJYjNEUUVCQ3dVQUE0SUJBUUF6cEhFcQprcDFybzlzTGxuNDJsaG9nRHZqTnBPWFFkQ25kT0EzV1JjM3g4a0NWK3RJMlNnZ00xKysrYkE0Y3RuVVJwTDFhNlJFSVZlZXhQYkxrCmlCY1BHYXM4bCtTd0hHRWROajF6aVJkczRCeXJpOStORitBcUQraDF3Mzk0Q2tWQzFaeCtJU29IYkU1UjV2SVhEUUNxaEpDWGRDbncKVFNCcnErUjFTdEJJZXNSeUM3NUtSK21KRFpld21Xc2hMVmZUTDVBdDJPVTJVZDVRK01RZHppOStWdUFOTXM2L2tvazNKWU15eCtzSgpVZG5wd2N6YWVSY3ZpL2R4cDNScmhvWW5ybHd6M3BKOUV6MmxDYXVYMHk2b3llaDVGZS82WEJKODI2NEgvdjNENjVZTmtFQzRsMU9YCmx1cFk5bWtSR3dDWWRnMTVsRjM5Q010YVpUNmliWTVvPC9kczpYNTA5Q2VydGlmaWNhdGU+PC9kczpYNTA5RGF0YT48L2RzOktleUluZm8+PHhlbmM6Q2lwaGVyRGF0YSB4bWxuczp4ZW5jPSJodHRwOi8vd3d3LnczLm9yZy8yMDAxLzA0L3htbGVuYyMiPjx4ZW5jOkNpcGhlclZhbHVlPkRqZm95Ly81QldFMTNla3M0aGY2THZCVmN5bXJyc0V1ZG9Kc2pXN3VDZi9lSlVtQnArMldxL0ZLWnNlYWdOYXUrOVpKdHZ3Z3l6N2ZkMkhhNzlsbWdDTFR1WEtmb0xPRjlWbFRlb1h4YjFQZXNwK0EzazJTMjhNNXFOaWsxSCtXVWNoZFQvTDQ2aytDREdVVGx6WEhmMjl0MDZiTEt1dm9EREd0S1JmMzdDcXhhQXYrcHhqYlk4Qmc1Y3dVK0p0NWcwNnZBblpHSFNFT2F5Wkw2dlkzN200eDZGQUpTODZCc3Z6bmxOZFc2dithdm9SOUFmeEJ6TElhd05MSVJsa1ZjdjJ2SUxkTGVDQXpxaE1jNi93WldUWFBDVk94ZktNK1JxenhYRlpQSklRWXhHTm1zSTJOa2lqMHhON0dGb2NsVVd6MjhZT2krcU5WOVQvWHFuRXZtdz09PC94ZW5jOkNpcGhlclZhbHVlPjwveGVuYzpDaXBoZXJEYXRhPjwveGVuYzpFbmNyeXB0ZWRLZXk+PC9kczpLZXlJbmZvPjx4ZW5jOkNpcGhlckRhdGEgeG1sbnM6eGVuYz0iaHR0cDovL3d3dy53My5vcmcvMjAwMS8wNC94bWxlbmMjIj48eGVuYzpDaXBoZXJWYWx1ZT40bnh2L1ZsVHVsUW1pZGxUWnFwRFRQdjVXTTBCeTQwWVZLNVNHNVM0eUo2OXN0NjVCUHltbnRYdmlDUFgwL3hVY0lRUGN1clVFNWhNZXdVZ2NqdnNQTmk3TlprR0pPME80VEVIWHFadUtROG43MmtURVdDMkhMMENKdUd5VExkdVNPRCtyNlBVSllJYXJQSkZLNE5YczJDZkd6MWN3RWJhRE5ZQSt2Ui9Mb2RZSmpUaXMzb0sxSlB5bFhVWk1VSjdZVmF3MVB4NVZzYmVJQU1vZ3RVWm9KZzBrbDNtY1pDcGZnR1JtNWI3UnNZZ3dTcGJaa1FPSTFkVjUxQnUzeVhRM0NpSm5QZHhKZlR0VXBpRUpyS3hIb0FDRlhIRyt0UW9CY2kzdmV4clZ5TlZYN2ZtNHhFL3NaanZXYUhMMGVhSUY0U0pyZmNQUSswNDlvSnJ3WXRzN2pJZ2xMWmEvblRtZTVSQ3RmZGl2RlpMdkdqZGJKNnQxbU5OL09kZWdySXFlN3RzVXZ3T0s2RGVyOXpGLzlxS0hSZXlraWIzc1BUVkxzT1lGZVJLM2x4UjRKNitTWmhybEp1S1dMc1RINnN4T2g2VTJzeVpoc2cyb0taejAzSzg5YlR2RzNSZ29RK3c3Qno4YmJ1MlA0Q1dmVm1paHhOVng5UUcvYjMxcUlSYUNHMXdhbzVPUkFPWjUzRHhUMmNqVHlYT29BRHRIakQ4SEkybnFLTzk5WjlYYmc3VVJSNUJEV3BoM0ozWEl6RjREQmlpT24xMlpnR3BwTkNBc0VNYjVsWndvUThDUWkwOStGVWZlRHFmRVUxYXBuN2JCMEFyaERBTVNaaUNGZmViSXFReHYyTjZrQzRZWkV6RW42S05OOHl6TXVlTDh1RFVvandyaXMxQXZZbm1NcDJtL0g4aXFXNnowKzdXUmk1eDlUSVBuVVIzZE0vWWkxOFlDakZwNTQvSFU4c0ljNlQyYnk0UjdpL0RYUTVLRjRZV2dVMEI4K0xNNy8rdFJrOWp6VmhlckZQZ3ZKcjR3bWdWcC9NTGhYSCt5NGFOY2RXall5bCtHQU55aVh5VGo5T0dVZERjY0pXOTVTZUlYMmRBQksvY0UyRkFkT0w0SGFZYjVkT0Z0cGpqcUJwRkFCVVZWRFEvN0RPbG9ZNnNNdGVVTHVUMjNHWlc5RCtRMmxKblJtZ1l3OFNseU9ad0dkRTc1SERMR2ZSS2ZpdUhKUDNFRlIrcFNCdFVZRlBJMGVCNmdiWkdzYkd1ZmxxQlVZYlVIWjBUZXBuTkZoUitPU0lDR3VvaGRiUjhnMExqcUk5Z24yc1BlVWY0Q0NNTTczZERLLzhMUkh2YWxuL1U4NFdCSEpKUU5oYjZHTnFYN2pHdnBMZ1ZTeEpuWnhyTzJUbDRoWUZTNmhxZWRic08zQUR4YW1BNlFHL1pscWo5K0JrcWpSdVNkZ2lNa1Zqdzh1TW1iZTdHWC94WnZBL0lSU0hja3ZlV3pCcmw4Qi9YMnd1b2o4U1BYaGhJMmlvMTNpaGlidGRhYnB2bVVJMkRaTkhvdDNHQWZFN0Q0d1BuZEZmZFo0cURodTlPSDZINmNidWVObTB4WU8zekxERFpHN01JRStuZE1YRlZ4Z1VVMkRJSEtiWnIxN1BPTEFVN1RKY01vSkpiaGtxeUdUK3liZVdTVUtlNHpCbWh4aUxCTFRpV3FBam1jbTRqZzRiU3l3YlhQcTFsVzF6d1laY1l4L3Z5S2VORVBvd0tEcG5nVFlrZkZIb1NCOWtCaFYzUEhudkl4MkRsYUJQaTR1ZG95b3lLRzdDSnZudzF0cUMrWUFXTlF4bHpzMHhNTHFIaFJBWGdVYVN5dkJwT3l6QXY3YUtHay9LMCs1THV1dnJydEc5SHR5VEVGOTg1QUVucEJ3eXJnMHJVWUl2dUJFbDZUYjJESEMwYjM3cEZ0eC9pZkJkbWQrWC85N2RnNnhzOGsyWC9OK1JiS3VpdUtBdkh4TWhVTWlFRG5La0o0L2QrWjEzTnpZVGdlc1FYOXFOaUp0dzM0KzRvMGk3U1lJdmF3dVE4ZUNrWm1VejlGSHNiT1l4R0tJb1F6VnIvTnd2alR4WEtkNi9PTjdqZGdreFkwZHJiclNsZC9SNFlHbFRob1dOUnVDMzlIOFBZd2xGdXEzcHlXU0dhaUlITlVHS01ITkRJSGlWejBHQXVXTXB6aElsZ1NYM3Y2Q2dWMW1OOEt4OTlLMmpmVjBrMHNIL0dSc2kwY09EYTFpYWMvS3BYVlpCaWhhZW5hbXEvSXBlck13NjhmV3VUMFJDbEYwaTZ4bit5eHU4YVFIZFAwejhUYTEzcUpHeWYvMGc5T0tVbnBQQVdodFZoOGxQcFNUVHpNak1wQUlmVWYzRHpEcmNvcCtLaEdtUHVoN2tEUklaUWpLRUhMdmhhYWM3L2sycFlTMUlhS2MrZUM5UW5WWHV1Ym1IZy9sYnIzVGFSM1lqZmdnMTlGaGxBL0lVR3R1SU5qMlNyZHNBQ2JOcnVjVUhJSnREekxCN2x5MVoxdnpJZzhzdHVHRGpLZ3hpejlIQllvNnhmQUxLdlkzdTh5SnIrenBSbTd1SWR3a1RIdGNxakpQVTNLc3F4eDRxYzlubVJ1c284WDBabWU4bFJSaTcvOThvbkFuWFIwZ2l6b1FJMVBiRUFPaDNiV2FFd093Y2Z0MmczVUxnU1ZPbWhvTFFaR3F3SU9uZWRiSWZ4MmNFSFYrQXNhWnRyVklHK1BQOEVabUZpOG1hVjdDdDh6dlk5aTd4VSttVk1NUTQrYmROam83WG9Wb2FQdUhwajgrTEhDbWNPZlVHeXljSmo1MU0zeFFXSlJMeCtlOU5NMDRNaG1rMUtPQnFWZDQxdWxLUWJGd290OXZxQTVvenIwTmhDendyVEtwckY1dlQyV0d6RTBqVGxJUkxHeUlwelcrWnVWNW5lekFPdEpaUnFmZHlQYlR5TjgxUy9RUWZjSDRYTFkxcDZaeTVwRDZrcEd3MS9LbGVPUmxhaEVJWmttYjl1VCt6ek0yeUNHWFRvdHdpRnJEL01TWGJCU3ZjUzZwcnFwQXg2YSs3VnprSXRMN0Q0YS9CZllBaHlhMDVCM0pVKzRHaFlxQkpCTWE3Nk9sN1BZWVlxUzQ3YXRFWWFKUVlqSk1samp0cWJsSno0NEZNRlZWNUpFUmpLSnV3ZGZZd1psMHduQmZCakRKK1V5b2tDeS92RklGSXU0VGVYcTNIZDJXaWRpbUhYVGlaUlRqRGJBSnZST2o0RUg2SGVzZS9RUmQwajY3SGF2VTFjc1RWVXFZUjcrVkRKZmVrSTFCSS85TGx2Zmt5KzFOZjQ5NGV6WHE2bWVxMkpJQXYwYlhsYXd1bUI0RGVhc3VMdWdpRjN3cFZCQ09rTjJQNDNLUk1teXYrd0pEdE9QclQ3cGdJMFQyeFlycWZoTUEySlhLTDNpUHlBSXRCS1lJNXZhbDY1QnlWenIvZUNhLzJicjRLRkltM2JRN3FaUXFRRk11U2JySnNmWTVFa2tTVjFsOURXbjlaRkpBRHMxZzhPb0wxako0ZnZTbVdtVFFUUDd6OUZMdXo5NWVlV0lFMlMxY3VHR011WVppM2J2cU1BL1dYcmZJL2JzdUg1OUtBbGJaaDBTd0d2eEFmbzVGNGE2aDJDQVNwWHZVMGFROHZCZ09Ddlh1b2IrNVp2dW5rdkdRRWdBRzh2aTRabm9hZWZBL2J6dlhTZDh2ZENsbnh2bmZxSDgvVmNXUVVuUXdiWkJnOFNYMW5pTGJwYklUVTFZYXZLVUVmYnhyMEpoOHluUUsxZFRIdVpQR05qUnl3dnVLeDk4emIxS3F3VnVvY012VGJ2Z3djam1ZMkRJaGRzejhvU1BtU1NSZ3g2N3RGOHcwajB1M1FmYUJSQmVDTFZiUnRYazllMkpCQmtLZmN1LzVrMkx1OU9RdDJUQmg2ZURmWXpJSDhvbjZGRURxa2gzeFloN1UvRHJERkdJZ1AyL0pvUXNMWmpqMUduM1liaWhWV0FCdDhCVTFWNHR1Qk9UVzdLNUh3Y0c4S3l4YjRMZ0w3eWdFQWdndUc2dFF1dFcycUNnbXNwd3grb3hlTVpwYkVURUFFVFVXZzk0alQ4TWdoR2lyREFGVUR0QVNsL3hjdkZSWk92bEJUa3h4ZUNyamRsd0NaanFjUXdIWHRyd1c2aVpjSmlSbXNLYlFBRlo4b255ckt1dVZpS3JoOEtES1oyR0tKdE41aVFGOFJYb0ZTRGU5V3FxRXJtNkNUZlBHNyszQmptUjAwdHE0Z3FUL3RkT05mU2c0L3NVUjVXdmkrd3NpNEpaaTJYeExUaE52VjlZMzBidE1vNnZmRXNVdTN1ekwxbjJ3a2o4c1lub3JkZEdzNjc1ZEVibXY4UTJZZWduRWdCNUJ3TnRWb1NOWUZHZC9nUjkzL3oycmF4UkcxcE9WK1h6eFVMZDVSRTRhMVdZZHM4ZFRWVyt0STIydVhFNGdCWUIwa1lzeGNHcEYyK2Z1dlY1bEZTUHBpWjE0U2t6T2lIQmdnSDZEcUNsbGFxa2MrYWY4UUdlN0dMS0didE5ha3FBQzhEa0lCTDB2cmNjcitpTlluMERtaDNINXNhQ3NhY2V3N0lvSE45U0M5L09pSjRYR0pHSWhjcHF3S1kxRWlYOEhLRm1nOGxidkFWSGpybFhOR3YzaDVTaGlhcnlqbDR0dmdnTkptdk52YWtVRWVqUTZFZnpLdEJSa1M2NGQvcTc3czdnUzV1YkFSNHhUZEtmd3RmRy9IWGFhUWRVVHRKd0EwVVdMOVBaZ09VenRGM1AvYmFWM0p4Rm5sQ1E4cnZxSENBSVBXckJkdHlpYjNKbXhrTnVsWDY0eVE3S3M0QXUzQ09LT2VuWmhFY3BVUXVubjZxaVhaVXpkTnhyOG1vRXhzUEVhNUx4cmhpWHdPSjF3eHhnMUJmTmhUVzVzK0lSQXJJKzNHZGRWdTVjNVA1d0FjTCt2T2JkZTMxRHZmZ1NJTWNOVkQwS2tlL3c4U2NEZzVVdS9TQzhsOGdISEw4MWhZZDZLdGdaSnFia2dkZnIzRFhUbkNRVUtjNG1CaERWUUp1U1MxSGNVOWhGZm1jb1BhM2VvN0owS0hWRkpNeTJkeExEUDVRdW1CUUhIdzBkRXNoMHQxc1l3S1RGNE9PQmdqVkM4cHpKaVNCNDFJYWoxWWdaQXUzWWlaa1lDSGNsZ1pKVXR5TG9yL1MzRithOStaU3ZpaC94TTI0MEdyaVoxQytGSHF2NWs3c01UQ25qemhpejdsVDJ4cHQwMEdTSnpWWFZQZUhtd01QOHlWc0NRMHdOZ09lUHlFMnNveTNSMklyOHNHZlpxYjZYUHM2MUJLY1VPOE5kZWZ4dkFzaVJ6dTZ6dkNHOFpOM29ZVWRpL3ZJSk53N1RjVVFZdkhhcnhkQ1ZPVmtFd3U3RXlKeXVEaDFrNGxUMHVoUzd2Q1FJcmtFUFdvOTlGeFdNWnM5YmhuQUhoVlFTMTVmeE5jVWVYOEJrQnlKV1ZCbTZPbGhNbXlEbVZTek5NYVIwZ05tcHRncTJ3WlVGYWRBTUdUR2Z1Q0VYWEQ0MFNuYldVcndWRDloU1VSMVQ4OUg3dHcvU1ZCRHRYNitwRXo5SFJGRkJBQnF5UlFWVUlxRU16dVJEMlc2VFZWRVNJQmZEam5pU3hMbHBkQU90TExUSHhRT2t2NjdtN1FMaTh2Smt6cGkzaGFiR3dTa0gvbTFyRnJSUis2N3ZaUzlvN1haQjFqL0VLTDMxTzYxOTNOY25BL1BNWEZtUUZLYnZIaVZDdEdxR2ZjRCttV1ppdkE5QkI0S1kvbFBIelRralNjVXYvc21RTFliQ3YybEdLb1NKTzV5amc1dGVFeW53cmxsSzJJZlQ5eGlmc2lMdC9JNEpEbWptdzRIYkZhY1VyYTYyVUtUNTJEQWtxVThiQ0lxOXhJYXlnem00MHUvZi93RmVoNGxKZkpQMkgzSTYxYXJscXJYT1FiNWJjZm04Qy9mNXkzczlsR25YQWhLQ3R4TWpER0QzU09wNWVyYUs0cTVKbTk5ckQzd05NZ2hESGJUNzdmR3NlR080aCsxdEZyNGRiV2xicStoeWZMWVR3U1VqZFNTM28xeld4dVVLbnAxTnVrY3ZqR1ZuY2UwRGVVMm9TemgvWWRaeUo1WGM4cEtPMDEwOUtZemdSZUlZYnNiNFlJSjZWRmJWei81S1JuZ0s0VGZ4NXZOUWsrVzl5WU52KzJ3c1BhNlFjaWJSRFZUVVRtaEhiNE5nczdsc24zekpwd0lxYXdHZFlQb20zZmMyOURRY3ZhMkFscStsNmtqNHQvMk9hM1V3Z2xrVEFIcWNvOXBUeDVkdjNNL3o1R2NqMmJJUHBKWUQ0ai9lZElPME5peThQUUN0UkJyZDlKZWJscFg5REJkTjhVTHlPdHJVMWFueFc1SFFFMzlKN3l1VCtPRFgyeDFaU3QyMmlXNzBWaSsvSnBZMWI5Mk1mOWZ2NWthYnBaN1RzMjF4eXhIRDA5dlg5OHdZUFNocFJuNmpTVi83RXdHUXJFODRySXplcDBJdXJkSXJGZnlJcmRWM0tHNm9SNjRaVHNIdlM3K3lqSmFRQkVnK1krcDhlYnkvdnlxQU1lSFdYUGF3cC9SaG1jLzRIb1JpQzNqTmE1UGZJUW92ZDFsblVYU2lFckluS1NUUS9sV1JrZDZRdFNqSFYwenVPUVVveDgvOUNlTStzNUsxMVBreG1EeER5Z0pjSVpSL09NVmJyeUxGSSszMkV1UmpHMjZXekRoM3IrcWluanRvV3FBRnQrQzZDOXNlb2dRekdFM3pKNGY1anNuejkrSkwreXMxcXVia1U0SWNueFQ3QXFCRlUxREFsalRyY2REOUFRcnpEbjZZWk5Nb2lGR3gwQ2dXbnNYbUVmUHdTRGJLV2dzWTlJczVxMjNKRU1LTExiTnkzSTlTT0VweUJLelBsak5Gb3RTSThIK1RVb1Z0U01XWUFDKzhZNFRDMUN6UUwydVhkb25YeGV3aUQwQVVTMTZycHRqdHY2TEgrWXovNGNTbDh4WUtNMDRyVFNpRGNUL2dNSEJBbEx5eElsMnBFWEhPbkExeGFTUkpnT0ZydmJnRGJHd2pYWXZaY3JET2FFOHg2Tyt6OC9RTnBLY3lHYk9CKzdQVEFVT0hMbyt2QXZkVjNIRENQWitvUE1QWW9jNGE5dkxkMWQvZXFzOGpwYXNsUSs0RVM2TXNvV1YwaW9oTG0wS24rNmlIUjBKWUZqUmx5bTd3SmIrQzFrMUVwWWRXbytqWS9NMWppSzUwdVRNN2ZvZzhlOGVQdmprRWpMTWVKQmNyOUxqTEF1WDVSb2Rla2hCWmFWNE94T2dzZlN6THFObVVRMDJJRVdVdjZ4YXNNOGdESGZFOW9zbUxKck9RNmJuUTJ1a0NFUXNaWW92YnlicnN6dnMyZ0dweFNEbHEwRGVtSFJTK3VhSi9xWXp5MENZZGlZb0dRZ2duQ1FwbmxGZGdmelp5cUFxTXhRSkp5N2tKZWUyZVAxaXJ3S09XQW5ZOGFrSEt2UW12Q21Nd3NqU1NHVUplRmsvZ0RZVklsNFhYejV3R3h5cEhzWVdlSk5DVWV1bU52RGxNSDVYYm5aeWI3V2NFNGlrK1ZpTDJOT09FSFFKdmptVStLZUNmUitRSmpSV1JGTFVDbHYzbTkvajV6aWdRS2diT0hwd3YzWG83d1cwM3FFK1FKbGMxck4vTHJnNU9HTlNvcGxsNU53b2l3K3BVYjU1UHFGS1pDR3Nxa1pLdlY0MWxYSjNLN3owbWlMOG5nNm9iUVNXNnJvWG9Ub2htaU1YRExHNGgraWxGalh6QkYxSURmckl0L3pjLzkwM0Y4WkxEeUlja2YxUmE4WHhvWXQ0U3cyalZzYmFMaXdQZGJjUXozdVZBeGg4QnRNPTwveGVuYzpDaXBoZXJWYWx1ZT48L3hlbmM6Q2lwaGVyRGF0YT48L3hlbmM6RW5jcnlwdGVkRGF0YT48L3NhbWwyOkVuY3J5cHRlZEFzc2VydGlvbj48L3NhbWwycDpSZXNwb25zZT4=
```
### setCookie?
```
General
---
Request URL: https://rp1.tbstest.catslab.ca/RPSimulator/setCookie?clf=1&return=https%3A%2F%2Frp1.tbstest.catslab.ca%2FRPSimulator%2Fresponse-eng.jsp
Request Method: GET
Status Code: 302 Found
Remote Address: 52.232.135.10:443
Referrer Policy: no-referrer-when-downgrade
---
Response Headers
---
Content-Length: 0
Date: Wed, 18 Mar 2020 13:40:22 GMT
Location: https://rp1.tbstest.catslab.ca/RPSimulator/response-eng.jsp?_saml_idp=aHR0cHM6Ly9jcHNpbTEuY2F0c2xhYi5jYQ%253D%253D
Server: Apache-Coyote/1.1
---
Request Headers
---
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Accept-Encoding: gzip, deflate, br
Accept-Language: en-US,en;q=0.9
Cache-Control: max-age=0
Connection: keep-alive
Cookie: JSESSIONID=F0B6BE5C429142418447715E32D7094E; _saml_idp=aHR0cHM6Ly9jcHNpbTEuY2F0c2xhYi5jYQ%3D%3D
DNT: 1
Host: rp1.tbstest.catslab.ca
Referer: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/idp/profile/SAML2/Redirect/SSO?execution=e1s1&_eventId_proceed=1
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: cross-site
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.132 Safari/537.36
---
Query String Parameters
---
clf: 1
return: https://rp1.tbstest.catslab.ca/RPSimulator/response-eng.jsp
```
### response-eng.jsp_saml_idp
```
General
---
Request URL: https://rp1.tbstest.catslab.ca/RPSimulator/response-eng.jsp?_saml_idp=aHR0cHM6Ly9jcHNpbTEuY2F0c2xhYi5jYQ%253D%253D
Request Method: GET
Status Code: 200 OK
Remote Address: 52.232.135.10:443
Referrer Policy: no-referrer-when-downgrade
---
Response Headers
---
Cache-Control: private
Content-Type: text/html;charset=utf8
Date: Wed, 18 Mar 2020 13:40:22 GMT
Expires: Wed, 31 Dec 1969 19:00:00 EST
Server: Apache-Coyote/1.1
Transfer-Encoding: chunked
---
Request Headers
---
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Accept-Encoding: gzip, deflate, br
Accept-Language: en-US,en;q=0.9
Cache-Control: max-age=0
Connection: keep-alive
Cookie: JSESSIONID=F0B6BE5C429142418447715E32D7094E; _saml_idp=aHR0cHM6Ly9jcHNpbTEuY2F0c2xhYi5jYQ%3D%3D
DNT: 1
Host: rp1.tbstest.catslab.ca
Referer: https://gluuserver-cc-01.canadacentral.cloudapp.azure.com/idp/profile/SAML2/Redirect/SSO?execution=e1s1&_eventId_proceed=1
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: cross-site
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.132 Safari/537.36
---
Query String Parameters
---
_saml_idp: aHR0cHM6Ly9jcHNpbTEuY2F0c2xhYi5jYQ%3D%3D
```
### home-eng.jsp 
```
General
---
Request URL: https://rp1.tbstest.catslab.ca/RPSimulator/home-eng.jsp
Request Method: GET
Status Code: 200 OK
Remote Address: 52.232.135.10:443
Referrer Policy: no-referrer-when-downgrade
---
Response Headers
---
Cache-Control: private
Content-Type: text/html;charset=utf8
Date: Wed, 18 Mar 2020 17:54:04 GMT
Expires: Wed, 31 Dec 1969 19:00:00 EST
Server: Apache-Coyote/1.1
Transfer-Encoding: chunked
---
Request Headers
---
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Accept-Encoding: gzip, deflate, br
Accept-Language: en-US,en;q=0.9
Connection: keep-alive
Cookie: JSESSIONID=F0B6BE5C429142418447715E32D7094E; _saml_idp=aHR0cHM6Ly9jcHNpbTEuY2F0c2xhYi5jYQ%3D%3D
DNT: 1
Host: rp1.tbstest.catslab.ca
Referer: https://rp1.tbstest.catslab.ca/RPSimulator/response-eng.jsp?_saml_idp=aHR0cHM6Ly9jcHNpbTEuY2F0c2xhYi5jYQ%253D%253D
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: same-origin
Sec-Fetch-User: ?1
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.132 Safari/537.36
```
### favicon.ico
```
General
---
Request URL: https://rp1.tbstest.catslab.ca/RPSimulator/images/favicon.ico
Request Method: GET
Status Code: 200 OK (from disk cache)
Remote Address: 52.232.135.10:443
Referrer Policy: no-referrer-when-downgrade
---
Response Headers
---
Accept-Ranges: bytes
Content-Length: 1406
Content-Type: image/x-icon
Date: Wed, 18 Mar 2020 16:44:46 GMT
ETag: W/"1406-1287506602000"
Last-Modified: Tue, 19 Oct 2010 16:43:22 GMT
Server: Apache-Coyote/1.1
---
Request Headers
---
DNT: 1
Referer: https://rp1.tbstest.catslab.ca/RPSimulator/home-eng.jsp
Sec-Fetch-Dest: image
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.132 Safari/537.36
```