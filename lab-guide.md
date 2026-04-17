\#  Lab Guide –  Network Attack Detection Lab



\##  Purpose



This lab demonstrates how to build a segmented network in Cisco Packet Tracer and simulate an internal attack to validate firewall protections and incident detection.



The lab covers:

\- VLAN segmentation

\- Inter-VLAN routing

\- ACL firewall filtering

\- Attack simulation

\- Traffic analysis

\- Incident investigation



\---



\#  Step 1 – Build the Topology



Add the following devices in Cisco Packet Tracer:



\## Devices

\- 1 Router (Cisco 2911)

\- 1 Switch (Cisco 2960)

\- 2 User PCs

\- 1 Server

\- 1 Admin PC

\- 1 Attacker PC







\---



\#  Step 2 – Connect Devices



Use \*\*Copper Straight-Through\*\* cables.



| Device | Port | Switch Port |

|--------|------|-------------|

| USER1 | Fa0 | Fa0/1 |

| USER2 | Fa0 | Fa0/2 |

| SERVER | Fa0 | Fa0/3 |

| ADMIN | Fa0 | Fa0/4 |

| KALI | Fa0 | Fa0/5 |

| Router | gig0/0 | fa0/24 |



\---



\#  Step 3  VLAN Plan



| VLAN | Name | Network |

|------|------|---------|

| 10 | USERS | 192.168.10.0/24 |

| 20 | SERVERS | 192.168.20.0/24 |

| 30 | ADMIN | 192.168.30.0/24 |

| 99 | ATTACKER | 192.168.99.0/24 |



\---



\#  Step 4 – Configure Switch



Open SW1 CLI.



Enter privileged mode:



enable

configure terminal



\-Create and name VLANs

\-Assign Ports

\-Configure Trunk to Router

\-save



\---



\# step 5 - Configure Router



Open R1 CLI.



Enter privileged mode:



enable

configure terminal



\-Enable interface

\-Create Subinterfaces



\---



\# step 6 - Configure Firewall ACL



\-Block attacker VLAN.

\-Apply ACl to the attacker subinterface



\---



\# step 7 - Configure End Devices

\-Assign ip address, default gateway, subnetmask to all device.



\---



\# step 8 - Simulate Attack

\-On attacker PC command prompt:ping 192.168.20.10

&#x20;                              ping 192.168.30.10



\---



\# step 9 - Validate Normal Access



\-From USER PC:ping 192.168.20.10

\-Open browser:http://192.168.20.10



\---



\# step 10 - Check Logs



\-On router:show access-lists



\# step 11 - Packet Analysis



\-Switch to:



Simulation Mode



Filter:



ICMP

TCP

HTTP



Observe:



denied packets

packet source

packet destination



\---



\# Step 12 – Capture Evidence



\-take screenshots of:



Topology

VLANs

ACL rules

Successful user access

Blocked attacker traffic

ACL counters

Packet analysis



