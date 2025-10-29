# 🧩 Splunk Security Monitoring Lab
This lab demonstrates **log ingestion, correlation, and alerting** using Splunk Enterprise and Universal Forwarder in a Windows and Linux hybrid environment.

## 📋 Objectives
- Set up Splunk Enterprise and Forwarder.
- Ingest Windows Event Logs (Security, System, Application).
- Detect failed logins and brute-force attempts.
- Build real-time dashboards and alerts.

## 📂 Folder Structure
- **Splunk_Lab_Report.md** → Detailed step-by-step report.  
- **logs/** → Raw data and event exports from Splunk searches.  
- **screenshots/** → Dashboard visualizations and alert configurations.  
- **dashboards/** → JSON exports of dashboards (for portfolio).

## 🧩 Tools Used
- **Splunk Enterprise** — Central SIEM and dashboarding tool.  
- **Windows Universal Forwarder** — Log shipping agent.  
- **MITRE ATT&CK Mapping** — For analytical alignment.

## 🧾 Summary
Successfully detected multiple failed login events (EventCode 4625) and visualized attempts per account and IP.  
Built custom alerts to detect brute-force trends within a 5-minute window.  
Next phase integrates **Sysmon logs** and **MITRE-aligned dashboards**.

---
**Author:** Emmanuel Patrick Ngari  
**Date:** $(date --iso-8601=seconds)
