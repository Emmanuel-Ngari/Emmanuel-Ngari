# Emmanuel Ngari

Cybersecurity | Network Security | Blue Team | Red Team | Homelab Engineering

I am building practical cybersecurity skills through hands-on labs, network engineering, Linux and Windows administration, defensive security, ethical hacking, threat detection, and incident response.

My goal is to understand cybersecurity from both the attacker and defender perspectives by designing realistic environments, securing them, testing them, troubleshooting problems, monitoring activity, and documenting the entire process.

---

## About Me

- Building a professional offensive and defensive cybersecurity homelab
- Developing practical Red Team and Blue Team skills
- Learning enterprise-style network segmentation and firewall engineering
- Building experience with Linux and Windows administration
- Practicing network security, ethical hacking, detection, and incident response
- Documenting practical cybersecurity projects on GitHub

My learning methodology:

**Learn → Build → Break → Troubleshoot → Fix → Test → Document → Repeat**

---

## Current Focus

My current focus areas include:

- Network Security
- Firewall Engineering
- Linux Administration
- Windows Administration
- Blue Team Operations
- Red Team Fundamentals
- SOC Operations
- Threat Detection
- Incident Response
- Ethical Hacking
- Penetration Testing
- Detection Engineering

---

## Featured Project

### Cybersecurity Homelab

My flagship project is a segmented offensive and defensive cybersecurity homelab built using:

- Oracle VirtualBox
- OPNsense
- Kali Linux
- Windows 11 Enterprise
- Ubuntu Server

The lab has evolved from a basic flat network into a segmented architecture with centralized firewalling, routing, NAT, DNS, security policies, and controlled attack paths.

Repository:

**`cybersecurity-homelab`**

---

## Current Homelab Architecture

The current environment contains three internal security zones protected by OPNsense.

| Zone | Network | Purpose |
|---|---|---|
| REDNET | `10.10.10.0/24` | Offensive Security |
| CORPNET | `10.10.20.0/24` | Management / Defensive Endpoint |
| SERVERNET | `10.10.30.0/24` | Protected Servers |

### Core Systems

| System | Operating System | Role | Address |
|---|---|---|---|
| `LAB-FW-01` | OPNsense | Firewall / Router / Security Gateway | Multiple Interfaces |
| `LAB-KALI-01` | Kali Linux | Offensive Security Workstation | `10.10.10.10` |
| `LAB-WIN-01` | Windows 11 Enterprise | Management / Defensive Endpoint | `10.10.20.20` |
| `LAB-UBUNTU-01` | Ubuntu Server | Protected Linux Server | `10.10.30.30` |

All inter-zone communication passes through OPNsense.

Direct VirtualBox NAT access on Kali, Windows, and Ubuntu has been disabled so internal traffic must use the firewall.

---

## What I Have Built

### Network Engineering

- Static IPv4 addressing
- Routing
- Default gateway configuration
- DNS configuration
- VirtualBox networking
- Internal network segmentation
- Multi-zone network architecture
- Connectivity testing
- Route troubleshooting
- NAT validation

### OPNsense Firewall

- Dedicated WAN interface
- CORPNET security zone
- REDNET security zone
- SERVERNET security zone
- Host aliases
- Network aliases
- Service aliases
- Least-privilege firewall rules
- Stateful firewall policies
- Outbound NAT
- DNS services
- NTP services
- Firewall management restrictions
- Inter-zone segmentation
- Security logging
- Configuration backups

### Linux

- Kali Linux
- Ubuntu Server
- Linux networking
- NetworkManager
- Netplan
- SSH
- Bash
- Service management
- Linux troubleshooting

### Windows

- Windows 11 Enterprise
- PowerShell
- Windows networking
- Routing
- DNS troubleshooting
- Windows Firewall
- Endpoint administration
- Network diagnostics

---

## Validated Security Controls

The current lab has been tested to confirm that firewall policy behaves as designed.

| Source | Destination | Result |
|---|---|---|
| Windows | OPNsense HTTPS | ALLOW |
| Windows | Ubuntu SSH | ALLOW |
| Windows | Kali | BLOCK |
| Kali | Ubuntu | ALLOW |
| Kali | Windows | BLOCK |
| Kali | OPNsense Management | BLOCK |
| Ubuntu | Windows | BLOCK |
| Ubuntu | Kali | BLOCK |

The environment therefore supports controlled offensive-security activity without giving the attacker network unrestricted access to trusted systems.

---

## Controlled Attack Path

The primary authorized offensive-security path is:

**Kali → REDNET → OPNsense → SERVERNET → Ubuntu**

This path is used for controlled:

- Reconnaissance
- Port scanning
- Enumeration
- Vulnerability assessment
- Service discovery
- Ethical hacking
- Future exploitation exercises

Nmap testing has confirmed SSH exposure on the Ubuntu target through the authorized firewall path.

---

## Controlled Administrative Path

The trusted administrative path is:

**Windows → CORPNET → OPNsense → SERVERNET → Ubuntu**

This allows approved server-management traffic while keeping other inter-zone communication restricted.

---

## Technical Skills

### Networking

- TCP/IP
- IPv4
- Subnetting
- Routing
- NAT
- DNS
- DHCP fundamentals
- ICMP
- TCP
- UDP
- Network segmentation
- Firewall policy design
- Connectivity troubleshooting

### Operating Systems

- Kali Linux
- Ubuntu Server
- Windows 11 Enterprise
- OPNsense

### Offensive Security

- Reconnaissance
- Network scanning
- Service enumeration
- Vulnerability assessment
- Ethical hacking fundamentals
- Penetration-testing fundamentals

### Defensive Security

- Firewall administration
- Network segmentation
- Security logging
- Endpoint monitoring fundamentals
- Blue Team fundamentals
- SOC fundamentals
- Incident-response fundamentals

---

## Tools and Technologies

### Infrastructure and Networking

- Oracle VirtualBox
- OPNsense
- TCP/IP
- DNS
- NAT
- SSH

### Offensive Security

- Kali Linux
- Nmap
- Burp Suite
- Metasploit
- Netcat
- Gobuster
- Wireshark

### Defensive Security

- OPNsense
- Windows Event Viewer
- PowerShell
- Linux logs
- Firewall logs
- Wireshark

### Planned Security Stack

- Wazuh
- Sysmon
- Suricata
- Linux auditd
- Windows Event Forwarding
- Velociraptor

---

## Cybersecurity Learning Roadmap

My development path is focused on building capabilities across both offensive and defensive cybersecurity.

Cybersecurity Fundamentals  
↓  
Networking Fundamentals  
↓  
Linux & Windows Administration  
↓  
Network Security  
↓  
Firewall Engineering  
↓  
SOC / Blue Team  
↓  
Threat Detection  
↓  
Incident Response  
↓  
Offensive Security  
↓  
Penetration Testing  
↓  
Advanced Red Team and Blue Team Operations

---

## Upcoming Homelab Development

The next stages of the lab include:

- SOC-NET
- Wazuh SIEM
- Centralized logging
- Windows Sysmon
- Windows security telemetry
- Linux audit logging
- OPNsense log forwarding
- Suricata IDS
- IDS alert analysis
- IPS experimentation
- Active Directory
- Windows Server
- Domain Controller
- Group Policy
- Active Directory attack simulation
- Detection engineering
- Vulnerable applications
- DMZ architecture
- Threat hunting
- Incident-response exercises

The long-term workflow is:

**Attack → Detect → Investigate → Respond → Remediate → Retest**

---

## Planned SOC Architecture

A future dedicated SOC network is planned.

**SOC-NET:** `10.10.40.0/24`

Potential components include:

- Wazuh Manager
- Wazuh Indexer
- Wazuh Dashboard
- Centralized log collection
- Detection engineering
- Security monitoring
- Alert investigation

Telemetry will eventually be collected from:

- Windows
- Ubuntu
- OPNsense
- Suricata
- Active Directory systems

---

## Planned Active Directory Lab

A future enterprise identity environment will include:

- Windows Server
- Active Directory Domain Services
- Domain Controller
- DNS
- Group Policy
- Domain users
- Domain computers
- Kerberos
- Windows authentication logging

Proposed network:

**AD-NET:** `10.10.50.0/24`

The lab will support both Active Directory attack simulation and defensive detection.

---

## Planned DMZ

A future DMZ will provide a separate environment for intentionally vulnerable and public-facing lab services.

Proposed network:

**DMZ-NET:** `10.10.60.0/24`

Potential targets include:

- OWASP Juice Shop
- DVWA
- Linux web servers
- APIs
- Intentionally vulnerable applications

---

## Certifications and Learning

### Completed

- Google Cybersecurity Professional Certificate

### Current and Planned Development

- Networking and CCNA-level knowledge
- Security fundamentals
- Network security
- SOC operations
- Blue Team operations
- Ethical hacking
- Penetration testing
- Incident response
- Detection engineering

---

## GitHub Goals

I use GitHub to document practical cybersecurity work including:

- Homelab architecture
- Network configurations
- Firewall configurations
- Security policies
- Troubleshooting
- Offensive-security exercises
- Defensive-security exercises
- Detection engineering
- Scripts
- Incident-response labs
- Cybersecurity learning notes

The goal is to build a portfolio that demonstrates both technical understanding and practical implementation.

---

## Professional Interests

I am particularly interested in:

- Cybersecurity
- Network Security
- Security Operations
- Blue Team
- Red Team
- SOC Operations
- Threat Detection
- Ethical Hacking
- Penetration Testing
- Incident Response
- Digital Forensics
- Detection Engineering
- Security Architecture
- Active Directory Security

---

## Current Mission

My goal is to progress beyond understanding cybersecurity concepts and become capable of designing, securing, attacking, monitoring, troubleshooting, and defending realistic environments.

I am building that capability one lab at a time.

**Learn → Build → Break → Troubleshoot → Fix → Test → Document → Repeat**

---

## Connect With Me

### GitHub

**Emmanuel-Ngari**

### LinkedIn

**Emmanuel Ngari**

[linkedin.com/in/emmanuel-ngari](https://www.linkedin.com/in/emmanuel-ngari)

LinkedIn username:

`emmanuel-ngari`
