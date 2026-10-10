# FSNA SQC | Network Configuration Lab
**Josh Roybal | NGT Academy | Cisco Packet Tracer**

## Overview
An assessed educational network configuration project covering management, data, and voice networking. The reference design also includes wireless access. The assessment covers Cisco IOS switch/router configuration and functional host connectivity.

## Assessment outcome
The supplied assessment report awards points across both switches, the router, and functional host connectivity. The listed awards total **1,000 points**: FSNA-SW1 300, FSNA-SW2 260, router 140, and connectivity 300. This total is calculated from the report rows; the report does not explicitly state an overall percentage or Pass label.

The report confirms a functional lab with host connectivity. It does not separately document wireless testing, individual call tests, or the command outputs used during verification.

## Technical scope
- Switch identity, management addressing, local authentication, and console/VTY login.
- SSH management, disabled Telnet access, and management-subnet VTY ACLs.
- Management, data, and voice VLANs; data/voice access ports.
- Switch-to-switch and switch-to-router trunks.
- Spanning-tree root configuration and basic voice QoS.
- Router subinterfaces, 802.1Q encapsulation, and VLAN gateway addressing.
- NAT-inside markings, DHCP, upstream default routing, and phone directory numbers.

## Reference environment
Two switches (FSNA-SW1 and FSNA-SW2), one router (FSNA-RTR), a management workstation, user PCs, phones, and guide-defined wireless endpoints.

| VLAN | Purpose | Reference subnet | Gateway |
| --- | --- | --- | --- |
| 100 | Management | 192.168.100.0/24 | 192.168.100.1 |
| 200 | Data | 192.168.200.0/24 | 192.168.200.1 |
| 150 | Voice | 192.168.150.0/24 | 192.168.150.1 |

Addresses describe the supplied reference design; raw configuration exports are not included in this repository.

## Verification and documentation
The instructor assessment supports the credited configuration tasks and functional host connectivity. Individual command outputs and screenshots are not included in this version. Relevant verification methods include VLAN/trunk inspection, interface and route inspection, DHCP lease checks, and endpoint connectivity tests.

See [LAB-EXPLANATION.md](FSNA-LAB-EXPLANATION.md) for the design explanation, verification approach, and assessment boundaries.

## Evidence and scope
Sources: the supplied FSNA Basic Complete Lab Configuration guide and my FSNA SQC assessment report. This documentation summarizes the sources without reproducing the course guide or configuration answer key.

This is a simulated educational project. It does not claim production deployment experience, complete NAT/PAT implementation, or separately scored wireless validation. VLAN segmentation is not, by itself, a policy preventing routed inter-VLAN communication.

[View assessment results (public copy)](Evidence_FSNA-SQC-Results.pdf)
