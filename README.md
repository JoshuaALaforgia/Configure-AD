# Configure-AD
<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Step 1: Create Virtual Machines
- Step 2: Set Domian Controller IP to Static
- Step 3: Ensure Connectivity between the client and Domain Controller
- Step 4: Login to Client-1 with Remote Desktop and ping DC-1’s private IP address with ping -t <ip address> (perpetual ping)
- Step 5: Login to the Domain Controller and enable ICMPv4 in on the local windows Firewall
- Step 6: Check back at Client-1 to see the ping succeed
- Step 7: Install Active Directory
- Step 8: Login to DC-1 and install Active Directory Domain Services
- Step 9: Promote as a DC: Setup a new forest as mydomain.com (can be anything, just remember what it is)
- Step 10: Restart and then log back into DC-1 as user: mydomain.com\labuser  
  
  
<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/gi0cLbk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
This is a representation of the network environment we are abou to create.
</p>
<br />

<p>
<img src="https://i.imgur.com/mjQSQNS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/m9JfKjf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
First Step is to create of virtual machines in Azure.
</p>
<br />

<p>
<img src="https://i.imgur.com/ROFpMzh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/8VCOgpf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/7SDw0Je.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
Set Domain Controllers NIC Private IP Address to be static
</p>
<br />

<p>
<img src="https://i.imgur.com/T8Q0acc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open Command prompt after Remote Desktop in client-1. ping -t 10.3.0.4
</p>
<br />

<p>
<img src="https://i.imgur.com/y57uhhW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Remote Desktop into DC-1 with the public IP Address and open wf.msc
</p>
<br />

<p>
<img src="https://i.imgur.com/Hc6ytMg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<img src="https://i.imgur.com/ffbTDqj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>  
<p>
Enable all ICMPv4 Traffic, and Ping will begin to get a reply.
</p>
<br />
  
<p>
<img src="https://i.imgur.com/C15c9pL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Enable Active Domain Services
</p>
<br />
<p>
<img src="https://i.imgur.com/wkImWEd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
New Forest, then name your Domain Name
</p>
<br />

<p>
<img src="https://i.imgur.com/Uvyb8wh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Promote as a DC
</p>
<br />
  
<p>
<img src="https://i.imgur.com/FdB6z8T.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Restart system and log back in as labuser 
</p>
<br />
