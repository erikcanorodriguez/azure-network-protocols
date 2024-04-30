<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Create a Resource Group with a Linux and a Microsoft Windows VM on Azure
- Within your Windows 10 Virtual Machine, Install Wireshark
- Open the Network Security Group your Ubuntu VM is using and disable incoming (inbound) ICMP traffic
- Observe different responses from SSh,ICMP, and DHCP traffic on wireshark

<h2>Actions and Observations</h2>

<p>
<img src="https://github.com/erikcanorodriguez/azure-network-protocols/assets/168192619/48c73ea8-b8bb-46ca-b6eb-dc097fa3c6d5" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Firstly, we must initiate a perpetual/non-stop ping from our Windows 10 VM to our Ubuntu VM. We then head over to our main computer and go on Azure.com. From here we Open the Network Security Group your Ubuntu VM is using and disable incoming (inbound) ICMP traffic and observe the results.

</p>
<br />

<p>
<img src="https://github.com/erikcanorodriguez/azure-network-protocols/assets/168192619/71772d4c-d52a-4f2c-be79-bd60b17c4a37" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Within our Windows 10 VM we had previously set a continuous ping from our Windows 10 VM to our Linux VM. We added the NSG rule to block any incoming ICMP traffic, notice how at first there was connectivity between the two but once the rule was set in motion no response was given.
</p>
<br />

<p>
<img src="https://github.com/erikcanorodriguez/azure-network-protocols/assets/168192619/748db5ad-3bec-40d1-ae24-59cc43fe7af3" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
From here we can play around and notice the different responses we get from the different protocols (ICMP,SSH,DNS, DHCP,ETC.) In the above example we use SSH to essentially SSH our way and connect our Windows 10 VM and log into Linux. We are able to observe the traffic on wireshark when we type different commands on the Linux machine.
</p>
<br />
