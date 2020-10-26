# Day 19 - Threat Modeling with DFDs, STRIDE
10/29/20

* [A Beginners Guide To The STRIDE Security Threat Model](https://www.ockam.io/learn/blog/introduction_to_STRIDE_security_model)

The STRIDE framework:
1. Spoofing
2. Tampering
3. Repudiation
4. Information Disclosure
5. Denial of Service
6. Elevation of Privilege

**Spoofing**</br>
Common authentication methods for systems and requirements to spoof a request:
* Single key: Anyone who obtains the key would have access to the systems that trust it indefinitely.
* Access token
* Signatures: to spoof a signature, the attacker would need access to the sender's private key.

**Tampering**</br>
Data may be altered to spoof access, could be caused by artificially-elevated privileges, or could cover the tracks of other vulnerabilities.

**Repudiation**</br>
You should implement auditing to catch and trace attempted security threats/breaches.

**Information Disclosure**</br>
"Any system that stores or accesses private information may accidentally disclose it."

**Denial of Service**</br>
Overloading a system with incoming requests can make it impossible for users to connect, a "denial of service" that makes a system unreachable.

**Elevation of Privilege**</br>
Elevation of privilege is related to authorization; the attacker not only claims to be a valid user, but one with an expanded/sys admin type of role.




### Additional Resources
* [Threat Modeling Security Fundamentals](https://docs.microsoft.com/en-us/learn/paths/tm-threat-modeling-fundamentals/)