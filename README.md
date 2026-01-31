# Ethical Hacking & Network Penetration Testing Report

## 📌 Overview
This repository documents an **end-to-end penetration testing exercise** conducted as part of an **Ethical Hacking module** in the Diploma in Cybersecurity & Digital Forensics.

The objective of this project was to **simulate a real-world attack lifecycle** against a small, Active Directory–based corporate network, identifying weaknesses across **wireless security, Active Directory, authentication mechanisms, network segmentation, and post-exploitation controls**.

All activities were performed in a **fully controlled, isolated lab environment** using virtual machines and **authorised test accounts**.

---

## 🎯 Project Objectives
- Simulate a realistic multi-stage cyber attack
- Identify misconfigurations and security weaknesses
- Demonstrate lateral movement and privilege escalation
- Perform post-exploitation activities (credential harvesting, data theft, persistence)
- Apply defensive recommendations based on findings

---

## 🧪 Test Environment

### Virtual Machines
| Role | Operating System |
|----|----------------|
| Attacker | Kali Linux |
| Victim 1 | Windows Server 2019 (Domain Controller) |
| Victim 2 | Windows 10 (Domain-joined workstation) |

### Network Design
- Segmented subnets using VMware virtual networking
- Attacker and Victim 2 isolated by subnet
- Victim 1 dual-homed across both networks
- Active Directory domain: **EH.COM**

---

## 🛠 Tools & Technologies Used

- Airgeddon (Evil Twin Wi-Fi attack)
- Nmap
- Metasploit Framework
- Meterpreter
- Msfvenom
- Davtest
- Chisel (network tunnelling & pivoting)
- ProxyChains
- Mimikatz
- Impacket Suite (psexec, ticketConverter)
- SMBClient
- Auditpol
- Wevtutil
- SQLCMD
- John the Ripper

---

## 🔗 Attack Lifecycle Summary

### 1️⃣ Initial Access
- Evil Twin Wi-Fi attack using a captive portal
- Wireless credential capture
- Network access gained to victim subnet

### 2️⃣ Reconnaissance & Enumeration
- Network scanning and host discovery
- Service and OS fingerprinting
- Identification of Domain Controller and exposed services

### 3️⃣ Exploitation
- WebDAV misconfiguration exploited
- File upload restriction bypass
- PHP dropper and Meterpreter payload execution

### 4️⃣ Privilege Escalation
- Process migration
- Escalation to Domain Administrator privileges

### 5️⃣ Lateral Movement & Pivoting
- Network tunnelling via Chisel
- Discovery of secondary subnet
- Pivot attack to Victim 2

### 6️⃣ Credential Attacks
- NTLM hash dumping using Mimikatz DCSync
- Silver Ticket attack (Kerberos TGS forgery)
- Administrator hash cracking

### 7️⃣ Post-Exploitation
- Sensitive data discovery and extraction
- SQL database access
- SMB data exfiltration
- Persistence via NTFS Alternate Data Streams
- Scheduled task backdoor creation

### 8️⃣ Covering Tracks
- Audit policy manipulation
- Windows event log clearing
- Removal of attacker artefacts

---

## ⚠️ Ethical & Legal Disclaimer
This project was conducted **strictly for educational purposes** within an **authorised lab environment**.  
No real systems, organisations, or users were targeted.

This repository **does not endorse or encourage unauthorised access, exploitation, or malicious activity**.

---

## 📄 Report
The full technical report is included in this repository:

📁 `Ethical_Hacking_Report.docx`

---
