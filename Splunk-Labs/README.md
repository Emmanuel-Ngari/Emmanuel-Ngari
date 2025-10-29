# 🧩 Splunk Security Monitoring Lab

This project demonstrates the use of **Splunk Enterprise** and **Universal Forwarder** for centralized log collection, correlation, and real-time threat detection across Windows and Linux environments.

---

## 📋 Objectives
- Deploy Splunk Enterprise and connect Universal Forwarders.  
- Collect and index Windows Event Logs (Security, System, Application).  
- Detect brute-force login attempts using correlation searches.  
- Create dashboards, visualizations, and alert workflows.  

---

## 📂 Folder Structure
- **Splunk_Lab_Report.md** → Step-by-step documentation of setup and analysis.  
- **logs/** → Raw log exports and data samples.  
- **dashboards/** → JSON exports of visual dashboards.  
- **screenshots/** → Images of dashboards, alert configurations, and search results.  

---

## 🧩 Tools Used
- **Splunk Enterprise** — SIEM for log analysis and visualization.  
- **Universal Forwarder** — Lightweight log collector for endpoints.  
- **MITRE ATT&CK** — Framework mapping for analytical coverage.  

---

## 🧾 Summary
Successfully identified multiple failed login events (**EventCode 4625**) and visualized attack patterns by username, IP, and time range.  
Created automated alerts for brute-force attempts within a 5-minute detection window.  
Next iteration integrates **Sysmon**, **Windows Defender logs**, and **MITRE ATT&CK-aligned dashboards**.

---

**Author:** Emmanuel Patrick Ngari  
**Date:** $(date +"%Y-%m-%d")
