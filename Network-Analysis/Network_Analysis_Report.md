# 🧠 Network Analysis — Detailed Report
## Overview
**Date:** $(date --iso-8601=seconds)
**Analyst:** Emmanuel Patrick Ngari
**Environment:** Kali (analyst), Windows 10 (target), Ubuntu (infrastructure) — Internal + NAT
---
## Scope
- Host discovery on 192.168.56.0/24
- Full TCP port scan and service/version enumeration
- RDP and SMB specific checks
- Packet captures (Wireshark/tcpdump) for traffic analysis
---
## Methodology
1. Recon: nmap -sn
2. Port discovery: nmap -p- -sS
3. Service detection: nmap -sV -O
4. NSE vulnerability checks: nmap --script vuln, --script rdp*, --script smb-vuln*
5. Packet capture: tcpdump -w and Wireshark analysis
---
## Findings (summary)
- Hosts discovered: 192.168.56.20, 192.168.56.30, 192.168.56.10
- Open service: RDP (3389) on 192.168.56.20
- SMB ports (139/445) filtered
- NSE check shows RDP supports CredSSP, RDSTLS; Windows version 10.0.19041
---
## Evidence / Artifacts
- Reports: host_discovery.txt, full_tcp_scan.txt, service_version_3389.txt, vuln_scan_nse.txt, rdp_specific.txt, smb_vulns.txt
- Screenshots and packet captures in screenshots/
---
## Risk & Recommendations
- RDP Exposed: Restrict access to trusted IPs, enable NLA, enforce complex passwords.
- Firewall Hardening: Review and block unnecessary inbound traffic.
- Monitoring: Implement alerting for repeated failed logins and unauthorized RDP attempts.
---
## Next Steps
- Perform brute-force simulation in lab to validate SIEM detection.
- Forward Sysmon logs to Splunk for deeper endpoint telemetry.
- Conduct rescans post-mitigation for validation.
