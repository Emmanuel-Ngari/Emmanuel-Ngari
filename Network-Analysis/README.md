# Network Analysis — Wireshark & Packet Investigation Labs

This section documents my hands-on work with **Wireshark**, focusing on network packet capture, protocol analysis, and traffic inspection — core skills for a Security Operations Center (SOC) analyst.

---

## 🧠 Overview
Wireshark is an open-source network protocol analyzer that helps cybersecurity analysts inspect network packets in real time or from captured files (PCAPs).  
Through these labs, I practiced identifying network anomalies, understanding protocols, and filtering traffic for incident response.

---

## 🔧 Tools & Environment
- **Wireshark** (installed on Kali Linux)
- **Ubuntu VM** for network simulation
- **Windows VM** for generating normal and suspicious traffic
- **VirtualBox** — dual-network setup:
  - Internal Network (VM-to-VM traffic)
  - NAT (Network 1 – Internet access)
- **Command-line utilities:** `ping`, `netcat`, `curl`, `traceroute`

---

## 🧩 Labs Completed

| # | Lab Title | Description | Tools Used | Outcome |
|---|------------|-------------|-------------|----------|
| 1 | Network Interface Discovery | Identified active interfaces using `ip addr` and configured correct interface in Wireshark | Kali Linux | Learned to distinguish NAT vs. Internal Network interfaces |
| 2 | Packet Capture Basics | Captured live traffic using Wireshark and saved PCAP files for analysis | Wireshark | Understood how packets are captured and stored |
| 3 | Protocol Analysis | Filtered and analyzed ICMP, TCP, UDP, and DNS traffic using display filters | Wireshark | Interpreted packet headers and payloads |
| 4 | Traffic Filtering | Practiced Wireshark display filters: `ip.addr`, `tcp.port`, `icmp` etc. | Wireshark | Gained precision in isolating relevant packets |
| 5 | Ping Flood Simulation | Simulated ICMP ping traffic between VMs and analyzed patterns | Kali Linux, Ubuntu | Detected packet floods and latency variation |
| 6 | Threat Detection Simulation | Captured suspicious traffic (failed logins, port scans) | Wireshark, Nmap | Learned to identify abnormal traffic signatures |

---

## 🔍 Example Display Filters

```wireshark
# Capture only ICMP traffic
icmp

# Capture DNS queries and responses
udp.port == 53

# Filter packets from a specific host
ip.addr == 192.168.56.10

# Track HTTP traffic
tcp.port == 80 || tcp.port == 443
```

---

## 🧪 Example Lab Exercise

**Objective:** Detect suspicious network activity  
**Action:** Used Nmap to scan a subnet from Kali Linux  
**Command:**
```bash
nmap -sS 192.168.56.0/24
```
**Analysis:**  
Captured packets in Wireshark showed multiple SYN requests without replies → indicating a potential SYN scan.  

---

## 📷 Screenshots
All screenshots of the network captures and analyses are stored in:
```
/Network-Analysis/screenshots/
```

---

## 📝 Key Takeaways
- Learned to capture and analyze packets safely in a lab environment.  
- Understood protocol structures (Ethernet, IP, TCP, UDP, ICMP).  
- Applied filters to isolate traffic during investigations.  
- Practiced identifying indicators of reconnaissance or scanning.  

---

## 🔗 Next Steps
- Capture real-world network logs and compare with simulated data.  
- Learn **tshark** for command-line packet analysis.  
- Integrate PCAP analysis into **Splunk** or **ELK Stack**.

---

> *This folder is part of my cybersecurity portfolio showcasing practical network monitoring and packet-analysis skills.*
