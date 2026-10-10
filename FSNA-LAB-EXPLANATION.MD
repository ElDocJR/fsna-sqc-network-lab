# FSNA SQC | Lab Explanation
**Author: Josh Roybal**

## Objective
Build and validate a simulated network supporting management, data, and voice services. The reference guide also includes wireless access. The exercise integrates Layer 2 switching, Layer 3 routing, addressing, secure management, and endpoint connectivity.

## Environment
Cisco Packet Tracer provides the simulated network. The guide specifies two switches, one router, a management PC, two user PCs, two phones, a wireless access point, and a tablet. Management, data, and voice use separate VLANs; router subinterfaces provide their gateways.

## Assessed work
The assessment credits configuration of switch hostnames and clocks, management addresses/default gateways, login settings, password-related configuration, SSH/Telnet settings, management ACLs, VLANs, data/voice access ports, QoS, and trunks. FSNA-SW1 also receives credit for spanning-tree root configuration.

Router credit covers subinterfaces, 802.1Q encapsulation, addresses, NAT-inside configuration, DHCP, a default route, and ephone directory numbers. The supplied report also credits functional host connectivity. Guide-defined wireless configuration is not separately listed in the report.

## Design explanation
VLANs create separate broadcast domains. Access ports connect endpoints to the appropriate VLAN; trunks carry several VLANs between network devices. Router-on-a-stick uses multiple tagged subinterfaces on one physical router link to route between VLANs.

DHCP supplies data clients with addressing parameters. SSH provides encrypted remote management; the VTY ACL restricts management connection sources. Spanning tree controls redundant switch paths to prevent Layer 2 loops. Voice VLANs and basic QoS settings support the telephony portion of the exercise.

## Verification
| Feature | Relevant verification method |
| --- | --- |
| VLAN membership | `show vlan` |
| Trunks | `show interfaces trunk` |
| Spanning-tree roles | `show spanning-tree` |
| Interface state/addressing | `show ip interface brief` |
| Routes | `show ip route` |
| DHCP | `show ip dhcp binding` and client `ipconfig /all` |
| Reachability | Gateway and simulated upstream ping tests |
| Management access | SSH login and ACL inspection/testing |
| Telephony | `show ephone` and call tests |
| Saved configuration | `show startup-config` |

These are guide-defined or relevant verification methods, not a reconstruction of the exact commands used in the assessed submission. Raw command outputs are not included. The score report provides the available external evidence of functional connectivity.

## Troubleshooting
The report contains no item-specific failure notes or diagnostic history. No specific troubleshooting incident is claimed. A systematic diagnostic approach for this design checks physical/link state, VLAN membership, trunking, gateway interfaces, addressing, routing, and then application behavior. A blocked redundant link can be expected spanning-tree operation rather than a fault.

## Results
The supplied assessment report awards points across both switches, the router, and functional host connectivity. The listed awards total **1,000 points**: FSNA-SW1 300, FSNA-SW2 260, router 140, and connectivity 300. This total is calculated from the report rows; the report does not explicitly state an overall percentage or Pass label.

The report confirms a functional lab with host connectivity. It does not separately document wireless testing, individual call tests, or the command outputs used during verification.

## Lessons and technical interpretation
The exercise brings together VLANs, trunks, router subinterfaces, DHCP, management access controls, and spanning tree. It illustrates why configuration checks and functional tests serve different purposes: a feature can be present in the configuration while a dependency prevents it from working.

The guide sets NAT-inside on subinterfaces but does not show all outside/PAT prerequisites. Supporting upstream and voice settings may exist in the starter file. No claim is made that every prerequisite was configured from scratch. Password obfuscation settings should not be equated with strong credential encryption. Packet Tracer connectivity is simulated rather than a production Internet deployment.

## Source basis
Original summary of the supplied FSNA configuration guide and my three-page SQC report. The report displays 10-09-2026; the original attempt date is not independently established here. Assessment credit supports educational practical work, not unrestricted claims of independent professional proficiency.
