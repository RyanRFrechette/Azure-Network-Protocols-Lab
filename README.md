# Azure Network Protocols and NSG Troubleshooting Lab

## Recruiter TLDR
This is a beginner-to-junior Azure networking portfolio lab showing how I set up a cloud troubleshooting environment, document each step with screenshots, and explain the support value behind the work. The finished lab will include Azure VMs, network security groups, Wireshark, ICMP, DNS, SSH, and RDP troubleshooting evidence.

## Business Scenario
A support technician needs to troubleshoot cloud-hosted systems that may be affected by network configuration, firewall rules, DNS behavior, or remote access issues. This lab rebuild documents that process step by step using Microsoft Azure and clear local screenshots.

## Lab Status
Rebuild in progress. Screenshots are being added one at a time, committed to GitHub, and explained for hiring managers.

## Screenshot Walkthrough

### 1. Resource Group Creation Review

![Azure resource group creation review](screenshots/setup/00-resource-group-create-review.png)

This screenshot shows the Azure resource group configuration before deployment. The resource group is the container used to organize the lab resources for this project, including the virtual machines, virtual network, network security group, and protocol testing environment. For a help desk or junior cloud support role, this demonstrates basic Azure portal navigation, resource organization, and awareness of how cloud infrastructure is grouped before troubleshooting begins.

### 2. Resource Group Overview

![Azure resource group overview](screenshots/setup/01-resource-group-overview.png)

This screenshot shows the completed Azure resource group that will contain the lab environment. In a support role, resource groups help technicians quickly identify which virtual machines, networks, security rules, and services belong to the same system or troubleshooting scenario. This confirms the cloud workspace is ready before deploying the Windows and Linux virtual machines.


### 3. Windows VM Overview

![Azure Windows VM overview](screenshots/setup/02-windows-vm-overview.png)

This screenshot shows the Windows virtual machine created for the lab. The VM acts as the support workstation used to test connectivity, run command-line troubleshooting tools, connect over RDP, and later capture protocol traffic with Wireshark. For a help desk or junior cloud support role, this demonstrates basic Azure VM deployment, cost-aware configuration, and safe documentation of cloud resources without exposing sensitive details.


### 4. Linux VM Overview

![Azure Linux VM overview](screenshots/setup/03-linux-vm-overview.png)

This screenshot shows the Linux virtual machine created as the target system for protocol and connectivity testing. It is placed in the same Azure virtual network as the Windows VM, but it does not expose inbound internet access. For a help desk or junior cloud support role, this demonstrates safer cloud lab design, internal network testing, and the ability to separate a troubleshooting client from a target server.


### 5. ICMP Test: Windows VM to Linux VM

![Windows VM pinging Linux VM successfully](screenshots/icmp/04-windows-to-linux-ping-success.png)

This screenshot shows a successful ping from the Windows VM to the Linux VM using the Linux VM's private IP address. The replies confirm that both virtual machines are on the same Azure virtual network and can communicate internally without exposing the Linux VM directly to the internet. For a help desk or junior cloud support role, this demonstrates basic ICMP testing, private IP troubleshooting, and validation of cloud network connectivity.


### 6. SSH Test: Windows VM to Linux VM

![Windows VM SSH connection to Linux VM](screenshots/ssh/05-windows-to-linux-ssh-success.png)

This screenshot shows a successful SSH connection from the Windows VM to the Linux VM using the Linux VM's private IP address. This confirms that the Windows support workstation can securely access the Linux target over the internal Azure virtual network without exposing SSH directly to the public internet. For a help desk or junior cloud support role, this demonstrates private network access, remote administration, SSH troubleshooting, and secure cloud lab design.


### 7. TCP Test: SSH Port 22 Connectivity

![Windows VM testing TCP port 22 to Linux VM](screenshots/tcp/06-windows-to-linux-ssh-port-test.png)

This screenshot shows a successful TCP port test from the Windows VM to the Linux VM on port 22. Unlike a basic ping test, this confirms that the SSH service is reachable over the internal Azure virtual network. For a help desk or junior cloud support role, this demonstrates port-level troubleshooting, service reachability testing, and the difference between general network connectivity and application-specific connectivity.


### 8. RDP Access: Host Computer to Windows VM

![RDP session connected to Azure Windows VM](screenshots/rdp/07-rdp-session-proof.png)

This screenshot shows a Remote Desktop session into the Azure Windows VM. RDP access is a common support workflow for remotely inspecting a Windows system, running troubleshooting commands, validating connectivity, and documenting findings. For a help desk or junior cloud support role, this demonstrates remote access familiarity and the ability to work inside a cloud-hosted Windows environment.


### 9. DNS Test: Name Resolution from Windows VM

![Windows VM DNS lookup test](screenshots/dns/08-dns-lookup-output.png)

This screenshot shows a DNS lookup from the Windows VM resolving microsoft.com to public IP addresses. DNS testing helps separate name resolution problems from network connectivity problems. For a help desk or junior cloud support role, this demonstrates basic DNS troubleshooting using command-line tools inside a cloud-hosted Windows environment.


### 10. NSG Block Test: ICMP Denied

![Windows VM ping blocked by Azure NSG rule](screenshots/nsg/09-icmp-blocked-by-nsg.png)

This screenshot shows ping failing after an Azure Network Security Group rule was applied to deny ICMP traffic from the Windows VM to the Linux VM. Earlier screenshots proved the same ping worked before the rule change, so this demonstrates how a cloud firewall rule can block traffic even when both virtual machines are running. For a help desk or junior cloud support role, this shows firewall-based troubleshooting and before/after connectivity validation.


### 11. Wireshark Setup: Ethernet Interface Selected

![Wireshark showing Ethernet capture interface](screenshots/wireshark/10-wireshark-interface-selected.png)

This screenshot shows Wireshark installed on the Azure Windows VM with the Ethernet capture interface available. This confirms the packet-capture tool is ready before running protocol tests. For a help desk or junior cloud support role, this demonstrates the ability to prepare a Windows troubleshooting workstation for network traffic inspection instead of relying only on command-line results.

### 12. Wireshark Capture: ICMP Blocked by NSG

![Wireshark showing ICMP requests blocked by NSG](screenshots/wireshark/11-wireshark-icmp-blocked-capture.png)

This screenshot shows Wireshark capturing ICMP echo requests from the Windows VM to the Linux VM while the Azure Network Security Group deny rule is active. The capture shows requests going from the Windows private IP to the Linux private IP with no successful replies, matching the failed ping test. For a help desk or junior cloud support role, this demonstrates packet-level troubleshooting and confirms that the connectivity failure is caused by traffic being blocked, not by the command-line tool itself.

## Tools Planned
- Microsoft Azure
- Windows virtual machine
- Linux virtual machine
- Azure Virtual Network
- Azure Network Security Group
- Remote Desktop Protocol
- PowerShell
- Wireshark
- ICMP / ping
- DNS lookup
- SSH

## Skills Demonstrated
- Azure portal navigation
- Cloud resource organization
- Screenshot-based technical documentation
- Beginner cloud networking fundamentals
- Support-focused troubleshooting mindset
- Clear written explanations for escalation or ticket notes

## Privacy Note
Screenshots are reviewed before publishing to avoid exposing credentials, secrets, subscription IDs, private keys, or unnecessary personal information.

## Next Step
Create and document the Windows virtual machine, then continue building the Azure networking lab one screenshot at a time.



