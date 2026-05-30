# Azure Network Protocols Lab Case Study

## Scenario

A support technician needs to troubleshoot connectivity between cloud-hosted Windows and Linux systems. The possible causes include virtual network configuration, private IP routing, DNS resolution, remote access settings, and Azure Network Security Group firewall rules.

## Environment

- Microsoft Azure
- Windows virtual machine used as the troubleshooting workstation
- Linux virtual machine used as the target server
- Azure Virtual Network
- Azure Network Security Group
- PowerShell
- Remote Desktop Protocol
- SSH
- Wireshark
- ICMP / ping
- DNS lookup

## Troubleshooting Process

1. Created an Azure resource group to organize the lab resources.
2. Deployed a Windows VM and Linux VM into the Azure lab environment.
3. Verified internal private IP connectivity from Windows to Linux using ping.
4. Verified SSH access from Windows to Linux over the private network.
5. Tested TCP port 22 reachability with PowerShell.
6. Verified DNS resolution from the Windows VM.
7. Applied an Azure NSG rule to deny ICMP traffic.
8. Confirmed ping failure after the deny rule was applied.
9. Used Wireshark to inspect packet behavior during blocked and allowed traffic.
10. Removed the deny rule and confirmed ICMP request/reply traffic returned.
11. Deleted the Azure resource group and saved proof that the cloud resources were removed.

## Result

The lab demonstrates a complete beginner-to-junior cloud troubleshooting workflow: build, verify, break, inspect, restore, document, and clean up. It shows practical understanding of private IP communication, remote access, DNS testing, Azure NSG behavior, and packet-level troubleshooting.

## Support Relevance

This maps to real support work because many cloud connectivity problems are caused by firewall rules, DNS behavior, or service reachability issues rather than the server being offline. The screenshots and command outputs show how to prove each layer instead of guessing.
