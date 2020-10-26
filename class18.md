# Day 18 - Web Application Threat Modeling with OWASP, DREAD
10/28/20

* [OWASP guide to Application Threat Modeling](https://owasp.org/www-community/Application_Threat_Modeling)
* [NIST SP800-154 Guide to Data-Centric Threat Modeling](https://csrc.nist.gov/publications/detail/sp/800-154/draft#pubs-abstract-header)

> "Threat modelling works to identify, communicate, and understand threats and mitigations within the context of protecting something of value."

Most of the time, a threat model includes:
**What**</br>
* A description / design / model of what you’re worried about
* A list of assumptions that can be checked or challenged in the future as the threat landscape changes
* A list of potential threats to the system
* A list of actions to be taken for each threat
* A way of validating the model and threats, and verification of success of actions taken

"***Threat modelling: the sooner the better, but never too late.***"

**Why**</br>
* Build a secure design
* Efficient investment of resources
* Bring Security and Development together to collaborate
* Identify threats/compliance requirements, evaluate their risk
* Define and build required controls
* Balance risks, controls, and usability
* Identify where building a control is unnecessary, based on acceptable risk
* Document threats and mitigation
* Ensure business requirements (or goals) are adequately protected in the face of a malicious actor, accidents, or other causes of impact
* Identification of security test cases / security test scenarios to test the security requirements

**The 4 Questions to ask:**
1. What are we building?
2. What can go wrong?
3. What are we going to do about that?
4. Did we do a good enough job?

"When the answer is that the system’s architecture isn’t changing, no new processes or dataflows are being introduced, and there are no changes to the data structures being transmitted, then it is unlikely that the answers to ‘what can go wrong’ will change. When one or more of those changes, then it’s useful to examine what can go wrong as part of the current work package, and to understand designs trade-offs you can make, and to understand what you’re going to address in this sprint and in the next one."

