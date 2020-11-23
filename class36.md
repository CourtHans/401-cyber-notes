# Day 36 - Scanning the OWASP BWA
11/23/20

* [Cross-site scripting](https://portswigger.net/web-security/cross-site-scripting)

***What IS cross-site scripting?(XSS)***</br>
"Cross-site scripting (also known as XSS) is a web security vulnerability that allows an attacker to compromise the interactions that users have with a vulnerable application. It allows an attacker to circumvent the same origin policy, which is designed to segregate different websites from each other. Cross-site scripting vulnerabilities normally allow an attacker to masquerade as a victim user, to carry out any actions that the user is able to perform, and to access any of the user's data. If the victim user has privileged access within the application, then the attacker might be able to gain full control over all of the application's functionality and data."

3 types of XSS attacks
* Reflected XSS
* Stored XSS
* DOM-based XSS

**Reflected XSS** is the simplest. An attacker can insert code into an HTTP request which can be executed in the user's browser.

"**Stored XSS** (also known as persistent or second-order XSS) arises when an application receives data from an untrusted source and includes that data within its later HTTP responses in an unsafe way."

"**DOM-based XSS** arises when an application contains some client-side JavaScript that processes data from an untrusted source in an unsafe way, usually by writing the data back to the DOM."

Burp Suite's web vulnerability scanner can find a lot of these, saving a lot of time. 

"Content security policy (CSP) is a browser mechanism that aims to mitigate the impact of cross-site scripting and some other vulnerabilities."</br>
"Dangling markup injection is a technique that can be used to capture data cross-domain in situations where a full cross-site scripting exploit is not possible, due to input filters or other defenses."

Some ways to prevent XSS attacks:
* Filter input on arrival
* Encode data on output
* Use appropriate response headers
* Content Security Policy

### Additional Resources
* [Security Report for In-Production Web Applications](https://www.rapid7.com/globalassets/_pdfs/whitepaperguide/rapid7-tcell-application-security-report.pdf)