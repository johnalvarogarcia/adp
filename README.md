<h1>Implementing Honeypot in Azure VM and logging with Sentinel by Country</h1>


<h2>Description</h2>
The PowerShell script in this repository is responsible for parsing out Windows Event Log information for failed RDP attacks and using a third party API to collect geographic information about the attackers location.

The script is used in this demo where I setup Azure Sentinel (SIEM) and connect it to a live virtual machine acting as a honey pot. We will observe live attacks (RDP Brute Force) from all around the world. I will use a custom PowerShell script to look up the attackers Geolocation information and plot it on an Azure Sentinel Map!

For this project we:
<ul>
  <li>Create a windows 10 Virtual Machine in Azure.</li>
  <li>Set firewall rules to allow for open traffic.</li>
  <li>Implement our PowerShell script, utiliziing ipgeolocation.io's free API.</li>
  <li>Setup Log Analytics Workspace to ingest logs and geographic information using our PowerShell script.</li>
  <li>Implement Sentinel and connect our Log Analytics Workspace.</li>
  <li>Create custom log in Sentinel.</li>
  <li>Create a workbook in Sentinel to vizualize Remote Desktop login attempts plotted on a map.</li>
</ul>
<br />


<h2>Platforms and Technologies Used</h2>

- <b>Azure</b> 
- <b>Sentinel</b>
- <b>PowerShell</b>

<h2>Utilities Used </h2>

- <b>ipgeolocation.io: IP Address to Geolocation API</b>

<h2>Program walk-through:</h2>

<p align="center">
Log by Geolocation after 24 Hours: <br/>
<img src="https://i.imgur.com/m3VBSjC.png" height="80%" width="80%"/>
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
