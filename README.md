# SIEM_Honeypot_security_monitoring


<h2>Description</h2>

This project aims to set up a security monitoring system using SIEM (Security Information and Event Management) on the Azure portal.

<h3> 2. ** Setting Up the Honeypot VM **: </h3>
A virtual machine (VM) running Windows OS was created and named "Honeypot" to simulate a vulnerable system for detecting potential threats. The security protocol was set to produce null values intentionally, allowing us to gather information about attackers.
<br />

<h3> 2. ** Collecting Failed RDP Logs **: </h3>
To start, the firewall on the VM was taken down to attract potential malicious activity. Remote Desktop Protocol (RDP) was used to access the VM and monitor any unauthorized 
access attempts. IP geolocation services were leveraged to collect information about the IP addresses involved in failed RDP attempts.
Using PowerShell, a code snippet was written to collect the failed RDP logs from the VM. These logs were also extracted from the Windows Event Viewer for thorough analysis.

<h3> 2. ** Configuring Analytic Workspace **: </h3>  
Creation and configuration of the analytic workspace to store and analyze the collected logs.


<h3> 2. ** Creating Custom Logs **: </h3>
A custom log was generated using the sample data retrieved from the failed RDP logs. Custom columns were created within this log to store information such as longitude, latitude, country, source host, and label.

<h3> 2. ** Running Azure Sentinel Queries **: </h3>
The collected data was then used to run Azure Sentinel queries, enabling us to identify patterns and potential threats. 

<h3> 2. ** Plotting Geographic Distribution **: </h3>
The output data was plotted on a map, providing visual representation of the attempted attacks and their sources.


<h2>Environments Used </h2>

- <b> Azure Portal </b> 
- <b> Azure Virtual Machine </b> 
-  <b> Azure Analytic Workkspace </b> 
-  <b> Azure Sentinal  </b> 
-  <b> Microsoft Remote Desktop </b> 
-  <b> Windows PowerShell </b> 

<h2> Lab walk-through:</h2>

<p align="center">
 </b>1. Azure Portal - VM Creation (Windows): <br/>
<img src="https://imgur.com/uJcYxeB"height="80%" width="80%" alt=" Virtual Machine"/>
<br />
<br />
<p align="center">
 </b> Capturing Dynamic IP Address Assignments: <br/>
<img src="https://i.imgur.com/OksBAHb.png?1 " height="80%" width="80%" alt="hospitality Network"/>
<br />
<br />
<p align="center">
</b> Analyzing Network Configuration and Connectivity <br/>
<img src="https://i.imgur.com/eS2pawF.png " height="80%" width="80%" alt="hospitality Network"/>
<br />
<br />
<p align="center">
</b> Displaying Interface IP Addresses and Status <br/>
<img src="https://i.imgur.com/x0Ai9t1.png " height="80%" width="80%" alt="hospitality Network"/>
<br />
<br />

<p align="center">
</b> Displaying VLAN Settings and Assignment <br/>
<img src="https://i.imgur.com/0mBzyoO.png " height="80%" width="80%" alt="hospitality Network"/>
<br />
<br />


<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
