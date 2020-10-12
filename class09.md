# Day 9 - Public Key Infrastructure
10/15/20

* [What is Public Key Infrastructure (PKI)](https://www.ssh.com/pki/)
* [Prof Messer Security+ PKI Components](https://www.youtube.com/watch?v=3yuad7_bszE)

> "Public Key Infrastructure (PKI) is a technology for authenticating users and devices in the digital world. The basic idea is to have one or more trusted parties digitally sign documents certifying that a particular cryptographic key belongs to a particular user or device. The key can then be used as an identity for the user in digital networks."

A public key infrastructure relies on digital signature technology, which uses public key cryptography. The most familiar use of PKI is in SSL certificates.

**Public Key Infrastructure** (or **PKI**) is a way to describe the policies, procedures, hardware, software, and people to manage digital certificates (creating, distributing, managing, storing, and revoking).

It also refers to the binding of public keys to people or devices.

Key generation</br>
Decide on the strength (# of bits) and which ciper to use. </br>
Then generate a certificate to allocate to a user</br>
Distribute it (make available to user)</br>
Storage</br>
Revoke (if compromised) or update upon expiration

Digital certificates help convey the authenticity of a key.

Different items listed w/ a digital certificate:
* Version
* Serial Number
* Signature Algorithm
* Issuer
* Valid from/valid to
* Subject
* Public Key
* Extensions

There are commercial certificate authorities (you would purchase a cert for your web site). It starts with the creation of a key pair (a public key and a private key). A CSR (certificate signing request) is sent and, if everything checks out, you'll get it sent back. 

However, you can also build them in house (private certificate authorities).

PKI trust relationships:
- Everyone receives their certificates from one authority
- Hierarchical (single CA issues certs, distributes cert management load)

**OCSP** - Online Certificate Status Protocol
The browser can check certificate revocation (not all browsers support this)
