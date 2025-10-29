# 🧠 Splunk Lab Report

**Analyst:** Emmanuel Ngari  
**Tool Used:** Splunk (Simulated Environment)  
**Date:** October 2025  

---

## Overview
This lab focused on understanding **log collection, analysis, and event correlation** using Splunk in a simulated cybersecurity environment. The objective was to demonstrate how log data from Windows and Linux systems can be ingested, queried, and visualized to identify system activity patterns, authentication attempts, and potential threats.

---

## Methodology
1. **Log Preparation:**  
   Windows and Linux logs were organized into `/logs` for indexing. This included:
   - Windows Security, System, and Application event logs.  
   - Linux authentication and syslog data.

2. **Data Indexing (Simulated):**  
   Logs were conceptually ingested into Splunk using indexes such as:index=windows OR index=linux
 This simulated event segregation by operating system.

3. **Query and Search Analysis:**  
Common Splunk SPL (Search Processing Language) queries were used:
- `index=windows EventCode=4624` → Successful logins  
- `index=windows EventCode=4625` → Failed logins  
- `index=linux "sshd"` → SSH login activity  
- `index=* error OR fail` → General system or application failures  

4. **Dashboard and Visualization Design:**  
Interactive dashboards were conceptually created to display:
- Login attempts over time  
- Failed vs successful logins  
- Event trends by host  
- Top error categories  

---

## Findings
- Multiple simulated failed login events (EventCode 4625) highlighted unauthorized login attempts.  
- Successful logins (EventCode 4624) aligned with authorized administrative sessions.  
- SSH activity logs revealed normal Linux user sessions with no root compromise.  
- Identified recurring system warnings, useful for early detection of performance issues.  

---

## Analysis Summary
This Splunk lab demonstrated how centralized log aggregation helps analysts identify suspicious activities across multiple hosts. The ability to filter, visualize, and interpret event codes provides strong insights into user behavior and system health.

The lab also emphasized the value of **data correlation** — linking events across systems to spot attack patterns or operational issues.

---

## Conclusion
The Splunk simulation successfully replicated a real-world SIEM workflow, covering:
- Log ingestion and indexing.  
- Query formulation using SPL.  
- Event correlation and visualization through dashboards.  

This exercise strengthened core skills for Security Operations Center (SOC) environments, enhancing the understanding of incident detection, alert creation, and data-driven security analysis.

---

## Attachments
- `/logs` — Sample log datasets.  
- `/dashboards` — Conceptual dashboard files and templates.  
- `/screenshots` — Visuals of Splunk queries and analysis results.  
