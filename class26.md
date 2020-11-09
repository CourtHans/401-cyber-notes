# Day 26 - Setting up Splunk SIEM
11/9/20

* [Is Cybersecurity Automation the Future?](https://www.forbes.com/sites/forbestechcouncil/2019/08/20/is-cybersecurity-automation-the-future/#4cd22ea4589c)
* [Automated Incident Response Explained](https://cybersecurity.att.com/blogs/security-essentials/automated-incident-response-in-action-7-killer-use-cases)

> "Automation ... increases the complexity of an organization’s information systems, and as malicious attackers expand their targets, cybersecurity programs must be ready to implement automated cybersecurity solutions."

SOAR - security automation and orchestration</br>
RPA - robotic process automation

Both approaches can "interact with an enterprise’s instrumentation to gather intelligence, perform analysis and either take-automated action or prompt a team member to take further action." Organizational complexity can be risky if it's not matched with appropriate cybersecurity measures. Automation can make a security team more efficient, help augment a lean workforce, and stave off the potential for human error. Automating the routine tasks can leave bandwidth open for more complex tasks.

**Engineering and Architecture**</br>
**Remediation Activities**</br>
**Automation Development and Engineering**</br>

The author argues: "In the future, the cybersecurity program may become a developer shop where automation capabilities will be created and advanced using multiple automation techniques." But you first need to specifically detail each step of a process you want to automate.

Three basic approaches:
1. Embed development capabilities in your cybersecurity team. 
2. Partner cybersecurity with organizational development teams.
3. Adopt a hybrid approach. Utilize an internal team for tactical development work and organizational development capabilities for complex integration tasks.

Examples of how automation can help:

With automated incident response, you can automatically update your firewall to block malicious IPs as they are detected.

With orchestration and automation tools, you can automate actions like fetching additional forensics data, disabling networking on an infected system, running automated vulnerability scans to identify other at-risk systems, and isolating those as well until you have a chance to patch or otherwise address them.

Having a solution with log management capabilities would allow you to search for relevant alarms and events instead of combing through them manually. 

With automation capabilities, you can move immediately from detection to response by blocking a domain automatically when your intrusion detection system detects the threat.

For example, if evidence of ransomware appears on a particular server, automation enables you to set up a rule to automatically disable networking to contain the intrusion and protect your data, whether or not you’re awake to trigger the action. 

Automation allows for essential capabilities like asset discovery, vulnerability scanning, intrusion detection, behavioral monitoring, SIEM, and log management. From the same pane of glass, you can manage IR activities within the other technologies you use, including Cisco Umbrella, Palo Alto Networks next-generation firewalls, ServiceNow, Carbon Black, and more.