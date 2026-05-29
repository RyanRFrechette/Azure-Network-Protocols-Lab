<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

# Azure Network Protocols and NSG Troubleshooting Lab

## Recruiter TL;DR

This repo demonstrates cloud/network troubleshooting in Azure using Windows and Linux VMs, Wireshark, command-line tests, and Network Security Groups. It proves I can test connectivity, identify protocol behavior, understand how cloud firewall rules affect access, and document troubleshooting evidence clearly for support or escalation.

## Project Summary

This lab demonstrates network troubleshooting inside Microsoft Azure using Windows and Linux virtual machines, Wireshark packet capture, command-line tools, and Azure Network Security Groups. I tested common protocols, observed traffic behavior, and changed cloud firewall rules to see how security policy affects connectivity.

This is a portfolio project for help desk, cloud support, network support, and junior systems roles. It shows practical troubleshooting ability: verify connectivity, isolate DNS or protocol issues, understand traffic flow, and explain what is happening at the network level.

## Hiring Manager Snapshot

| Area | What this lab demonstrates |
|---|---|
| Azure Networking | Built a VM-based network lab in Azure |
| Connectivity Testing | Used ping, SSH, DNS lookup, and Remote Desktop scenarios |
| Packet Analysis | Captured and filtered traffic in Wireshark |
| Network Security Groups | Created rules to allow and deny traffic |
| Troubleshooting Process | Compared expected behavior vs blocked/allowed traffic |
| Protocol Awareness | Observed ICMP, SSH, DHCP, DNS, UDP, and RDP behavior |
| Documentation | Captured screenshots and explained technical findings clearly |

## Business Scenario

A support technician is asked to investigate why two cloud-hosted machines cannot communicate. The issue could be DNS, firewall rules, protocol blocking, VM configuration, or routing.

This lab simulates that kind of troubleshooting by using two Azure VMs, testing connectivity, observing traffic in Wireshark, then changing Network Security Group rules to see how access changes.

## Tools and Technologies

- Microsoft Azure Virtual Machines
- Azure Network Security Groups
- Windows 10 VM
- Ubuntu Server VM
- Remote Desktop
- PowerShell / Command Line
- Wireshark
- ICMP
- SSH
- DHCP
- DNS
- RDP

## What I Built and Tested

- Created two virtual machines in Azure
- Connected to the Windows VM using Remote Desktop
- Installed and configured Wireshark
- Captured live network traffic
- Used protocol filters to isolate traffic types
- Tested ICMP/ping between machines
- Tested SSH traffic to the Linux VM
- Ran DNS lookups and observed DNS behavior
- Renewed IP configuration and observed DHCP traffic
- Created an NSG rule to deny ICMP traffic
- Verified how blocked traffic appears during troubleshooting
- Re-enabled ICMP and confirmed connectivity returned

## Skills Demonstrated

- Cloud networking fundamentals
- Azure NSG rule awareness
- Network connectivity troubleshooting
- Packet capture and traffic analysis
- DNS troubleshooting basics
- SSH/RDP protocol awareness
- Windows and Linux VM support basics
- Evidence-based technical documentation
- Ability to explain network behavior in plain language

## Lab Evidence and Walkthrough

### 1. Wireshark Setup in Azure

<p>
<img src="https://i.imgur.com/3RvPBHn.png" height="80%" width="80%" alt="Wireshark capture in Azure"/>
</p>

I used a Windows VM in Azure as the troubleshooting workstation and installed Wireshark to observe live traffic. This gave visibility into what was happening during connectivity tests instead of relying only on command output.

### 2. Packet Capture and Filters

<p>
<img src="https://i.imgur.com/6wdotlb.png" height="80%" width="80%" alt="Installing Wireshark"/>
</p>

I captured traffic from the active network interface and applied filters to focus on specific protocols. Filtering is important in real support work because raw network captures can be noisy.

### 3. Connectivity and Protocol Testing

<p>
<img src="https://i.imgur.com/LFEnDg3.png" height="80%" width="80%" alt="PowerShell network testing"/>
</p>

I used command-line tools to generate traffic and validate connectivity. Examples included ping tests, SSH connections, DNS lookups, and IP renewal commands. This helped connect command-line troubleshooting with what appeared in Wireshark.

### 4. NSG Rule Change and Blocked Traffic

<p>
<img src="https://i.imgur.com/75vM76Q.png" height="80%" width="80%" alt="Azure Network Security Group rule testing"/>
</p>

I created a Network Security Group inbound rule to deny ICMP traffic to the Linux VM. After applying the rule, ping behavior changed, proving that Azure NSG rules can directly affect VM-to-VM communication.

### 5. Protocol Analysis

<p>
<img src="https://i.imgur.com/0zDtwkB.png" height="80%" width="80%" alt="Protocol analysis filters"/>
</p>

I reviewed traffic for protocols such as ICMP, SSH, DHCP, DNS, UDP, and RDP. This helped reinforce how different support scenarios create different traffic patterns.

### 6. Lab Summary

<p>
<img src="https://i.imgur.com/yYzsS1k.png" height="80%" width="80%" alt="Network lab summary"/>
</p>

This lab connected cloud networking, packet analysis, and support troubleshooting into one repeatable workflow.

## Real-World Support Relevance

This lab maps to common support and cloud tickets such as:

- “I cannot connect to the server”
- “Ping works from one machine but not another”
- “Remote Desktop is not responding”
- “SSH to a Linux VM is failing”
- “DNS lookup is not resolving correctly”
- “A firewall or NSG rule may be blocking access”
- “Traffic is allowed in one direction but blocked in another”

## Troubleshooting Method Used

1. Confirm the source and destination machines
2. Test basic connectivity
3. Identify which protocol is failing
4. Capture traffic when possible
5. Check cloud firewall / NSG rules
6. Change one variable at a time
7. Retest and document the result

## What I Learned

- NSG rules can create issues that look like server or application problems
- Packet capture makes troubleshooting more evidence-based
- Different protocols require different tests and filters
- DNS and connectivity should be verified before assuming an application is broken
- Clear screenshots and notes make troubleshooting easier to communicate and escalate

## Status

Completed portfolio lab. Future improvements could include route tables, private/public IP comparisons, Network Watcher flow logs, VPN scenarios, and a deeper incident-style troubleshooting write-up.
