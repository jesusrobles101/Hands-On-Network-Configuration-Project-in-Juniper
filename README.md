# Hands On Network Configuration Project in Juniper

## Introduction

This project demonstrates my practical skills in cloud-based network management, switch configuration, and implementation of various networking protocols.

## Project Overview
- Objective: Set up and configure a small campus network using Juniper Mist Wired Assurance
- Duration: Approximately 24 hours
- Environment: Juniper Cloud Labs (JCL) virtual environment

## Network Topology
The lab topology consists of a single Core switch and two Access switches (and one for future), representing two different IDFs. The Core switch functions as both the default gateway for local VLANs and forms an OSPF adjacency with the internet firewall.

![image](https://github.com/user-attachments/assets/eee3afd6-3bd5-4f64-887d-72343632b956)

- 1 Core Switch (vEX)
- 2 Access Switches (vEX)
- 1 Spare Switch (for future use)
- Virtual firewall (vSRX)
- 2 User VLANs


## Key Technologies Demonstrated
- Juniper Mist Cloud Platform
- Switch configuration management
- VLANs and trunking
- Layer 3 routing (OSPF)
- DHCP server configuration
- Out-of-band management

## Configuration Process
### 1. Organization-level Switch Template
- Created a template for common switch configurations
- Configured authentication and accounting servers
- Set up NTP and DNS settings
- Created a management VLAN (VLAN 1033)
### 2. Site-specific Configuration
- Created site-specific VLANs:
  - User_Vlan_A (VLAN 1088)
  - User_Vlan_B (VLAN 1099)
- Configured port profiles:
  - switch_uplink (trunk)
  - access_user_a
  - access_user_b
### 3. Core Switch Configuration
- Named the switch "core_01"
- Configured in-band management IP
- Set up IRBs for User VLANs
- Configured LACP trunks to access switches
- Implemented DHCP server for user VLANs
- Configured OSPF
### 4. Access Switch Configuration
- Configured access_01 and access_02
- Set in-band management IPs
- Applied appropriate port profiles

### 5. Advanced Configuration Using Site Variables
- Demonstrated use of site variables for scalable configuration
- Created User_Vlan_C using variables

## Key Skills Demonstrated
1. Cloud-based Network Management
2. Switch Configuration
3. Layer 3 Networking
4. Network Segmentation
5. DHCP Configuration
6. Port Profiling
7. Template-based Configuration
8. Variable-based Configuration
9. Network Validation
10. Documentation Skills

## Challenges and Solutions
- Configuring OSPF routing between the core switch and firewall presented some difficulties. I had to carefully verify the adjacency and routing table to ensure proper operation.
- Setting up the DHCP server on the core switch to serve multiple VLANs required careful IP planning and configuration to avoid conflicts.
- Managing multiple VLANs and ensuring correct trunking across switches required attention to detail, especially with the different user VLANs.

## Results and Validation
- Successfully configured and connected all switches
- Verified OSPF operation and routing
- Tested user connectivity across VLANs
- Demonstrated monitoring capabilities in Mist Wired Assurance

## Conclusion
This project showcases my ability to:
- Configure and manage enterprise network switches
- Implement cloud-based network management solutions
- Troubleshoot and validate network configurations
- Apply best practices in network design and security

Thank you for your time. I'd be happy to answer any questions about the project or discuss how these skills can benefit your organization.
