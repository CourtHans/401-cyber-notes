# Day 34 - PowerShell in Cybersecurity
11/19/20

* [10 essential PowerShell security scripts for Windows administrators](https://www.csoonline.com/article/3148823/10-essential-powershell-security-scripts-for-windows-administrators.html)

1. POSH-Sysmon: Configuring Sysmon
Install and configure Sysmon to better track future attacks. ysmon collects the events it generates using Windows Event Collection or SIEM agents.

2. Enable the Client Rules Forwarding Block control: Email hardening
You can use individual PowerShell commands to review if there is a forwarding set up and disable it accordingly. The command `Set-RemoteDomain [remote domain name] -AutoForwardEnabled $false` ensures that attackers can't send emails from your network without you knowing about it

3. Remove-LocalAdmins Masiv: Local administrator review
"A longstanding script you can use is the Remove-LocalAdmins Masive script, which is still a key tool to look at all the computers specified in a text file for all the users listed in another file, and then remove those users."<br>
"The Local Administrator Password (LAPS) toolkit allows you to set random local administrator passwords in a domain to ensure that pass-the-hash attacks do not occur. Then you can use the LAPS Reporting PowerShell script to audit the use of the LAPS toolkit or use a LAPSpass to retrieve a password for a single user."

4. MicroBurst: Azure PowerShell scripts
For Azure situations, "[MicroBurst](https://github.com/NetSPI/MicroBurst) is a collection of PowerShell scripts that support Azure Services discovery, weak configuration auditing, and post exploitation actions such as credential dumping."

5. SecurityPolicyDsc: Local security policies
PowerShell can be used to set local security policies with the [PowerShell script SecurityPolicyDsc](https://github.com/dsccommunity/SecurityPolicyDsc).

6. Device Guard and Credential Guard: Deploying secure systems
"Microsoft provides the Device Guard and Credential Guard [hardware readiness tool](https://www.microsoft.com/en-us/download/details.aspx?id=53337), which is a Windows PowerShell script. Run it with elevated permissions on Windows 10 (beginning with version 1607) and Windows Server 2016 and now Server 2019. The tool can check if the device can run Device Guard or Credential Guard, check for compatibility with the Hardware Lab Kit tests that are run by partners, enable and disable Device Guard or Credential Guard."

7. NTFSSecurity: File system security
NTFSSecurity enhances the options available from PowerShell (Get-Acl and Set-Acl), allowing you to get, add or remove various permissions.

8. Posh-SecMod: Network discovery
Posh-SecMod is a bundle of scripts - Discovery, Parse, PostExploitation, Registry, Utilities, Audit, Database

9. MonitorADGroupMembership: Monitoring movement
One script that can monitor changes to group membership is MonitorADGroupMembership (you can also set it up to send an email alerts).

10. BlackViperScript: Standalone workstation hardening
[BlackViperScript](https://github.com/madbomb122/BlackViperScript) "lets you set Windows 10's services based on Black Viper's service configurations, your own service configuration (if in a proper format), a backup of your service configurations made by this script, or a custom configuration using the script."

* [Varonis Blog - What is Mimikatz](https://www.varonis.com/blog/what-is-mimikatz/)

> [Mimikatz](https://github.com/gentilkiwi/mimikatz) is an open-source application that allows users to view and save authentication credentials like Kerberos tickets.

"Attackers commonly use Mimikatz to steal credentials and escalate privileges: in most cases, endpoint protection software and anti-virus systems will detect and delete it. Conversely, pentesters use Mimikatz to detect and exploit vulnerabilities in your networks so you can fix them."
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