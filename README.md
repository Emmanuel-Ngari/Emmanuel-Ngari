# Hi, I'm Emmanuel Ngari

### Cybersecurity | Purple Team | SOC Operations | Detection Engineering

I am a cybersecurity practitioner focused on building practical capability across both **offensive and defensive security**, with a long-term direction toward **Purple Team operations, SOC analysis, detection engineering, threat hunting, and incident response**.

I believe strong cybersecurity professionals should understand both sides of an attack:

> Understand how the attacker operates, understand what the defender can see, then improve detection and response.

---

##  Connect With Me

[![GitHub](https://img.shields.io/badge/GitHub-Emmanuel--Ngari-black?logo=github)](https://github.com/Emmanuel-Ngari)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Emmanuel%20Ngari-blue?logo=linkedin)](https://www.linkedin.com/in/emmanuel-ngari/)
[![Email](https://img.shields.io/badge/Email-emmanuelpatrick377%40gmail.com-red?logo=gmail)](mailto:emmanuelpatrick377@gmail.com)

---

# Cybersecurity Focus

My current technical focus includes:

- Purple Team Operations
- Security Operations Center (SOC)
- Detection Engineering
- Threat Hunting
- SIEM Monitoring
- Incident Investigation
- Windows Security
- Linux Security
- Active Directory Security
- Network Security
- Firewall Engineering
- Intrusion Detection
- Offensive Security Fundamentals

---

#  Featured Project

## Enterprise Purple Team Cybersecurity Home Lab

My flagship project is a cybersecurity home lab that evolved from a simple three-machine environment into a segmented enterprise-style Purple Team platform.

🔗 **Repository:**  
[Cybersecurity Home Lab](https://github.com/Emmanuel-Ngari/cybersecurity-homelab)

The project began with:

- Kali Linux
- Windows
- Ubuntu Server
- Nmap
- SSH
- Hydra
- fail2ban

It later evolved into a complete six-zone architecture with:

- OPNsense firewalling
- network segmentation
- Wazuh SIEM
- endpoint monitoring
- Suricata IDS
- Active Directory
- Group Policy
- Linux auditd
- Windows Sysmon
- PowerShell logging
- Nginx monitoring
- DMZ security
- custom detection engineering
- Purple Team validation

---

#  Final Lab Architecture

| Security Zone | Network | Primary System | Purpose |
|---|---|---|---|
| REDNET | `10.10.10.0/24` | LAB-KALI-01 | Offensive Security |
| CORPNET | `10.10.20.0/24` | LAB-WIN-01 | Corporate Workstation |
| SERVERNET | `10.10.30.0/24` | LAB-UBUNTU-01 | Internal Linux Server |
| SOCNET | `10.10.40.0/24` | LAB-SIEM-01 | Security Operations |
| ADNET | `10.10.50.0/24` | LAB-DC-01 | Active Directory |
| DMZ | `10.10.60.0/24` | LAB-DMZ-01 | Public-Facing Services |

Central routing and firewalling are handled by:

**LAB-FW-01 — OPNsense**

---

#  What I Built

## Network Security

- Six-zone network segmentation
- OPNsense firewall
- Least-privilege access control
- Inter-zone filtering
- Logged security boundaries
- Controlled Internet access
- Isolated REDNET attacker network
- Protected Active Directory network
- Dedicated DMZ

---

## Security Monitoring

- Wazuh SIEM
- Centralized endpoint monitoring
- Windows Security Event monitoring
- Linux security monitoring
- OPNsense firewall telemetry
- Suricata IDS integration
- Nginx application monitoring

---

## Windows Security

Implemented:

- Sysmon
- PowerShell Script Block Logging
- PowerShell Module Logging
- PowerShell transcription
- advanced Windows auditing
- Microsoft Defender monitoring
- Windows Firewall telemetry
- File Integrity Monitoring

---

## Linux Security

Implemented:

- auditd
- SSH monitoring
- fail2ban
- Wazuh Agent monitoring
- Linux account-change detections

---

## Active Directory

Built the domain:

`cyberlab.internal`

using:

- Windows Server 2025
- Active Directory Domain Services
- DNS
- Kerberos
- LDAP
- Global Catalog
- Organizational Units
- role-based security groups
- privileged-account separation
- domain-joined Windows workstation
- Group Policy
- Domain Controller monitoring

---

## Network IDS

Deployed Suricata on OPNsense.

Final telemetry path:

`Suricata → OPNsense Remote Logging → rsyslog → JSON → Wazuh`

This provides network-level intrusion detection alongside endpoint telemetry.

---

## DMZ Security

Built a dedicated Ubuntu/Nginx DMZ server with:

- segmented DMZ network
- Wazuh monitoring
- Nginx access/error log monitoring
- REDNET HTTP exposure
- restricted SSH administration
- Ed25519 key authentication
- password authentication disabled
- root SSH login disabled

---

#  Detection Engineering

I have built and validated detections from multiple telemetry sources.

| Detection | Rule |
|---|---|
| Linux User Creation | `100200` |
| Linux User Deletion | `100201` |
| OPNsense Firewall Correlation | `87702` |
| Suricata IDS Alert | `86601` |
| Nginx Web Event | `31101` |

My detection workflow follows:

`Generate Activity → Collect Telemetry → Decode → Detect → Investigate → Improve → Retest`

---

#  Purple Team Methodology

My lab has now transitioned from infrastructure building into realistic Purple Team operations.

Each scenario follows:

    Attack
       ↓
    Telemetry
       ↓
    Detection
       ↓
    SOC Investigation
       ↓
    Gap Analysis
       ↓
    Detection Improvement
       ↓
    Retest

Current and future scenarios include:

- Reconnaissance
- Credential attacks
- PowerShell abuse
- Privilege escalation
- Persistence
- Lateral movement
- Active Directory abuse
- Web attacks
- Threat hunting
- Incident response
- Detection-gap analysis

---

#  Technologies & Tools

## SIEM / Detection

![Wazuh](https://img.shields.io/badge/Wazuh-SIEM-blue)
![Sysmon](https://img.shields.io/badge/Sysmon-Windows%20Telemetry-blue)
![Suricata](https://img.shields.io/badge/Suricata-IDS-red)
![auditd](https://img.shields.io/badge/auditd-Linux%20Auditing-orange)

## Networking & Infrastructure

![OPNsense](https://img.shields.io/badge/OPNsense-Firewall-orange)
![VirtualBox](https://img.shields.io/badge/VirtualBox-Virtualization-blue)
![Nginx](https://img.shields.io/badge/Nginx-Web%20Server-green)

## Operating Systems

![Kali Linux](https://img.shields.io/badge/Kali%20Linux-Offensive%20Security-blue)
![Ubuntu](https://img.shields.io/badge/Ubuntu-Linux-orange)
![Windows](https://img.shields.io/badge/Windows-Endpoint-blue)
![Windows Server](https://img.shields.io/badge/Windows%20Server-Active%20Directory-blue)

## Enterprise Security

![Active Directory](https://img.shields.io/badge/Active%20Directory-Identity%20Security-blue)
![Group Policy](https://img.shields.io/badge/Group%20Policy-Windows%20Security-blue)

## Security Testing

![Nmap](https://img.shields.io/badge/Nmap-Network%20Reconnaissance-lightgrey)
![Hydra](https://img.shields.io/badge/Hydra-Authentication%20Testing-red)
![fail2ban](https://img.shields.io/badge/fail2ban-Linux%20Defense-green)

---

#  Current Development Path

I am building toward professional Purple Team capability through a structured combination of offensive and defensive security.

## Offensive Development

- reconnaissance
- enumeration
- exploitation fundamentals
- credential attacks
- Active Directory attack paths
- adversary behaviour

## Defensive Development

- SIEM
- endpoint telemetry
- detection engineering
- firewall analysis
- IDS
- threat hunting
- incident investigation

## Purple Team Integration

- MITRE ATT&CK-aligned simulations
- telemetry validation
- detection-gap analysis
- defensive tuning
- retesting

---

#  Certifications & Training

- Google Cybersecurity Professional Certificate
- Hands-on cybersecurity lab development
- Practical cybersecurity training focused on security operations

My certification strategy is role-based.

I prioritize certifications and training that strengthen:

**Networking → Defensive Security → Offensive Security → Detection Engineering → Purple Team Operations**

rather than collecting unrelated certifications.

---

#  Current Project Status

## Infrastructure

✅ Six-zone network architecture  
✅ OPNsense firewall  
✅ Wazuh SIEM  
✅ Windows endpoint monitoring  
✅ Linux endpoint monitoring  
✅ Suricata IDS  
✅ Active Directory  
✅ Group Policy  
✅ Domain Controller monitoring  
✅ DMZ  
✅ Nginx monitoring  
✅ SSH hardening  
✅ Detection engineering  
✅ Final architecture validation  

## Current Focus

🔄 SOC investigations  
🔄 Purple Team scenarios  
🔄 MITRE ATT&CK mapping  
🔄 Detection engineering  
🔄 Threat hunting  
🔄 Active Directory security testing  
🔄 Incident response  

---

#  Project Documentation

The Cybersecurity Home Lab repository contains dedicated documentation for:

- Architecture
- Networking
- Firewall Engineering
- Virtual Machines
- Active Directory
- Blue Team Monitoring
- Detection Engineering
- Suricata Integration
- Linux Monitoring
- Troubleshooting
- Build Journal
- Purple Team Scenarios

The documentation preserves both:

- the final architecture
- the engineering journey that produced it

including troubleshooting, design changes, failed approaches, and final validation.

---

#  Career Direction

I am working toward roles including:

- SOC Analyst
- Security Analyst
- Detection Engineer
- Threat Hunter
- Incident Response Analyst
- Purple Team Analyst

My long-term objective is to develop deep capability in both offensive and defensive cybersecurity so I can understand attacks from both perspectives and improve how organizations detect and respond to threats.

---

#  Security Philosophy

I do not consider a security control complete just because it was installed.

I want to know:

**Does it work?**

**Can I test it?**

**Can I see the telemetry?**

**Can the SOC detect it?**

**Can an analyst investigate it?**

**Can the detection be improved?**

That mindset drives my cybersecurity projects.

---

#  Connect With Me

- GitHub: [github.com/Emmanuel-Ngari](https://github.com/Emmanuel-Ngari)
- LinkedIn: [linkedin.com/in/emmanuel-ngari](https://www.linkedin.com/in/emmanuel-ngari/)
- Email: [emmanuelpatrick377@gmail.com](mailto:emmanuelpatrick377@gmail.com)

---

### Emmanuel Ngari

**Cybersecurity | Purple Team | SOC Operations | Detection Engineering**

> Building the attacker mindset and defender visibility required to understand security from both sides.
