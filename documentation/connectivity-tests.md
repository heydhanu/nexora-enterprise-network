# Nexora Technologies – Network Connectivity Testing

## 1. Test Environment

Network connectivity and security were tested using Cisco Packet Tracer 9.0.

## 2. Connectivity Tests

### Internal Network Connectivity

| Test | Expected Result | Status |
|---|---|---|
| ADMIN to default gateway | Successful | PASS |
| ADMIN to DHCP server | Successful | PASS |
| ADMIN to FINANCE | Successful | PASS |
| IT to ADMIN | Successful | PASS |
| IT to FINANCE | Successful | PASS |
| IT to STAFF | Successful | PASS |
| Internal DNS resolution | Successful | PASS |
| Internal website access | Successful | PASS |

### Security Tests

| Test | Expected Result | Status |
|---|---|---|
| FINANCE to ADMIN | Blocked | PASS |
| FINANCE to STAFF | Blocked | PASS |
| STAFF to ADMIN | Blocked | PASS |
| STAFF to FINANCE | Blocked | PASS |
| GUEST to internal web server | Blocked | PASS |

### External Connectivity

| Test | Expected Result | Status |
|---|---|---|
| GUEST to external test PC | Successful | PASS |
| ADMIN to external test PC | Successful | PASS |
| NAT/PAT translation | Translation observed | PASS |

### Switch Security

| Test | Expected Result | Status |
|---|---|---|
| Unused switch ports | Administratively disabled | PASS |
| Unused switch port assignment | VLAN 999 | PASS |

## 3. Test Summary

The tests confirmed that the simulated enterprise network supports internal connectivity, network services, controlled inter-department communication and external access.

Guest network restrictions and unused switch port hardening were also verified.

## 4. Testing Tools

- Cisco Packet Tracer PC Command Prompt
- ping command
- nslookup and DNS resolution
- Web Browser
- Cisco IOS CLI
- show ip nat translations
- show interfaces status