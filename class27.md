# Day 27 - Adding Data Sources with Splunk SIEM
11/10/20

* [Getting data into Splunk from Windows endpoints](https://lantern.splunk.com/hc/en-us/articles/360043721173-Getting-data-into-Splunk-from-Windows-endpoints)

"The most efficient way to gather data from any Windows server is to install universal forwarders on the hosts that you want to gather data. Universal forwarders use limited resources. In some cases, such as Registry monitoring, you must use a forwarder, because you cannot collect Registry data over WMI." 

"WMI rarely works with Splunk apps and solutions, including Splunk premium apps. Lastly, from a security perspective, WMI utilizes a method of access which is considered insecure with well understood exploitation means. **For these reasons and more, it is considered a best practice to use a Splunk forwarder installed on remote hosts and avoid WMI for Splunk data collection.**"

