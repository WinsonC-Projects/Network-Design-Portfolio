# Enterprise Network with Redundant Core Routing

## Overview

This lab demonstrates the design and implementation of a hierarchical enterprise network using Cisco Packet Tracer. The topology features a three-router core with full mesh connectivity, four access-layer switches, and eight end-user devices across multiple subnets.

## Network Topology

- **Core Layer**: 3 routers (Router1, Router2, Router3) in a triangle/full mesh topology
- **Access Layer**: 4 switches (Switch1, Switch2, Switch3, Switch4)
- **End Devices**: 8 PCs distributed across 4 different subnets

## IP Addressing Scheme

### Subnets

| Subnet   | Network Address | Subnet Mask   | Connected Switch | PCs      |
| -------- | --------------- | ------------- | ---------------- | -------- |
| Subnet 1 | 192.168.10.0/24 | 255.255.255.0 | Switch1          | PC1, PC2 |
| Subnet 2 | 192.168.11.0/24 | 255.255.255.0 | Switch2          | PC3, PC4 |
| Subnet 3 | 192.168.12.0/24 | 255.255.255.0 | Switch3          | PC5, PC6 |
| Subnet 4 | 192.168.13.0/24 | 255.255.255.0 | Switch4          | PC7, PC8 |

### Router Interconnections

- Router1 ↔ Router3: 192.168.14.0/30
- Router2 ↔ Router3: 192.168.15.0/30
- Router1 ↔ Router2: 192.168.12.0/30 (via Switch3)

### Device IP Addresses

- **PC1**: 192.168.10.2/24 | Gateway: 192.168.10.1
- **PC2**: 192.168.10.3/24 | Gateway: 192.168.10.1
- **PC3**: 192.168.11.2/24 | Gateway: 192.168.11.1
- **PC4**: 192.168.11.3/24 | Gateway: 192.168.11.1
- **PC5**: 192.168.12.2/24 | Gateway: 192.168.12.1
- **PC6**: 192.168.12.3/24 | Gateway: 192.168.12.1
- **PC7**: 192.168.13.2/24 | Gateway: 192.168.13.1
- **PC8**: 192.168.13.3/24 | Gateway: 192.168.13.1

## Technologies Implemented

- **IP Subnetting**: /24 networks for user subnets, /30 for router interconnections
- **Inter-VLAN Routing**: Router-on-a-stick or Layer 3 switching
- **Routing**: Static routes or dynamic routing protocol (OSPF/EIGRP)
- **Network Redundancy**: Multiple paths between core routers for fault tolerance
- **Hierarchical Design**: Three-tier architecture (core, distribution, access)

## Lab Objectives

1. Design a scalable enterprise network with proper IP addressing
2. Configure routers for inter-subnet communication
3. Implement redundant paths for high availability
4. Verify end-to-end connectivity across all subnets
5. Apply hierarchical network design principles

## Verification & Testing

Connectivity testing was performed using ICMP (ping) to verify routing functionality:

- ✅ PC1 successfully communicated with all PCs (PC2-PC8) across different subnets
- ✅ All ICMP packets showed "Successful" status
- ✅ Inter-VLAN routing confirmed operational
- ✅ Default gateway configurations verified

## Skills Demonstrated

- Network topology design
- IP addressing and subnetting (VLSM)
- Router and switch configuration
- Routing protocol implementation
- Network troubleshooting and verification
- Documentation and network diagramming

## Files Included

- `Cisco Packet Tracer.pkt` - Complete network topology and configurations
- Network topology screenshot showing logical layout
- PDU simulation screenshot demonstrating successful connectivity

## Tools Used

- Cisco Packet Tracer
- IP addressing calculations
- Network design principles

## How to Use

1. Download and open the `.pkt` file in Cisco Packet Tracer
2. Switch to Simulation Mode to observe packet flow
3. Use the "Add Simple PDU" tool to test connectivity between devices
4. Examine router configurations using CLI commands (`show ip route`, `show ip interface brief`)

## Key Learning Outcomes

- Understanding of hierarchical network design
- Practical experience with IP subnetting and address planning
- Configuration of multi-router environments
- Implementation of redundant network paths
- Verification techniques for network connectivity

## Author

Created as part of Digital Forensics & Cybersecurity graduate coursework demonstrating practical networking skills applicable to security architecture and network defense.

---
