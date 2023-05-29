# Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols
<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this project, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDP, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)
- Power Shell

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Active Azure Subscription
- Azure Cloud Tenant (Resource Group)
- Ports and Protocols
- Windows and Linux Virtual Machines

<h2>Actions and Observations</h2>

<p>
  
![thisismyimage](https://github.com/ELIZABETHONAS/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/blob/main/IMG_0085.jpeg?raw=true)
  
</p>
<p>
 
- Create two Virtual Machines for Windows 10 and Linux Ubuntu (this has been previously created VMONE and VMTWO)
</p>
<br />

<p>

![thisismyimage](https://github.com/ELIZABETHONAS/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/blob/main/IMG_0088.jpeg?raw=true)
</p>
<p>
 
- Observe Your Virtual Network within Network Watcher
</p>
<br />

<p>
  
![thisismyimage](https://github.com/ELIZABETHONAS/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/blob/main/Screenshot%202023-05-04%20at%209.02.05%20PM.jpeg?raw=true)
</p>
<p>
 
- Confirm network uniformity i.e vnet, nsg, for both VMs
</p>
<br />

<p>
  
![thisismyimage]()
</p>
<p>
 
- Use Remote Desktop to connect to your Windows 10 Virtual Machine
</p>
<br />

<p>
  
![thisismyimage]()
</p>
<p>
 
- If you have an apple laptop, you will be required to install "Microsoft Remote Desktop" via the app store
</p>
<br />

<p>
<img src="https://imgur.com/Dux33mi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 
- Login with VMONE Public IP address
</p>
<br />

<p>
<img src="https://imgur.com/Dux33mi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 
- Within your VMONE, Install Wireshark
</p>
<br />

<p>
<img src="https://imgur.com/93V67mo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
