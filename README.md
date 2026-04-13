# Network Traffic Monitoring Lab (Wireshark + Snort)

## Overview
This project demonstrates a network security lab where I monitored and analyzed network traffic and detected attacks using Wireshark and Snort.

The goal of this lab is to simulate real-world attack scenarios and understand how security tools detect malicious activity at the network level.

---

## Lab Setup

The lab consists of three virtual machines running on VMware:

- Attacker: Kali Linux (192.168.119.131)
- Monitor: Ubuntu (192.168.119.132)
  - Tools installed: Wireshark, Snort
- Victim: Windows Machine (192.168.119.130)

All systems are connected in the same subnet (192.168.119.0/24).

---

## Tools Used

- Wireshark – Packet capture and traffic analysis  
- Snort – Intrusion Detection System (IDS)  
- Nmap – Network scanning tool  
- VMware – Virtual lab environment  

---

## Attacks Simulated

### 1. ICMP Ping Detection
- Generated traffic using:
  ```bash
  ping 192.168.119.132
Captured ICMP packets in Wireshark
Created a Snort rule to detect ICMP traffic

Result: Snort successfully detected ICMP ping activity

2. SYN Scan Detection
Performed SYN scan using:nmap -sS -Pn 192.168.119.132
Observed SYN packets in Wireshark
Used Snort to detect scanning behavior

Result: Snort generated multiple alerts indicating SYN scan activity

Analysis
ICMP traffic shows communication between attacker and target
SYN scan sends multiple connection requests to different ports
Wireshark was used to filter and analyze packets
Snort detected both ICMP and SYN-based attacks in real time

Key Learnings
Understanding of TCP/IP and ICMP protocols
Packet-level analysis using Wireshark
Writing and testing Snort detection rules
Identifying network attacks such as port scanning
Building a basic SOC-style monitoring environment

Conclusion
This lab demonstrates how network monitoring and IDS tools can detect and analyze attacks in real time.
It provides hands-on experience relevant for:
SOC Analyst roles
Cybersecurity Analyst positions
Network Security roles
