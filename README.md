# Enterprise Network Infrastructure Lab

Enterprise-grade network infrastructure developed in Cisco Packet Tracer focused on security, segmentation, redundancy, wireless management and centralized administration.

---

# Topology

![Topology](Enterprise-Network-Lab/docs/topology.png)

---

# Project Overview

This project simulates a real-world enterprise network environment using Cisco technologies and security best practices.

The infrastructure was designed using a hierarchical architecture model with:

- Core Layer
- Distribution Layer
- Access Layer
- Wireless Infrastructure
- Dedicated Management Network
- Server Segment
- DMZ Zone
- Border Firewalls
- ISP Connectivity
- Redundant Routing

---

# Infrastructure Features

## Network Segmentation

- Department-based VLAN segmentation
- Dedicated management VLAN
- Wireless client isolation
- Server VLAN separation
- Voice VLAN support

---

## Redundancy & High Availability

- Dual core switches
- HSRP default gateway redundancy
- EtherChannel aggregation
- Redundant firewall architecture
- OSPF dynamic routing

---

## Security Features

- SSH-only remote administration
- ACL-based management access
- Port Security
- BPDU Guard
- DHCP Snooping
- Dynamic ARP Inspection (DAI)
- Dedicated management subnet
- Disabled unused interfaces
- VLAN isolation
- Vlan Black Hole

---

## Wireless Infrastructure

- Wireless LAN Controller (WLC)
- Enterprise wireless segmentation
- Wireless client VLAN
- Centralized wireless administration

---

## Routing & Switching

- Inter-VLAN Routing
- OSPF Area 0
- Layer 3 core switching
- Trunking
- EtherChannel (LACP)
- HSRP gateway redundancy

---

# Network Architecture

## Core Layer

| Device | Function |
|---|---|
| sw-core1 | Primary Layer 3 Core |
| sw-core2 | Secondary Layer 3 Core |

The core layer is responsible for:

- Inter-VLAN routing
- Dynamic routing (OSPF)
- Gateway redundancy (HSRP)
- Distribution switching
- High availability

---

## Firewall Layer

| Device | Function |
|---|---|
| fw1 | Primary Border Firewall |
| fw2 | Secondary Border Firewall |

Firewall responsibilities:

- Border protection
- Access control
- ICMP filtering
- SSH management restriction
- WAN connectivity

---

## Access Layer

| Switch | Department |
|---|---|
| SW-ADM | Administration |
| sw-design | Design |
| sw-ti | IT |
| sw-financeiro | Finance |
| sw-marketing | Marketing |
| sw-caixa | POS/Cashier |
| sw-servidores | Servers |
| sw-gerenciamento | Management |
| sw-dmz | DMZ |

---

# VLAN Structure

| VLAN | Purpose | Subnet |
|---|---|---|
| 10 | Management | 192.168.10.0/24 |
| 20 | Administration | 192.168.20.0/24 |
| 30 | Design | 192.168.30.0/24 |
| 40 | IT | 192.168.40.0/24 |
| 50 | Wireless | 10.20.0.0/16 |
| 60 | Finance | 192.168.60.0/24 |
| 70 | Voice | Voice VLAN |
| 80 | POS/Cashier | 192.168.80.0/24 |
| 90 | Marketing | 192.168.90.0/24 |
| 100 | Servers | 10.11.11.32/27 |
| 199 | Disabled/Unused Ports | Isolated |

---

# Dynamic Routing

The infrastructure uses OSPF for internal routing.

## OSPF Features

- Area 0 backbone
- Dynamic route propagation
- Redundant path support
- Core-to-firewall routing

---

# High Availability

## HSRP

Implemented across all VLAN gateways:

- Virtual gateway redundancy
- Automatic failover
- Improved availability

---

## EtherChannel

LACP EtherChannel configured between core devices for:

- Link aggregation
- Increased bandwidth
- Redundancy

---

# Security Hardening

## Switch Security

- Sticky MAC
- Port-security
- Violation restriction
- BPDU Guard
- PortFast
- Disabled unused interfaces

---

## Layer 2 Protection

- DHCP Snooping
- Dynamic ARP Inspection
- Trusted trunk interfaces

---

## Administrative Security

- SSH Version 2
- ACL-restricted management
- Local authentication
- Management VLAN isolation

---

# Enterprise Services

The infrastructure includes:

- DHCP relay
- RADIUS-ready environment
- Wireless management
- Centralized administration
- DMZ segmentation
- Internal server infrastructure

---

# Technologies Used

- Cisco Packet Tracer
- Cisco Layer 2/3 Switching
- Cisco Routing
- OSPF
- HSRP
- EtherChannel
- VLANs
- STP
- SSH
- ACLs
- DHCP Snooping
- Dynamic ARP Inspection
- Wireless LAN Controller

---

# Repository Structure

```txt
Enterprise-Network-Lab/
│
├── README.md
├── packet-tracer/
│   └── enterprise-network-lab.pkt
│
├── docs/
│   ├── topology.png
│   ├── screenshots/
│   └── architecture-notes.md
│
├── configs/
│   ├── core/
│   ├── access/
│   ├── firewall/
│   ├── routing/
│   └── wireless/
│
└── verification/
    ├── show-ip-route.txt
    ├── show-vlan.txt
    ├── show-etherchannel.txt
    └── show-standby.txt
```

---

# Screenshots

## Core Infrastructure

Add screenshots showing:

- Core switches
- HSRP
- EtherChannel
- OSPF neighbors
- VLAN routing

---

## Security Features

Add screenshots showing:

- Port-security
- DHCP Snooping
- ARP Inspection
- SSH access restriction

---

# Usage

Open the `.pkt` file using:

- Cisco Packet Tracer 8.x+

---

# Objectives

This project was developed to improve skills in:

- Enterprise networking
- Cisco infrastructure
- Layer 2 security
- Layer 3 routing
- High availability
- Wireless networking
- Infrastructure hardening
- Network segmentation

---

# Author

Developed for networking and cybersecurity learning purposes.
