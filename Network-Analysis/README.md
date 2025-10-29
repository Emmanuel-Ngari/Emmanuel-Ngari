# 🧠 Network Analysis Lab

This project focuses on discovering, scanning, and analyzing hosts across a simulated enterprise network using **Nmap**, **Wireshark**, and **tcpdump**.  
It demonstrates how to map a network, identify potential attack surfaces, and capture packets for in-depth inspection.

---

## 📋 Objectives
- Identify live hosts using ICMP and ARP discovery.
- Perform comprehensive TCP and UDP port scans.
- Detect service versions and operating systems.
- Capture and analyze packets using Wireshark and tcpdump.
- Generate a detailed vulnerability summary report.

---

## 📂 Folder Structure
- **Network_Analysis_Report.md** → Detailed report of findings and recommendations.  
- **reports/** → Raw scan outputs (`.txt` files).  
- **screenshots/** → Visuals from Wireshark, Nmap, and terminal sessions.  

---

## 🧩 Tools Used
- **Nmap** — Host discovery, port scanning, and OS detection.  
- **Wireshark** — Deep packet inspection and traffic filtering.  
- **tcpdump** — CLI-based capture and protocol analysis.  

---

## 🧾 Summary
This lab simulated a small corporate network, identifying open RDP (3389) and SMB (445) services.  
Captured packets were analyzed to detect cleartext credentials and unencrypted protocols.  
Recommendations included enforcing **TLS encryption**, **restricting RDP access**, and **enabling firewalls** on all hosts.

---

**Author:** Emmanuel Patrick Ngari  
**Date:** $(date +"%Y-%m-%d")
