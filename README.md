\#  Network Attack Detection Lab



\##  Project Overview

This project simulates a \*\*Security Operations Center (SOC) investigation workflow\*\* by building a segmented enterprise network in Cisco Packet Tracer and detecting unauthorized internal reconnaissance activity.



The lab demonstrates how network defenders can:

\- Segment networks using VLANs

\- Apply firewall rules using ACLs

\- Detect suspicious activity

\- Analyze traffic

\- Investigate incidents



\---



\##  Objectives

\- Build a secure segmented network

\- Simulate attacker behavior from a rogue workstation

\- Block unauthorized access using ACLs

\- Capture evidence of malicious traffic

\- Document the incident 



\---



\##  Tools Used

\- Cisco Packet Tracer

\- Router ACLs

\- VLAN Segmentation

\- Packet Capture Simulation

\- Network Traffic Analysis





\---



\##  Network Architecture



\### VLAN Design



| VLAN | Purpose | Network |

|------|---------|---------|

| 10 | Users | 192.168.10.0/24 |

| 20 | Servers | 192.168.20.0/24 |

| 30 | Admin | 192.168.30.0/24 |

| 99 | Attacker | 192.168.99.0/24 |



\---



\##  Network Topology



!\[Topology](screenshots/01\_topology.png)



\---



\##  Switch VLAN Configuration



!\[VLAN Config](screenshots/02\_vlan\_config.png)



\---



\##  Router Inter-VLAN Routing



!\[Router Config](screenshots/03\_router\_subinterfaces.png)



\---



\##  Firewall ACL Rules



The router was configured to:

\- Block attacker VLAN from accessing server VLAN

\- Block attacker VLAN from accessing admin VLAN

\- Permit legitimate business traffic



\- Block user VLAN from accessing admin VLAN

\- Permit legitimate business traffic







!\[ACL Rules](screenshots/04\_acl\_rules.png)



\---



\##  Legitimate Access Test



Normal users can successfully access the internal server.



!\[User Access](screenshots/05\_user\_to\_server\_success.png)



\---



\##  Attack Simulation



The attacker workstation attempted to access protected resources and was blocked.



!\[Blocked Attack](screenshots/06\_kali\_blocked\_ping.png)



\---



\##  ACL Log Evidence



Access control lists recorded denied traffic attempts.



!\[ACL Logs](screenshots/07\_acl\_hit\_counter.png)



\---



\##  Packet Analysis



Traffic was analyzed in simulation mode to identify:

\- source IP

\- destination IP

\- blocked packets





!\[Packet Capture](screenshots/08\_packet\_capture.png)



\---



\##  Server Access Validation



Users could still access the internal web server.



!\[Web Access](screenshots/09\_server\_http\_access.png)



\---



\##  Incident Summary



\### Threat Type

Unauthorized internal reconnaissance attempt



\### Source

192.168.99.10



\### Target

192.168.20.10



\### Detection Method

ACL deny logs and packet analysis



\### Response

Traffic blocked by segmentation firewall policy



\---



\##  Security Concepts Demonstrated

\- Network segmentation

\- Least privilege access

\- Internal threat detection

\- Traffic monitoring

\- Incident response workflow

\- Firewall policy enforcement



\---



\##  Project Files



| File | Description |

|------|-------------|

| `README.md` | Project overview |

| `lab-guide.md` | Build instructions |

| `configuration.txt` | Router \& switch commands |

| `incident-report.md` | SOC analysis report |

| `screenshots/` | Evidence images |



\---



\##  Key Learning Outcomes

This lab improved my understanding of:

\- Enterprise network defense

\- SOC investigation workflow

\- Traffic analysis

\- Threat containment

\- Documentation for incident response



\---



\##  Future Improvements

Possible future upgrades:

\- Real Kali Linux integration

\- Wireshark live capture

\- Snort IDS alerts

\- Wazuh SIEM integration

\- Syslog central logging



\---



\##  Author

\*\*DAVID ITUNU FAJUYI\*\*  

Cybersecurity security Enthusiast



\---

