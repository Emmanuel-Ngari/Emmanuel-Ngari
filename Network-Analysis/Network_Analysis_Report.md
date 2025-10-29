# 🛰️ Network Analysis Report

**Analyst:** Emmanuel Ngari  
**Tool Used:** Wireshark  
**Environment:** VirtualBox Internal Network (192.168.56.0/24)  
**Date:** October 2025  

---

## Overview
The purpose of this analysis was to inspect and understand network communication within a controlled virtual lab environment. Using **Wireshark**, live packet captures were conducted to identify protocols in use, monitor traffic flow, and assess potential anomalies or signs of compromise.

The activity focused on capturing packets between Windows, Ubuntu, and Kali Linux virtual machines on the internal network.

---

## Methodology
1. **Network Interface Identification:**  
   The correct adapter (VirtualBox Host-Only Adapter) was selected to monitor internal traffic among lab machines.  

2. **Packet Capture Setup:**  
   Wireshark was launched with administrative privileges, and a live capture session was initiated to observe active communication between hosts.  

3. **Traffic Filtering:**  
   Display filters such as:
   - `ip.addr == 192.168.56.10`  
   - `tcp.port == 3389`  
   - `http`, `icmp`, and `dns`  
   were applied to isolate relevant packets and sessions.  

4. **Traffic Inspection:**  
   Source and destination IPs, protocol types, and TCP flags were analyzed to understand session establishment, request-response flow, and termination patterns.  

5. **Export and Documentation:**  
   Screenshots of key captures, including RDP, ICMP, and TCP streams, were saved under `/screenshots` for reference.

---

## Findings
- Detected **TCP and RDP communications** between 192.168.56.10 (attacker machine) and 192.168.56.20 (Windows target).  
- **ICMP packets** confirmed successful connectivity and network reachability.  
- No plaintext credentials or unencrypted sensitive data were captured.  
- **ARP packets** validated active communication and address resolution within the subnet.  

---

## Analysis Summary
Wireshark enabled deep visibility into packet-level network communication. The data captured confirmed expected traffic between virtual machines. Patterns such as ping sweeps, port scans, and RDP connections were consistent with testing activity observed during vulnerability assessment.

---

## Conclusion
This network analysis exercise successfully demonstrated how to:
- Capture live traffic in a secure test environment.  
- Apply effective filters for meaningful inspection.  
- Identify common protocol behaviors and communication flows.  

The experiment provided foundational hands-on experience in packet analysis — an essential skill for cybersecurity analysts during threat hunting, intrusion detection, and forensic review.

---

## Attachments
- `/screenshots` — Wireshark traffic captures and analysis visuals.  
- `/reports` — Contains this detailed Network Analysis Report.
