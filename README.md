# Nexora Technologies – Enterprise Network Infrastructure

## Project Overview

Nexora Technologies is a simulated enterprise network designed and implemented using Cisco Packet Tracer 9.0.

The project demonstrates practical networking skills through VLAN segmentation, inter-VLAN routing, network services, traffic filtering and network security configurations.

## Network Features

- VLAN segmentation for different departments
- Inter-VLAN routing using router-on-a-stick
- DHCP for automatic IP address allocation
- DNS for internal domain name resolution
- Internal web server hosting
- NAT/PAT for external network access
- Access Control Lists (ACLs) for traffic restrictions
- LACP EtherChannel for link aggregation
- Unused switch port hardening using VLAN 999

## Network Segments

| VLAN | Department | Network |
|---|---|---|
| 10 | ADMIN | 192.168.10.0/24 |
| 20 | FINANCE | 192.168.20.0/24 |
| 30 | IT | 192.168.30.0/24 |
| 40 | STAFF | 192.168.40.0/24 |
| 50 | SERVERS | 192.168.50.0/24 |
| 60 | GUEST | 192.168.60.0/24 |
| 99 | MANAGEMENT | 192.168.99.0/24 |
| 999 | UNUSED | Unused switch ports |

## Network Services

- DHCP Server: 192.168.50.10
- DNS Server: 192.168.50.11
- Web Server: 192.168.50.12
- Internal website: www.nexora.local

## Security Implementation

- Department-level traffic restrictions using ACLs
- Guest network isolation from internal networks
- Controlled access to network resources
- Unused switch ports assigned to VLAN 999 and administratively disabled

## Tools and Technologies

- Cisco Packet Tracer 9.0
- Cisco IOS CLI
- VLANs and 802.1Q trunking
- Inter-VLAN routing
- DHCP and DNS
- NAT/PAT
- Extended and standard ACL concepts
- LACP EtherChannel

## Project Files

- `nexora-network.pkt` – Cisco Packet Tracer project file
- `topology/network-topology.png` – Network topology diagram

## Project Purpose

This individual project was developed to strengthen practical knowledge of enterprise networking, network configuration, troubleshooting and infrastructure security.

**Author:** Dhanushini Balan