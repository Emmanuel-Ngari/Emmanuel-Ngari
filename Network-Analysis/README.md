# 🧠 Network Analysis Lab

This project focuses on analyzing network traffic using Wireshark, Nmap, and tcpdump to identify hosts, open ports, and suspicious activities. It demonstrates practical skills in packet capture, filtering, and threat detection — essential for any SOC Analyst.

---

## 🎯 Objectives
- Identify live hosts and analyze network topology.
- Capture and inspect network packets.
- Perform comprehensive port and service scans using Nmap.
- Analyze captured data for possible anomalies or threats.
- Document findings and summarize security insights.

---

## 🧰 Tools & Technologies
- **Wireshark** – Packet capture and analysis.
- **Nmap** – Network discovery and vulnerability scanning.
- **tcpdump** – Command-line packet capture utility.
- **Kali Linux / Ubuntu** – Lab environment for testing.
- **VirtualBox Internal Network** – Isolated network setup for analysis.

---

## ⚙️ Workflow
1. **Host Discovery:**  
   Used `nmap -sn 192.168.56.0/24` to identify active hosts.

2. **Port Scanning:**  
   Conducted a full TCP scan using `nmap -p- -sS -T4` to enumerate open ports.

3. **Service Enumeration:**  
   Verified service versions with `nmap -sV` to detect running applications.

4. **Traffic Capture:**  
   Captured live packets using Wireshark and `tcpdump` to analyze traffic patterns.

5. **Filtering & Analysis:**  
   Applied Wireshark filters (`tcp.port==80`, `ip.addr==192.168.56.10`) to focus on HTTP and host-specific activity.

---

## 📸 Screenshots
Screenshots from this lab are stored in the `screenshots` folder:
- Host discovery and port scans.
- Wireshark filtered sessions.
- Protocol analysis and summary.

---

## 📄 Report
Detailed documentation of the experiment can be found in:
[`Network_Analysis_Report.md`](./Network_Analysis_Report.md)

---

## 🧩 Key Takeaways
- Enhanced understanding of network behavior and communication flow.
- Improved ability to identify suspicious packets and host activity.
- Demonstrated proficiency in Nmap and Wireshark usage for network reconnaissance.
