# Day 33 - Malware Analysis
11/18/20

* [Building a malware analysis Lab: How to become a malware analysis hunter](https://cybersecurity.att.com/blogs/security-essentials/building-a-home-lab-to-become-a-malware-hunter-a-beginners-guide)

"The list of tactics used [by cybercriminals] is seemingly endless and can include obfuscation, packers, executing from memory with no file drop, and P2P botnet architecture with frontline command and control servers (C2s) and gateways being compromised websites. Add to these tactics the concerns about Domain Generations Algorithms (DGA), Fast Flux and Dynamic DNS, and you complicate the mix even further."

**What should be in your Malware Analysis Lab?**
* Windows 7 Virtual Machine (home network)
* Windows 10 Virtual Machine (home network)
* Ubuntu 15.10 Virtual Machine (home network)
* Ubuntu 14.04 SSH Honeypot (VPS)
* Windows Server 2012 R2 (VPS)
* Security Onion on an empty server which I’m still configuring
* Various email spam traps for collecting macro malware & other specimens (such as phishing attempts or malware which may be hosted on a link in an email).

**Malware Hunter Toolset**
Wireshark - Incredibly powerful packet analysis tool
* PeStudio - A great tool for analyzing Portable Executable (PE) files. 
* RegShot / TotalCommander - RegShot is a tool for taking snapshots of the machine's registry allowing you to compare before/after infection
* ProcessExplorer –  a “Task Manager on Steroids” and includes a lot of great features (including color coding of processes)
* ProcessMonitor - allows you to track I/O operations on the machine and view what's happening to your registry, file system, processes
* Fakenet / ApateDNS - these tools allow you to essentially “blackhole” your outbound traffic to an address that you specify (127.0.0.1 maybe? You can then run a malware specimen and capture all DNS requests (and more with Fakenet), in order to identify C2s ready for reporting.
* Hexinator – an incredibly powerful Hex editor
* Resource Hacker – Resource hacker allows you to feed in a file (an executable for example) and it will then break that file down into the resources that make up the file.

Checklist before investigating a malware specimen further
* Filename
* File creation date
* Compile date
* File size (useful for comparison to other samples later on)
* File appearance (Anything suspicious? .exe with a Word icon?)
* Hash of the file

Suggested reading:
* Just starting out with malware analysis? - *Practical Malware Analysis*
* Deep DFIR/Malware forensics - *Malware Forensics Field Guide for (Windows/Linux) Systems*
* Advanced malware analysis/heavy RE - *Malware Analysts Cookbook & DVD*

### Additional Resources
* [Malware Analysis Bootcamp - Introduction to Malware Analysis](https://www.youtube.com/watch?v=BjRMbe0-kLI)