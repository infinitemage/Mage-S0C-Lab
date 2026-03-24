# 🚀 Project Mage-SOC: Security Operations & Automated Defense

![mage-soc-layout](images/banner.jpg)

### 📖 Executive Overview
Designed to build a fully integrated Security Operations Center (SOC) from scratch. This project simulates a corporate production environment, moving from initial vulnerability baselining to active threat emulation and automated detection engineering.

**Goal:** Architect, integrate, and harden a heterogeneous network (Linux, Windows, IoT) to detect and respond to advanced persistent threats.

### 🧰 Skills & Technologies
* **SIEM & Log Aggregation:** Wazuh, Sysmon, OSQuery, Syslog
* **Vulnerability Management:** Tenable Nessus Pro, Credentialed Scanning, Remediation
* **Threat Emulation & Offensive Tools:** Nmap, Hydra, Metasploit (Parrot OS)
* **Frameworks Applied:** NIST Cybersecurity Framework (CSF), MITRE ATT&CK

---

## 🏗️ System Architecture 

| **Node** | **Hostname** | **Role** | **OS / Hardware** | **Core Software** |
| :--- | :--- | :--- | :--- | :--- |
| **The Brain** | `SOC-Server` | SIEM & Log Aggregator | Raspberry Pi 5 (SunFounder Pironman 5 Max, 1TB SSD) | Wazuh Server, Dashboards |
| **The Auditor** | `Pop-Scanner` | Vuln. Management | Pop!_OS (Baremetal), Nvidia 5080 | Tenable Nessus Pro |
| **Endpoint 1** | `Windows-Machine` | Hardened Target | Windows (Baremetal) | Sysmon, Wazuh Agent |
| **Endpoint 2** | `Linux-Machine` | Hardened Target | Pop!_OS (Baremetal), Nvidia 5080 | OSQuery, Wazuh Agent |
| **Attacker** | `Parrot-Attacker` | Threat Emulation | Parrot OS (Baremetal) | Nmap, Hydra, Metasploit |

---

## 🗺️ Project Phases & Documentation

### Phase 1: Vulnerability Management & Hardening
*Implemented credentialed scanning to establish a baseline and remediated critical misconfigurations.*
* 📄 [Windows 10 Vulnerability Assessment](./Vulnerability_Management/)

* 📄 [SMB Signing](./Vulnerability_Management/01_SMB_Signing_Misconfig.md)

* 📄 [Windows 10 OS End-of-Life Lifecycle](./Vulnerability_Management/)

* 📜 [Linux Hardening & Auditing Scripts](./Scripts/Linux_Hardening.sh)

### Phase 2: Log Aggregation & SIEM Deployment *(In Progress)*
*Configuring Wazuh to ingest endpoint telemetry via Sysmon and OSQuery.*
* 📄 [Setting up the Wazuh Server on Raspberry Pi 5](#)
* 📄 [Deploying Sysmon & Wazuh Agents to Endpoints](#)

### Phase 3: Threat Emulation & Detection Engineering *(Upcoming)*
*Executing localized attacks from Parrot OS and writing custom detection rules.*
* 📄 [Detecting Brute Force & SSH Credential Stuffing](#)
* 📄 [Writing Custom Wazuh Rules for MITRE ATT&CK Techniques](#)

---

## 👤 About the Author 
I am a driven Cybersecurity Engineer with a focus on Detection Engineering, Vulnerability Management, and Systems Architecture, coupled with a strong passion for offensive security and penetration testing. 

<img src="" alt="TryHackMe Cyber Security 101 Certificate" />

<img src="" alt="TryHackMe Pre Security Certificate" />

> *"The way you do one thing is the way you do everything."* — Miyamoto Musashi
