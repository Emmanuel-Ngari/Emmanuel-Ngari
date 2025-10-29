# 🧠 Network Analysis Lab
This lab focuses on discovering, scanning, and analyzing hosts across a simulated network using **Nmap**, **Wireshark**, and **tcpdump**.  
It provides detailed visibility into open ports, services, and vulnerabilities within the internal lab environment.

## 📋 Objectives
- Identify live hosts on the subnet.
- Perform full TCP and targeted scans.
- Analyze captured traffic and service banners.
- Document findings and recommendations.

## 📂 Folder Structure
- **Network_Analysis_Report.md** → Comprehensive findings and summary.  
- **reports/** → Contains raw `.txt` outputs (Nmap scans, vulnerability checks, etc.).  
- **screenshots/** → Visual evidence from Wireshark, Nmap, and terminal sessions.

## 🧩 Tools Used
- **Nmap** — Host discovery, port scanning, service detection.  
- **Wireshark** — Deep packet inspection and analysis.  
- **tcpdump** — CLI-based packet capture.  

## 🧾 Summary
This lab validated RDP (3389) exposure and SMB enumeration, revealing potential brute-force and misconfiguration risks.  
Mitigation included access restrictions, NLA enforcement, and firewall tuning.

---
**Author:** Emmanuel Patrick Ngari  
**Date:** $(date --iso-8601=seconds)
