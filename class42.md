# Day 42 - Scanning and Enumeration with NMAP
12/2/20

* [What is Mimikatz?](https://www.varonis.com/blog/what-is-mimikatz/)

> “Mimikatz has done more to advance security than than any other tool I can think of.”  -- Jake Williams, Rendition Infosec

"**Mimikatz is an open-source application that allows users to view and save authentication credentials like Kerberos tickets.**" 

Attackers can use Mimikatz to steal credentials and session cookies to mimic legitimate users and escalate privilege. 

Examples:

* Pass-the-Hash
* Pass-the-Ticket
* Over-Pass the Hash (Pass the Key)
* Kerberos Golden Ticket
* Kerberos Silver Ticket
* Pass-the-Cache

Mimikatz needs to be “Run as Admin” to function completely, even if you are using an Administrator account.

*Extracting clear text passwords from memory*
```
mimikatz # privilege::debug
mimikatz # log nameoflog.log
mimikatz # sekurlsa::logonpasswords
```

The `coffee` command returns ascii art of coffee. Cause everyone needs coffee.