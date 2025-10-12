# Splunk Labs — Hands-on SIEM Experience

This section documents all my hands-on work with **Splunk Enterprise** and **Splunk Universal Forwarder**, focusing on log ingestion, search, alerting, and dashboard creation.

---

## 🧠 Overview
Splunk is a Security Information and Event Management (SIEM) platform used to collect, index, and analyze machine data from various sources.  
Here, I practice essential SOC analyst skills — from setup to detection and response.

---

## 🔧 Tools & Environment
- **Splunk Enterprise (Free version)** installed on Windows VM  
- **Universal Forwarder** for sending logs  
- **Kali Linux / Ubuntu** as log sources  
- **VirtualBox** for network isolation and VM management  
- Network Mode: Internal + NAT (dual network setup for analysis)

---

## 🧩 Labs Completed
| # | Lab Title | Description | Tools Used | Outcome |
|---|------------|-------------|-------------|----------|
| 1 | Splunk Setup & Configuration | Installed Splunk Enterprise on Windows and connected Universal Forwarder from Linux. | Splunk, Universal Forwarder | Logs successfully indexed and visible on Splunk Search Head |
| 2 | Search Processing Language (SPL) Basics | Performed searches, filters, and data correlation using SPL commands (`stats`, `table`, `eval`, etc.). | Splunk | Understood how to query indexed logs and extract insights |
| 3 | Dashboard & Visualization | Built custom dashboards to visualize login events, network scans, and traffic patterns. | Splunk Dashboard Studio | Created real-time SOC-style dashboards |
| 4 | Detection Rules & Alerts | Configured alert rules to detect suspicious activity (failed logins, scanning behavior). | Splunk Alerting | Automated email/console notifications for triggered alerts |

---

## 🧪 Example SPL Queries

```spl
# List top 10 IP addresses by failed SSH login attempts
index=syslog sourcetype=secure "Failed password"
| stats count by src_ip
| sort -count
| head 10
```

```spl
# Track login activity over time
index=auth sourcetype=linux_secure action=success
| timechart span=1h count by user
```

---

## 📷 Screenshots
All screenshots of installations, dashboards, and detections are stored in the `/Splunk-Labs/screenshots` folder.

---

## 📝 Key Takeaways
- Learned how to deploy and configure Splunk in a lab environment.
- Understood SPL for searching and correlating logs.
- Built dashboards for SOC-style monitoring.
- Created detection alerts for incident response workflows.

---

## 🔗 Next Steps
- Integrate more data sources (Windows Event Logs, Sysmon).
- Build detection correlation rules across multiple hosts.
- Automate log forwarding with Python scripts.

---

> *This folder is part of my cybersecurity portfolio showcasing practical SIEM and SOC analysis skills.*
