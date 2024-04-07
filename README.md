# Azure Detection Lab
<h2>Description</h2>
- <b>Configure and Deploy Azure Resources such as Log Analytics Workspace, Virtual Machines, and Azure Sentinel
<br />
- <b>Implement Network and Virtual Machine Security Best Practices
<br />
- <b>Utilize Data Connectors to bring data into Sentinel for Analysis
<br />
- <b>Understand Windows Security Event logs
<br />
- <b>Configure Windows Security Policies
<br />
- <b>Utilize KQL to query Logs
<br />
- <b>Write Custom Analytic Rules to detect Microsoft Security Events
<br />
- <b>Utilize MITRE ATT&CK to map adversary tactics, techniques, detection and mitigation procedures
<h2>Environments Used </h2>

- <b>Azure Sentinel</b>
- <b>Remote Desktop</b>
- <b>Task Manager</b>
- <b>Task Scheduler</b>
- <b>Local Security Policy</b>

<h2>Configuration walk-through:</h2>

<p align="center">
<h2>Setting up the Detection Lab</h2>
<br />
<br />
Create Resource Group:  <br/>
<img src="https://imgur.com/wv0qKVb.png" height="80%" width="80%" alt="Steps"/>
<br />
<br />
Deploy Virtual Machine: <br/>
<img src="https://imgur.com/b0oxEVe.png" height="80%" width="80%" alt=" Steps"/>
<br />
<br />
Enable Just in Time permissions:  <br/>
<img src="https://imgur.com/i19iuIC.png" height="80%" width="80%" alt="Steps"/>
<br />
<br />
Deploy Log Analytics: <br/>
<img src="https://imgur.com/PcJweCN.png" height="80%" width="80%" alt="Steps"/>
<br />
<br />
Add Microsoft Sentinal :  <br/>
<img src="https://imgur.com/c7Xh1mG.png" height="80%" width="80%" alt="Steps"/>
<br />
<br />
<h2>Generating Log Events</h2>
<br />
<br />
Adding Data collection rule:  <br/>
<img src="https://imgur.com/EAQ7Kgd.png" height="80%" width="80%" alt="Steps"/>
<br />
<br />
RDP into the VM and check security logs:  <br/>
<img src="https://imgur.com/zS4cLJ9.png" height="80%" width="80%" alt="Steps"/>
<br />
<br />
Use KQL query to display logs of an eventID of 4624(login attempts) : <br/>
<img src="https://imgur.com/zqC655J.png" height="80%" width="80%" alt=" Steps"/>
<br />
<br />
<h2>Task scheduler and Persistence attacks</h2>

Enable object access events as Windows doesnt display these events automatically:  <br/>
<img src="https://imgur.com/LJ9oBdQ.png" height="80%" width="80%" alt="Steps"/>
<br />
<br />
Add Parse command in order to extract only the information I need: <br/>
<img src="https://imgur.com/xDybWOk.png" height="80%" width="80%" alt="Steps"/>
<br />
<br />
Analytics rule creation :  <br/>
<img src="https://imgur.com/X47s7gn.png" height="80%" width="80%" alt="Steps"/>
<br />
<br />
Entity Mapping Settings:  <br/>
<img src="https://imgur.com/qP0sAxK.png" height="80%" width="80%" alt="Steps"/>
<br />
<br />
Configure a Time Scheduler task : <br/>
<img src="https://imgur.com/Kwk4SED.png" height="80%" width="80%" alt="Steps"/>
<br />
<br />
Incident showing up in the Sentinel which displays the tactic as persistence:  <br/>
<img src="https://imgur.com/j3ffnMf.png" height="80%" width="80%" alt="Steps"/>
<br />
<br />
<h2>Mitre Framework</h2>
The observed MITRE ATT&CK tactic used in this lab is TA0003 Persistence which essentially allows a malicious actor to maintain a foothold in an environment. :  <br/>
<img src="https://imgur.com/fqz93KT.png" height="80%" width="80%" alt="Steps"/>
<img src="https://imgur.com/fDri8gz.png" height="80%" width="80%" alt="Steps"/>
<img src="https://imgur.com/xvcEzne.png" height="80%" width="80%" alt="Steps"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
