# Microsoft Sentinel Threat Detection & Incident Response Lab

![Microsoft Sentinel](https://img.shields.io/badge/Microsoft-Sentinel-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)
![Azure](https://img.shields.io/badge/Azure-Cloud-blue?style=for-the-badge&logo=microsoftazure)
![KQL](https://img.shields.io/badge/KQL-Kusto-orange?style=for-the-badge)
![Windows Security](https://img.shields.io/badge/Windows-Security-success?style=for-the-badge)

---

# Project Overview

This project demonstrates the implementation of a cloud-based Security Operations Center (SOC) using **Microsoft Sentinel**, **Azure Arc**, **Azure Monitor Agent**, and **Log Analytics Workspace**.

The objective was to collect Windows Security Events, perform threat hunting using **Kusto Query Language (KQL)**, create Microsoft Sentinel analytics rules, investigate security incidents, and document findings following industry best practices.

This lab simulates common SOC analyst tasks including authentication monitoring, process monitoring, privilege escalation detection, and incident investigation.

---

# Project Objectives

- Deploy Microsoft Sentinel
- Connect a Windows endpoint using Azure Arc
- Configure Azure Monitor Agent (AMA)
- Configure Data Collection Rules (DCR)
- Collect Windows Security Events
- Perform threat hunting using KQL
- Develop Analytics Rules
- Investigate security events
- Create incident reports
- Map detections to MITRE ATT&CK

---

# Architecture

```
Windows 10 VM
      │
      ▼
Azure Arc
      │
      ▼
Azure Monitor Agent (AMA)
      │
      ▼
Data Collection Rule (DCR)
      │
      ▼
Log Analytics Workspace
      │
      ▼
Microsoft Sentinel
      │
 ┌────┼────────────┐
 │    │            │
 ▼    ▼            ▼
KQL Analytics  Threat Hunting
Rules
      │
      ▼
 Alerts
      │
      ▼
Incidents
```

---

# Technologies Used

| Category | Technology |
|----------|------------|
| Cloud Platform | Microsoft Azure |
| SIEM | Microsoft Sentinel |
| Endpoint Management | Azure Arc |
| Monitoring | Azure Monitor |
| Log Storage | Log Analytics Workspace |
| Data Collection | Azure Monitor Agent |
| Query Language | Kusto Query Language (KQL) |
| Operating System | Windows 10 |
| Virtualization | VirtualBox |
| Version Control | Git & GitHub |

---

# Windows Security Events Investigated

| Event ID | Description |
|----------|-------------|
| 4624 | Successful Logon |
| 4625 | Failed Logon |
| 4688 | Process Creation |
| 4720 | User Account Created |
| 4732 | User Added to Administrators Group |
| 1102 | Audit Log Cleared |

---

# Analytics Rules Implemented

- Brute Force Login Detection
- New Local User Detection
- Process Creation Monitoring
- Administrator Group Modification Detection
- Audit Log Cleared Detection

---

# Threat Hunting

The following Windows Security Events were investigated using Kusto Query Language (KQL):

- Event ID 4624 – Successful Logon
- Event ID 4625 – Failed Logon
- Event ID 4688 – Process Creation
- Event ID 4720 – User Account Created
- Event ID 4732 – Administrator Group Modification
- Event ID 1102 – Audit Log Cleared

Each investigation includes:

- Detection Objective
- KQL Query
- Investigation Methodology
- Expected Findings
- MITRE ATT&CK Mapping

---

# Incident Reports

The project includes structured incident reports for:

- Brute Force Login Attempt
- Unauthorized User Creation
- Privilege Escalation
- Audit Log Cleared

Each report documents:

- Incident Summary
- Timeline
- Evidence
- Investigation
- MITRE ATT&CK Mapping
- Recommended Response
- Lessons Learned

---

# Repository Structure

```
Microsoft-Sentinel-Threat-Detection-Lab/

├── README.md

├── Architecture/

├── Documentation/
│   ├── Architecture.md
│   ├── Lab-Setup.md
│   └── Lessons-Learned.md

├── Screenshots/
│   ├── Azure-Setup/
│   ├── KQL-Queries/
│   ├── Analytics-Rules/
│   ├── Incidents/
│   └── Workbooks/

├── KQL/

├── Analytics-Rules/

├── Threat-Hunting/

├── Incident-Reports/

└── MITRE-Mapping/
```

---

# Skills Demonstrated

### Microsoft Sentinel

- Analytics Rules
- Threat Hunting
- Incident Investigation
- Log Analysis

### Azure

- Azure Arc
- Azure Monitor
- Azure Monitor Agent
- Data Collection Rules
- Log Analytics Workspace

### Windows Security

- Authentication Monitoring
- Process Monitoring
- User Account Monitoring
- Privilege Escalation Detection
- Audit Log Monitoring

### Detection Engineering

- Kusto Query Language (KQL)
- Windows Security Events
- Analytics Rule Development
- MITRE ATT&CK Mapping

### Incident Response

- Alert Investigation
- Security Event Analysis
- Timeline Analysis
- Evidence Collection
- Documentation

---

# MITRE ATT&CK Mapping

| Event ID | Tactic | Technique |
|----------|---------|-----------|
|4624|Initial Access|Valid Accounts (T1078)|
|4625|Credential Access|Brute Force (T1110)|
|4688|Execution|Command and Scripting Interpreter (T1059)|
|4720|Persistence|Create Account (T1136)|
|4732|Privilege Escalation|Account Manipulation (T1098)|
|1102|Defense Evasion|Clear Windows Event Logs (T1070.001)|

---

# Key Learning Outcomes

Through this project I gained practical experience with:

- Microsoft Sentinel deployment and configuration
- Azure Arc onboarding
- Azure Monitor Agent configuration
- Data Collection Rules
- Log Analytics Workspace
- Windows Security Event analysis
- Kusto Query Language (KQL)
- Threat Hunting
- Detection Engineering
- Incident Investigation
- MITRE ATT&CK mapping
- Technical documentation

---

# Future Improvements

Potential enhancements include:

- Sysmon integration
- Microsoft Defender for Endpoint integration
- Sentinel Workbooks
- Automation Rules
- Logic Apps
- Email alerting
- Custom detection rules
- Advanced KQL hunting queries

---

# Screenshots

The repository contains screenshots demonstrating:

- Azure Arc onboarding
- Azure Monitor Agent installation
- Data Collection Rules
- Microsoft Sentinel configuration
- KQL query execution
- Analytics Rules
- Security Event investigations
- Incident generation

---

# Disclaimer

This project was created in a controlled lab environment for educational and learning purposes. All activities were performed on a dedicated virtual machine and Azure resources owned by the project author.

---

# Author

**Mohammad Shaikh**

Cybersecurity Enthusiast | SOC Analyst Aspirant

