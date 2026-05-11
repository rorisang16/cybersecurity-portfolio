# Enterprise Network Segmentation Lab

## Overview

Built a segmented enterprise-style network in Cisco Packet Tracer using VLANs, trunking, and router-on-a-stick inter-VLAN routing.

The lab includes:
- VLAN segmentation
- Inter-VLAN communication
- Static IP configuration
- 802.1Q trunking
- Router subinterfaces
- Network troubleshooting

---

# Network Topology

![Enterprise Network Topology]network-security\images\network topology.png

---

# IP Addressing

| Device | VLAN | IP Address | Gateway |
|---|---|---|---|
| EMP-WS01 | 10 | 10.10.10.10 | 10.10.10.1 |
| ATT-WS01 | 10 | 10.10.10.20 | 10.10.10.1 |
| APP-SRV01 | 20 | 10.10.20.30 | 10.10.20.1 |

---

# Endpoint Configuration

## EMP-WS01

Configured as an employee workstation in VLAN 10.

![EMP-WS01 Configuration](images/emp-ws01-ip-config.png)

---

## ATT-WS01

Configured as a second workstation to simulate another internal user/attacker.

![ATT-WS01 Configuration](images/att-ws01-ip-config.png)

---

## APP-SRV01

Configured inside the server VLAN.

![APP-SRV01 Configuration](images/app-srv01-ip-config.png)

---

# VLAN Configuration

Created separate VLANs for users, servers, and admin traffic.

| VLAN | Name |
|---|---|
| 10 | USERS |
| 20 | SERVERS |
| 30 | ADMIN |

![VLAN Creation](images/VLAN%20Creation.png)

---

# Port Assignments

Assigned switch ports to the correct VLANs.

| Interface | Assignment |
|---|---|
| Fa0/1 | VLAN 10 |
| Fa0/2 | VLAN 10 |
| Fa0/3 | VLAN 20 |
| Fa0/4 | Trunk Port |

![VLAN Port Assignments](images/VLAN%20Port%20Assignments.png)

---

# Router Configuration

Configured router-on-a-stick inter-VLAN routing using subinterfaces.

## Initial Router Setup

![Router Initial Setup](images/Route%20Configuration%20Started.png)

---

## Subinterface Configuration

Configured:
- GigabitEthernet0/0.10
- GigabitEthernet0/0.20

Used 802.1Q encapsulation for VLAN tagging.

![Subinterface Configuration](images/Subinterface%20Configuration.png)

---

## Interface Verification

Verified interfaces were operational and assigned correctly.

![Subinterface Verification](images/Subinterface%20Verification.png)

---

# Troubleshooting

Inter-VLAN communication initially failed.

Troubleshooting included:
- checking VLAN assignments
- verifying trunk configuration
- checking interface states
- validating router subinterfaces

---

## VLAN Verification

![VLAN Troubleshooting](images/trunk_troubleshoot.png)

---

## Interface Verification

![Interface Troubleshooting](images/trunk_troubleshoot_2.png)

---

## Trunk Resolution

The issue was caused by the trunk configuration between the switch and router.

After reconfiguring the trunk port, inter-VLAN communication succeeded.

![Trunk Resolution](images/trunk_troubleshoot_3.png)

---

# Connectivity Testing

Successful communication between VLANs after troubleshooting.

![Successful Ping Test](images/ping%2010.10.20.30%20command.png)

---

# Skills Demonstrated

- VLAN segmentation
- Inter-VLAN routing
- Cisco switch configuration
- Router subinterfaces
- 802.1Q trunking
- Network troubleshooting
- Enterprise network design

---

# Security Relevance

Network segmentation reduces lateral movement and isolates critical systems from user devices.

This is commonly used in enterprise environments to improve:
- access control
- monitoring
- containment
- infrastructure security
