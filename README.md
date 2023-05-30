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
  
![thisismyimage](https://github.com/ELIZABETHONAS/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/blob/main/IMG_0091.png?raw=true)
</p>
<p>
 
- Use Remote Desktop to connect to your Windows 10 Virtual Machine
</p>
<br />

<p>
  
![thisismyimage](https://github.com/ELIZABETHONAS/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/blob/main/IMG_0089.jpeg?raw=true)
</p>
<p>
 
- If you have an apple laptop, you will be required to install "Microsoft Remote Desktop" via the app store
</p>
<br />

<p>
  
![thisismyimage](https://github.com/ELIZABETHONAS/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/blob/main/IMG_0090.jpeg?raw=true)
</p>
<p>
 
- Login with VMONE Public IP address
</p>
<br />

<p>

![thisismyimage](https://github.com/ELIZABETHONAS/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/blob/main/IMG_0093.jpeg?raw=true)
![thisismyimage](https://github.com/ELIZABETHONAS/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/blob/main/IMG_0094.jpeg?raw=true)
</p>
<p>
 
- Within your VMONE, Install Wireshark
</p>
<br />

<p>

![thisismyimage](https://github.com/ELIZABETHONAS/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/blob/main/IMG_0096.jpeg?raw=true)
</p>
<p>
  
- Open Wireshark and filter for ICMP traffic only
</p>
<br />

<p>

![thisismyimage](https://github.com/ELIZABETHONAS/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/blob/main/IMG_0099.png?raw=true)
</p>
<p>
  
- Open Power Shell or command line
</p>
<br />

<p>
  
![thisismyimage](https://github.com/ELIZABETHONAS/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/blob/main/IMG_0101.jpeg?raw=true)
</p>
<p>
 
- Retrieve the private IP address of the VMTWO and attempt to ping it from within VMONE
</p>
<br />

<p> 
  
![thisismyimage](https://github.com/ELIZABETHONAS/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/blob/main/IMG_0104.jpeg?raw=true) 
</p>
<p>
  
- Observe ping requests and replies within WireShark
</p>
<br />

<p>

![thisismyimage](https://github.com/ELIZABETHONAS/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/blob/main/IMG_0102.jpeg?raw=true)
</p>
<p>
 
- From The Windows 10 VM/ VMONE, through the command line or PowerShell and attempt to ping a public website (such as www.google.com) and observe the traffic in WireShark
</p>
<br />

<p>
  
![thisismyimage](https://github.com/ELIZABETHONAS/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/blob/main/IMG_0108.jpeg?raw=true)
![thisismyimage](https://github.com/ELIZABETHONAS/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/blob/main/IMG_0107.jpeg?raw=true)
</p>
<p>
 
- Initiate a perpetual/non-stop ping from your VMONE to your Ubuntu VM
  - Open the Network Security Group on VMTWO and disable incoming (inbound) ICMP traffic
</p>
<br />
    
<p>

![thisismyimage](https://github.com/ELIZABETHONAS/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/blob/main/IMG_0109.jpeg?raw=true)
![thisismyimage](https://github.com/ELIZABETHONAS/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/blob/main/IMG_0111.jpeg?raw=true)
</p>
<p>

- Back in VMONE, observe the ICMP traffic in WireShark and the command line Ping activity
</p>
<br />

<p>
  
![thisismyimage](https://github.com/ELIZABETHONAS/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/blob/main/IMG_0112.jpeg?raw=true)
![thisismyimage](https://github.com/ELIZABETHONAS/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/blob/main/IMG_0113.jpeg?raw=true)
</p>
<p>
 
- Re-enable ICMP traffic for the Network Security Group VMTWO is using
  - Back in VMONE, observe the ICMP traffic in WireShark and the command line Ping activity (should start working)
  - Stop the ping activity
</p>
<br />

<p>

![thisismyimage](https://github.com/ELIZABETHONAS/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/blob/main/IMG_0114.jpeg?raw=true)
![thisismyimage](https://github.com/ELIZABETHONAS/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/blob/main/IMG_0115.jpeg?raw=true)
</p>
<p>

- (Observe SSH Traffic)
  - Back in Wireshark, filter for SSH traffic only
  - From VMONE, “SSH into” your VMTWO (via its private IP address)
  - Type commands (username, pwd, etc) into the linux SSH connection and observe SSH traffic spam in WireShark
  - Exit the SSH connection by typing ‘exit’ and pressing [Enter]
</p>
<br />

<p>
![thisismyimage](https://github.com/ELIZABETHONAS/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/blob/main/IMG_0117.jpeg?raw=true)
![thisismyimage](https://github.com/ELIZABETHONAS/Network-Security-Groups-NSGs-and-Inspecting-Network-Protocols/blob/main/IMG_0118.jpeg?raw=true)
</p>
<p>
 
- (Observe DHCP Traffic)
 - Back in Wireshark, filter for DHCP traffic only
 - From VMONE, attempt to issue your VM a new IP address from the command line (ipconfig /renew)
 - Observe the DHCP traffic appearing in WireShark
</p>
<br />
