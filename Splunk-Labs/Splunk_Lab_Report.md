# 🧩 Splunk Lab — Detailed Report
## Overview
**Date:** $(date --iso-8601=seconds)
**Analyst:** Emmanuel Patrick Ngari
**Environment:** Splunk Enterprise (Ubuntu) + Universal Forwarder (Windows 10)
---
## Objectives
- Install and configure Splunk Enterprise and Universal Forwarder.
- Ingest and analyze Windows Event Logs.
- Create actionable dashboards and alerts for SOC monitoring.
---
## Implementation Summary
1. Installed Splunk Enterprise on Ubuntu (:8000).
2. Enabled receiving on port 9997.
3. Installed Universal Forwarder on Windows.
4. Configured outputs.conf to send data to 192.168.56.30:9997.
5. Forwarded logs: Security, System, Application.
6. Verified logs with index=windows EventCode=4625.
---
## Key SPL Queries
- Failed Logins: index=windows EventCode=4625 | stats count by Account_Name, src_ip
- Successful Logins: index=windows EventCode=4624 | stats count by Account_Name, src_ip
- RDP Brute-Force Detection: index=windows EventCode=4625 | stats count by src_ip | where count > 10
---
## Dashboards & Alerts
- Dashboard: Failed vs Successful Logins, Top Source IPs, Brute Force Trends.
- Alert: Notify when >10 failed logins from same IP within 5 mins.
---
## Findings
- Forwarder successfully transmitted logs to Splunk index.
- Detected failed login attempts and validated visibility on dashboard.
- Encountered and fixed forwarder connectivity issue.
---
## Recommendations
- Enable SSL for data forwarding.
- Integrate Sysmon logs for process monitoring.
- Expand dashboard to map detections to MITRE ATT&CK.
---
## Next Steps
- Parse EventCode 4688 (Process Creation) from Sysmon.
- Build MITRE-aligned dashboard.
- Export Splunk dashboards as JSON to dashboards/ folder for portfolio.
