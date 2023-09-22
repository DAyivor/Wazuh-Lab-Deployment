<h1>Wazuh Lab Deployment</h1>

 ### [YouTube Demonstration](https://www.youtube.com/watch?v=3CaG2GI1kn0&t=0s)

<h2>Description</h2>
Project consists of creating and deploying a cloud server, setting up containers, and deploying agents to virtual machines to practice threat detection/incident response. Wazuh is an open-source Security Information and Event Management system for aggregating and analyzing telemetry in real time for threat detection and compliance. 
<br />


<h2>Languages and Software Used</h2>

- <b>Bash</b> 
- <b>Terminal</b>
- <b>Docker</b>
- <b>Wazuh</b>
- <b>VirtualBox</b>

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)
- <b>Windows 11</b> (22H2)
- <b>MacOS</b> (12.6.1 Monterey)
- <b>Kali Linux</b> (2023.3 - Debian)
- <b>Ubunto</b> (20.04.6)
  
<h2>Program walk-through:</h2>

<p align="center">
Deploy a Linux server w/Wazuh installed through the Linode Marketplace: <br/>
<img src="https://i.imgur.com/ULuqA1K.png" height="60%" width="60%" alt="Wazuh Lab Deployment"/>
<img src="https://i.imgur.com/8UbG99O.png" height="50%" width="50%" alt="Wazuh Lab Deployment"/> 
<img src="https://i.imgur.com/7Bk6LMY.png" height="80%" width="80%" alt="Wazuh Lab Deployment"/>
<img src="https://i.imgur.com/9tKYs5A.png" height="80%" width="80%" alt="Wazuh Lab Deployment"/>
<br />
<br />
Deploy a Linux server through the Linode Marketplace for Docker: <br/>
<img src="https://i.imgur.com/K0deecb.png" height="80%" width="80%" alt="Wazuh Lab Deployment"/>
<br />
<br />
Install Docker (Command - sudo apt install docker.io docker-compose -y):  <br/>
<img src="https://i.imgur.com/2cveuWx.png" height="60%" width="60%" alt="Wazuh Lab Deployment"/>
<br />
<br />
After Docker install is complete, execute command to deploy Wazuh as a single-node stack w/ self-signed certificates: <br/>
(Command - docker-compose -f generate-indexer-certs.yml run --rm generator) <br/>
<img src="https://i.imgur.com/d3QXwlR.png" height="60%" width="60%" alt="Wazuh Lab Deployment"/>
<br />
<br />
Install Wazuh images/applications on the signle-node stack (Command - docker-compose up -d):  <br/>
(May take some time) <br/>
<img src="https://i.imgur.com/R9Sqv1E.png" height="60%" width="60%" alt="Wazuh Lab Deployment"/>
<img src="https://i.imgur.com/Vttgnr3.png" height="60%" width="60%" alt="Wazuh Lab Deployment"/> <br/>
(Command - docker stats to confirm) <br/>
<img src="https://i.imgur.com/aI7TH2J.png" height="60%" width="60%" alt="Wazuh Lab Deployment"/>
<br />
<br />
Once Wazuh is installed, access the Wazuh dashboard through the RDNS address:  <br/>
<img src="https://i.imgur.com/OdUbZsc.png" height="80%" width="80%" alt="Wazuh Lab Deployment"/> <br/>
Select "Add agent" to begin deploying agent to virtual machines <br/>
<img src="https://i.imgur.com/xguNNa3.png" height="125%" width="125%" alt="Wazuh Lab Deployment"/>
<br />
<br />
Select "Deploy New Agent" within the Agent dashboard:  <br/>
<img src="https://i.imgur.com/EAO6Hvr.png" height="80%" width="80%" alt="Wazuh Lab Deployment"/>
<br />
<br />
Select the appropriate options to configure the agent for the virtual machine: <br/>
<img src="https://i.imgur.com/ydZmT6s.png" height="70%" width="70%" alt="Wazuh Lab Deployment"/>
<br />
<br />
The selections will create a command you can enter within the virtual machine to install the agent: <br/>
<img src="https://i.imgur.com/uz8Rcpr.png" height="70%" width="70%" alt="Wazuh Lab Deployment"/>
<br />
<br />
Connect to the virtual machine and enter the command to connect the Wazuh agent: <br/>
<img src="https://i.imgur.com/It87A2D.png" height="80%" width="80%" alt="Wazuh Lab Deployment"/>
<img src="https://i.imgur.com/vALooFR.png" height="80%" width="80%" alt="Wazuh Lab Deployment"/>
<img src="https://i.imgur.com/nq3Un1L.png" height="80%" width="80%" alt="Wazuh Lab Deployment"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
