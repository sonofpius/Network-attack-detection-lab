#  Incident Report – Unauthorized Internal Reconnaissance Attempt



## Incident Information



| Field | Details |

|-------|---------|

| Incident ID | IR-2026-001 |

| Date | 17 April 2026 |

| Analyst | Your Name |

| Severity | Medium |

| Status | Resolved |



---



##   Summary



A simulated attacker workstation located on a restricted VLAN attempted to access protected internal resources within the network.



The firewall access control list (ACL) successfully blocked the unauthorized traffic, preventing access to the server and management networks.



The event was detected through:

- ACL deny logs

- Packet capture analysis

- Connectivity testing



---



##  Environment Details



| VLAN | Purpose | Subnet |

|------|---------|--------|

| VLAN 10 | Users | 192.168.10.0/24 |

| VLAN 20 | Servers | 192.168.20.0/24 |

| VLAN 30 | Admin | 192.168.30.0/24 |

| VLAN 99 | Attacker | 192.168.99.0/24 |



---



##  Incident Description



A workstation configured as an attacker system attempted to:



- Ping the internal server

- Access the management network

- Enumerate accessible services



The source device was placed in:



```text

192.168.99.10

