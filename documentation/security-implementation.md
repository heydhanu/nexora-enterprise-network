# Nexora Technologies – Security Implementation

## 1. VLAN Segmentation

The network is divided into separate VLANs to isolate departments and control communication between network segments.

- VLAN 10: ADMIN
- VLAN 20: FINANCE
- VLAN 30: IT
- VLAN 40: STAFF
- VLAN 50: SERVERS
- VLAN 60: GUEST
- VLAN 99: MANAGEMENT

## 2. Access Control Lists (ACLs)

Extended ACLs are configured on R1-EDGE to control traffic between selected network segments.

### FINANCE Network
- Blocks FINANCE-initiated traffic to ADMIN.
- Blocks FINANCE-initiated traffic to STAFF.
- Allows specified ICMP echo-reply traffic for permitted ping responses.
- Allows other traffic according to the remaining ACL rules.

### STAFF Network
- Blocks STAFF-initiated traffic to ADMIN.
- Blocks STAFF-initiated traffic to FINANCE.
- Allows specified ICMP echo-reply traffic for permitted ping responses.
- Allows other traffic according to the remaining ACL rules.

### GUEST Network
- Allows DHCP requests.
- Allows access to the GUEST default gateway.
- Blocks access to internal private network addresses.
- Allows access to destinations outside the internal network ranges.

## 3. Unused Switch Port Hardening

Unused switch ports are assigned to VLAN 999 (UNUSED) and administratively disabled.

This reduces the risk of unauthorised devices connecting through unused physical ports.

## 4. Network Security Objectives

The security implementation aims to:

- Separate departmental network traffic.
- Restrict unauthorised inter-department communication.
- Isolate guest devices from internal resources.
- Reduce risks from unused physical switch ports.
- Maintain necessary network services and external connectivity.

## 5. Verification

The following security behaviours were tested:

- FINANCE access to ADMIN and STAFF was blocked.
- STAFF access to ADMIN and FINANCE was blocked.
- GUEST access to internal servers was blocked.
- GUEST access to the simulated external network was permitted.
- DHCP remained functional for guest clients.
- Unused switch ports were verified as disabled and assigned to VLAN 999.