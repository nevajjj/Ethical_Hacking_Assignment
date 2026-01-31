# Ethical Hacking: Vulnerability Assessment & Penetration Testing

## 📌 Project Overview
This repository contains a comprehensive security assessment of the **Metasploitable 2** virtual machine. The project simulates a professional penetration test, moving from initial reconnaissance through to exploitation and post-exploitation analysis.

---

## 🎯 Objectives
* **Information Gathering:** Identifying open ports, services, and operating system details.
* **Vulnerability Assessment:** Using automated tools and manual research to find weaknesses.
* **Exploitation:** Demonstrating how specific vulnerabilities (like VSFTPD or Samba) can be leveraged to gain access.
* **Reporting:** Documenting findings and providing remediation strategies to secure the system.

---

## 🛠 Technical Stack & Tools
* **Target:** Metasploitable 2 (Linux-based vulnerable VM).
* **OS:** Kali Linux.
* **Tools Used:**
    * `Nmap`: Network discovery and port scanning.
    * `Nessus` / `OpenVAS`: Automated vulnerability scanning.
    * `Metasploit Framework`: Exploitation and payload delivery.
    * `Searchsploit`: Offline exploit database searching.

---

## 📈 Methodology
The assessment followed the standard penetration testing lifecycle:

1.  **Reconnaissance:** Scanning the target for active services.
2.  **Analysis:** Mapping discovered services to known CVEs (Common Vulnerabilities and Exposures).
3.  **Exploitation:** Gaining unauthorized access via misconfigured services or unpatched software.
4.  **Post-Exploitation:** Assessing the level of control gained (e.g., Root access).

---

> **⚠️ Disclaimer:** This project was conducted in a controlled, isolated lab environment for educational purposes only. Unauthorized hacking is illegal and unethical.
