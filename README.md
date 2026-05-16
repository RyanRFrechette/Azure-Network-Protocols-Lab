<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Examining Network Protocols and Network Security Group (NSG) Management</h1>

<h2>About This Project</h2>

This portfolio lab demonstrates hands-on network troubleshooting and traffic analysis inside Microsoft Azure. It uses Windows and Linux virtual machines, Wireshark, command-line tools, and Azure Network Security Groups to observe how common network protocols behave and how firewall-style cloud rules affect connectivity.

This project is relevant to help desk, cloud support, network support, and junior systems roles because it shows practical troubleshooting skills: testing connectivity, reading protocol behavior, understanding DNS/SSH/RDP/ICMP traffic, and using NSG rules to allow or deny traffic in a cloud environment.

In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDP, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Install and configure Wireshark
- Perform network activities and observe traffic in Wireshark
- Configure Network Security Groups in Azure Portal
- Analyze different types of network traffic in Wireshark

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/3RvPBHn.png" height="80%" width="80%" alt="Wireshark capture in Azure"/>
</p>
<p>
I gained hands-on experience with network analysis using Wireshark, a widely-used network protocol analyzer. The primary objective was to install and configure Wireshark, perform network activities, and observe the generated traffic in Wireshark. The entire process was executed within the Azure environment, utilizing two virtual machines (VM1 and VM2).
</p>
<br />

<p>
<img src="https://i.imgur.com/6wdotlb.png" height="80%" width="80%" alt="Installing Wireshark"/>
</p>
<p>
The installation and configuration of Wireshark on VM1 involved connecting to the virtual machine through Microsoft Remote Desktop. After downloading and installing Wireshark, I began capturing network traffic by selecting the Ethernet option. Throughout the lab, I applied various filters to focus on specific types of network traffic as needed.
</p>
<br />

<p>
<img src="https://i.imgur.com/LFEnDg3.png" height="80%" width="80%" alt="PowerShell network testing"/>
</p>
<p>
The next phase of the project involved performing network activities and observing the resulting traffic in Wireshark. By utilizing PowerShell on VM1, I executed various network tasks, such as pinging VM2 and external sites, connecting to VM2 via SSH, renewing VM1's IP address, and conducting DNS lookups. Monitoring the traffic in Wireshark provided valuable insights into how these network activities generated different types of traffic.
</p>
<br />

<p>
<img src="https://i.imgur.com/75vM76Q.png" height="80%" width="80%" alt="Azure Network Security Group rule testing"/>
</p>
<p>
An essential aspect of the project was configuring Network Security Groups within the Azure Portal. I created a new inbound security rule for VM2 to deny ICMP traffic, simulating a real-life scenario where specific traffic types might be blocked for security reasons. After updating the rule to allow ICMP traffic, I observed the successful pinging between VM1 and VM2, demonstrating the impact of security configurations on network communication.
</p>
<br />

<p>
<img src="https://i.imgur.com/0zDtwkB.png" height="80%" width="80%" alt="Protocol analysis filters"/>
</p>
<p>
Lastly, the lab enabled me to analyze various types of network traffic in Wireshark by applying different filters, such as ICMP, SSH, DHCP, DNS, UDP, and RDP. This exercise deepened my understanding of how each network protocol functions and how they interact within a networked environment.
</p>
<br />

<p>
<img src="https://i.imgur.com/yYzsS1k.png" height="80%" width="80%" alt="Network lab summary"/>
</p>
<p>
Overall, this lab project was a valuable learning experience, reinforcing my understanding of network analysis, security configurations, and protocol interactions. By working with Wireshark and Azure, I gained practical skills that can be applied in various network administration and security roles.
</p>
<br />
