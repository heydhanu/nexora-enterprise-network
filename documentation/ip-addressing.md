# Nexora Technologies – IP Addressing Plan

## 1. Network Overview

The network uses a private IPv4 addressing scheme with separate /24 subnets for each department and network segment.

### VLAN 10 – ADMIN
- Network: 192.168.10.0/24
- Default Gateway: 192.168.10.1

### VLAN 20 – FINANCE
- Network: 192.168.20.0/24
- Default Gateway: 192.168.20.1

### VLAN 30 – IT
- Network: 192.168.30.0/24
- Default Gateway: 192.168.30.1

### VLAN 40 – STAFF
- Network: 192.168.40.0/24
- Default Gateway: 192.168.40.1

### VLAN 50 – SERVERS
- Network: 192.168.50.0/24
- Default Gateway: 192.168.50.1

### VLAN 60 – GUEST
- Network: 192.168.60.0/24
- Default Gateway: 192.168.60.1

### VLAN 99 – MANAGEMENT
- Network: 192.168.99.0/24
- Default Gateway: 192.168.99.1

### VLAN 999 – UNUSED
- Reserved for unused switch ports
- No IP subnet assigned

## 2. Server Address Allocation

### DHCP Server
- IP Address: 192.168.50.10
- Purpose: Automatic IP address allocation

### DNS Server
- IP Address: 192.168.50.11
- Purpose: Internal domain name resolution

### WEB Server
- IP Address: 192.168.50.12
- Purpose: Internal website hosting

## 3. Network Addressing Design

- Each department is assigned a dedicated VLAN and subnet.
- Inter-VLAN communication is managed by the R1-EDGE router.
- DHCP provides automatic IP configuration to client devices.
- Servers use dedicated addresses within VLAN 50.
- VLAN 999 is reserved for unused switch ports.

## 4. External Network

The simulated external network uses the following addressing:

- R1-EDGE WAN interface: 203.0.113.1
- R2-ISP interface: 203.0.113.2
- External test PC: 198.51.100.10

NAT/PAT is configured on R1-EDGE to allow internal clients to access the simulated external network.