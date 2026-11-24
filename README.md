# Wazuh SOC Home Lab

## Project Overview
This project demonstrates a hands-on Security Operations Center home lab using Wazuh 4.14.10 to monitor a Kali Linux endpoint, investigate security events, and document findings.

## Lab Architecture
- SIEM: Wazuh 4.14.10
- Endpoint: Kali Linux 2026.2
- Virtualization: VMware Workstation
- Agent ID: 001

## Project Objectives
- Connect and monitor a Linux endpoint using Wazuh.
- Configure File Integrity Monitoring.
- Detect file creation, modification, and deletion.
- Investigate FIM security events.
- Examine Linux authentication logs.
- Document security investigations.

## Technologies Used
- Wazuh
- Kali Linux
- VMware Workstation
- Linux system logs
- File Integrity Monitoring
- Security event investigation

## Investigations

### Investigation 1: File Integrity Monitoring
A controlled test created, modified, and deleted a file in a monitored directory. Wazuh detected all three actions in real time (rules 554, 550, 553), including file path and SHA-1/SHA-256 hashes.
[Read the report](reports/fim-investigation.md)

### Investigation 2: Linux Authentication Monitoring
Controlled successful sudo activity was examined through Linux logs and Wazuh (rules 5402, 5501, 5502, with MITRE ATT&CK mapping). A failed-authentication test was not captured, so that detection is documented as unverified.
[Read the report](reports/auth-investigation.md)

## Skills Demonstrated
- SIEM monitoring
- Endpoint monitoring
- FIM configuration
- Alert triage
- Linux log analysis
- Security event investigation
- Incident documentation

## Repository Contents
- `configuration/`: FIM configuration example.
- `reports/`: Investigation reports.
- `screenshots/`: Lab evidence.

## Disclaimer
All testing was performed in an authorized, isolated home lab environment using harmless test activity.
