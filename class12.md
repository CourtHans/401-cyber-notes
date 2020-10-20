# Day 12 - Intrusion Detection and Prevention Systems (IDS/IPS)
10/20/20

* [The Pros and Cons of Network Intrusion Detection Systems](https://blog.rapid7.com/2017/01/11/the-pros-cons-of-intrusion-detection-systems/)

> "A network intrusion detection system (NIDS) can be an integral part of an organization’s security, but they are just one aspect of many in a cohesive and safe system."

An intrusion detection system (IDS) can be likened to a fire alarm - an early warning device to protect you/your data.  However an Intrusion Protection System (IPS) is a device that can monitor your system, warn you, AND is capable of stopping threats without a system administrator getting involved.  

"An NIDS [Network Intrusion Detection System] and an HIDS [Host Intrusion Detection System] are complementary systems that differ by the position of the sensors: network-based (monitoring the ethernet or WiFi) and host-based, respectively."  Network-based sensors have a quicker response than host-based and doesn’t need to alter existing infrastructure.  They monitor everything on a network segment, regardless of the target host’s operating system. An HIDS monitors event and audit logs, comparing new entries to attack signatures. HIDS are resource intensive.

* An NIDS can detect attacks that an HIDS will miss because it looks at packet headers in real-time. 
* An HIDS will also be able to pick up some things that an NIDS will miss, such as unauthorized users making changes to the system files.

NIDS can detect in real-time (useful if an attacker is trying to erase their tracks); however, this can turn up a lot of false positives.

### Pros of Network Intrusion Detection Systems:
* **They Can Be Tuned to Specific Content in Network Packets** (a NIDS can be tuned to show you the specific content within the packets.)
* **They Can Look at Data in the Context of the Protocol** (looks at the TCP and UDP payloads) 
* **They Can Qualify and Quantify Attacks** (an IDS analyzes the amount and types of attacks). 
* **They Make It Easier to Keep Up With Regulation** (you can also use your IDS logs as part of the documentation to meet certain requirements)
* **They Can Boost Efficiency**

### Cons of Network Intrusion Detection Systems:
* **They Will Not Prevent Incidents By Themselves**
* **An Experienced Engineer Is Needed to Administer Them** (usefulness all depends on what you do with the information gathered). 
* **They Do Not Process Encrypted Packets**
* **IP Packets Can Still Be Faked** (network address can still be spoofed)
* **False Positives Are Frequent**
* **They Are Susceptible to Protocol-based Attacks** (NIDS can be crashed by protocol analyzer bugs and also invalid data)
* **The Signature Library Needs to Be Continually Updated to Detect the Latest Threats**