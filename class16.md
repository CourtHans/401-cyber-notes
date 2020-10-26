# Day 16 - Threat Analysis, Cyber Kill-Chain, and Stuxnet
10/26/20

* [Breaking the Kill-Chain: A Defensive Approach](https://thecisoperspective.com/index.php/2020/03/27/breaking-the-kill-chain-a-defensive-approach/)
* [Breaking the Kill-Chain: A Defensive Approach](https://www.youtube.com/watch?v=II91fiUax2g)

> "The kill chain is more then just a model for how an attack executed, it’s also a blueprint for building a good cybersecurity program."

"First developed by Lockheed Martin, the **Cybersecurity Kill Chain** is a model for describing the steps an attacker must complete to carry a successful attack. This model is made up of 7 sequential steps, including:

1. Reconnaissance
2. Weaponization
3. Delivery
4. Exploitation
5. Installation
6. Command and Control
7. Actions on Objectives"

***Reconnaissance***</br>
*The entire goal of the reconnaissance phase is to find a weakness that can be exploited.*
Guarding against passive reconnaissance relies upon employee education for social media, guarding against the level of detail made public (through job postings, etc.), removing specific information about errors from public servers.</br>
Guarding against active reconnaissance takes a bit more finesse; and involves a knowledgeable *hardening* of your system (like ensuring that unused ports and services are disabled).

> "Honeypots are great tools that can be used as a decoy against a would be attacker."

***Weaponization***</br>
Commonly used tools:
* Metasploit or exploit-db
* The Veil framework
* Social Engineering Toolkit

Patch Management continues to be one of the best defensive measures, as is disabling Office macros, javascript and browser plugins.

Technical controls
* Endpoint and network edge malware protection
* An IPS that specifically tuned to look for exploit attempts
* URL and domain filtering to prevent access to known malware channels 
* Email security that includes AV and AntiSpam

***Delivery***</br>
Examples of delivery channels: </br>
* Websites (malicious or clean)
* Social media
* User input
* Email
* USB

"*The single best security measure against the delivery of the attack is user awareness.*" "Remember that SSL accounts for >70% of web and email traffic today, so if you’re not doing SSL inspection in all your delivery channels – you may be completly blind to what’s passing through that encrypted tunnel."

Other effective measures:
Some other effective measures include: 
* Webfiltering
* Disabling USB and not giving any user “admin” rights
* DNS Filtering

***Exploitation***</br>
"Protective measures are limited once an attacker has been able to execute the exploit but they do exist: </br>
* DEP (Data Execution Prevention) is a software and hardware feature which attempts to prevent the execution of code in memory where it doesn’t belong.  
* Anti-Exploit is a feature on some AV solutions that monitor known applications for unusual calls to memory.</br>
Both of these techniques act as the last line of defense against common exploit attempts"

***Installation**</br>
Common payloads and techniques during this stage involve:</br>
* DLL hijacking
* Injecting Meterpreter or other similar payloads
* Installing Remote Access Tools (or RAT)
* Registry changes to make my program automatically start up
* Executing Powershell in fileless attacks

***Command and Control***</br>
" If you have the ability to do micro segmentation through a “Zero trust security” model...this would essentially leave the infected user completely isolated on that port until they can verify their machine is clean and have been authenticated."

"Make sure that you are using Layer-7 application control to block commonly known remote access tools like telnet, ssh, powershell, RDP and various other protocols that really have no business leaving your network." "For detection, IoCs or Indicators of Compromise are an excellent post detection tool. An IoC, is an observed behavior by a user or server that are indicative of a breach. IoC’s can be observed and collected on the endpoint,  or it could be detected by a SIEM with an IoC feed."

***Actions on Objectives***</br>
Moving laterally is a common step for an attacker to take once they gained access to your system, so it's critical to design your network with this in mind, giving least access and privilege.  

***Dwell Time***</br>
"Dwell time is the length of time an attacker is active inside the network before being detected. For CISOs or Security Directors, this is a critical metric to follow. According to a report by Ponemom Institute and IBM, the average dwell time is 191 days."

As with any chain, it only takes one link to break the chain...