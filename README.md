# Breach Autopsy 

A practical cybersecurity research project examining three major real-world security incidents: **Equifax (2017), Target (2013), and Colonial Pipeline (2021)**. This project evaluates the attack methods, security weaknesses, business impact, risk severity, attack lifecycle, potential SOC detection opportunities, and defensive security controls associated with each incident.

The objective is to understand how security failures occur, how attackers exploit weaknesses, and how organizations can strengthen their security posture through effective monitoring, risk management, and defence-in-depth strategies.

---

## Project Overview

Cybersecurity incidents provide valuable lessons about the importance of vulnerability management, identity security, network segmentation, endpoint protection, and continuous security monitoring.

This project investigates three significant cybersecurity incidents from a defensive security perspective. Each case study examines the incident, identifies the underlying security weaknesses, evaluates its impact, and explores how security teams could detect, investigate, and prevent similar attacks.

The project also connects real-world incident analysis with a personal cybersecurity home lab assessment using Windows 11 and VMware.

## Case Studies

### 1. Equifax Data Breach (2017)

**Incident category:** Large-scale data breach

The Equifax breach involved attackers exploiting an unpatched vulnerability in the Apache Struts web application framework to gain unauthorized access to internal systems and steal sensitive personal information.

**Areas investigated:**
- Exploitation of Apache Struts vulnerability (CVE-2017-5638).
- Vulnerability and patch management failures.
- Exposure of sensitive personal information.
- Internal access and database security weaknesses.
- Potential detection opportunities through web server, application, authentication, and database logs.

### 2. Target Data Breach (2013)

**Incident category:** Point-of-sale (POS) malware attack

The Target breach involved attackers using compromised third-party vendor credentials to gain access to the organization's network and reach point-of-sale systems. Malware was deployed to collect payment card information.

**Areas investigated:**
- Third-party vendor access compromise.
- Network segmentation weaknesses.
- POS malware and payment card data theft.
- Security alert monitoring and response failures.
- Potential detection opportunities through authentication, endpoint, network, DNS, and POS logs.

### 3. Colonial Pipeline Ransomware Incident (2021)

**Incident category:** Ransomware and data exfiltration

The Colonial Pipeline incident involved the DarkSide ransomware group gaining access through a compromised legacy VPN account that did not have multi-factor authentication enabled. The incident resulted in data theft, ransomware deployment, and disruption to pipeline operations.

**Areas investigated:**
- Compromised VPN credentials.
- Legacy account security weaknesses.
- Lack of multi-factor authentication.
- Data exfiltration and ransomware impact.
- Potential detection opportunities through VPN, authentication, endpoint, file activity, and network logs.

---

## Project Objectives

The primary objectives of this project are to:

1. Analyze real-world cybersecurity incidents using publicly available information.
2. Understand the impact of security breaches on confidentiality, integrity, and availability.
3. Identify vulnerabilities, threats, and security control failures.
4. Evaluate incident severity through qualitative risk assessment.
5. Map attacker activities to an eight-stage attack lifecycle.
6. Identify relevant log sources for SOC monitoring and investigation.
7. Recommend preventive, detective, and corrective security controls.
8. Assess the attack surface of a Windows 11 and VMware home lab.
9. Apply defence-in-depth principles to strengthen the home lab security posture.
10. Develop practical incident analysis and defensive security documentation skills.

---

## Security Analysis Framework

### 1. CIA Triad Assessment

Each incident is evaluated using the three fundamental principles of information security.

| Security Principle | Assessment Focus |
|---|---|
| Confidentiality | Unauthorized disclosure or exposure of sensitive information |
| Integrity | Unauthorized modification or manipulation of systems and data |
| Availability | Disruption or loss of access to systems and services |

### 2. Vulnerability, Threat and Risk Assessment

Each breach is examined to identify the security weaknesses that contributed to the incident and the threats that exploited them.

**Risk calculation:**

`Risk Score = Likelihood × Impact`

Both likelihood and impact are rated on a scale of 1 to 5.

| Risk Score | Risk Classification |
|---:|---|
| 1–4 | Low |
| 5–9 | Moderate |
| 10–16 | High |
| 17–25 | Critical |

*Risk scores represent qualitative analytical assessments for this project, not official ratings assigned by the affected organizations.*

### 3. Attack Lifecycle Analysis

The incidents are mapped against eight attack lifecycle stages to understand attacker behaviour and identify possible detection opportunities.

| No. | Attack Lifecycle Stage |
|---:|---|
| 1 | Reconnaissance |
| 2 | Initial Access |
| 3 | Execution |
| 4 | Persistence |
| 5 | Privilege Escalation / Credential Access |
| 6 | Discovery / Lateral Movement |
| 7 | Collection |
| 8 | Exfiltration / Impact |

Where public reporting does not establish a specific technique, it is documented as not publicly confirmed rather than assumed.

### 4. SOC Log Source Analysis

Potential log sources are identified for each incident to understand how a Security Operations Center could monitor and investigate similar activity.

| Log Source | Security Monitoring Purpose |
|---|---|
| Windows Event Logs | Authentication, account activity, and system events |
| Sysmon | Process creation, network connections, and other endpoint activity |
| Firewall Logs | Network connections and blocked traffic |
| DNS Logs | Suspicious domain resolution and unusual DNS activity |
| VPN Logs | Remote access and authentication activity |
| Web Server Logs | HTTP requests, suspicious requests, and application activity |
| Database Audit Logs | Unauthorized database access and unusual queries |
| EDR Alerts | Suspicious endpoint behaviour and malware activity |
| Proxy Logs | Web access and potentially suspicious outbound connections |

**Note:** These are potential SOC investigation sources. They should not be interpreted as proof that every listed log source was available or retained during the original incidents.

---

## Home Lab Security Assessment

This project extends beyond historical breach analysis by examining the security posture of a personal cybersecurity home lab.

**Lab Environment:**

| Component | Configuration |
|---|---|
| Host Operating System | Windows 11 |
| Virtualization Platform | VMware Workstation |
| Host Memory | 16 GB RAM |
| Virtual Environment | VMware Virtual Machines |
| Security Focus | Attack Surface Assessment and Defence in Depth |

### 1. Attack Surface Assessment

The assessment identifies potential entry points and weaknesses across the home lab environment.

Key assets and services examined include:

- Windows 11 host operating system.
- VMware Workstation.
- Virtual machines.
- Administrator and standard user accounts.
- Remote Desktop Protocol (RDP).
- Secure Shell (SSH).
- Web applications.
- VMware network adapters.
- Shared folders.
- SIEM / Wazuh server.

Each item is assessed based on its exposure, potential security risk, and available evidence.

### 2. Defence-in-Depth Assessment

The home lab security architecture is evaluated using six defensive layers.

| Security Layer | Example Controls |
|---|---|
| Perimeter | Router firewall and secure Wi-Fi configuration |
| Network | Network segmentation, VMware Host-only networking, and firewall rules |
| Host | Windows Defender Antivirus, host firewall, and system updates |
| Identity and Access | Strong passwords, MFA, and least privilege |
| Application and Data | Application updates, access controls, and secure backups |
| Monitoring and Response | Wazuh SIEM, Sysmon, Windows Event Logs, and incident response procedures |

The objective is to understand how multiple independent security controls can reduce attack opportunities, detect suspicious activity, and limit the impact of a compromise.

---

## Key Learning Outcomes

Through this project, I explored:

- Real-world attack patterns and cybersecurity incidents.
- CIA Triad and security impact assessment.
- Vulnerability identification and threat analysis.
- Qualitative risk scoring and prioritization.
- MITRE ATT&CK-aligned attack lifecycle concepts.
- SOC-relevant log sources and detection opportunities.
- Network security and segmentation principles.
- Third-party access security.
- Endpoint and authentication monitoring.
- Attack surface identification.
- Defence-in-depth security architecture.
- Preventive, detective, and corrective security controls.
- Technical research and incident documentation.

---

## Repository Structure

```text
breach-autopsy-portfolio/
│
├── README.md                      # Project overview, breaches chosen, link to final PDF
│
├── 01-research/
│   ├── sources.md                 # Links to every report, grouped by breach
│   ├── equifax/
│   │   ├── notes.md               # Raw timeline and key facts
│   │   └── report-links.md
│   ├── target/
│   │   ├── notes.md
│   │   └── report-links.md
│   └── colonial-pipeline/
│       ├── notes.md
│       └── report-links.md
│
├── 02-analysis/
│   ├── cia-classification.md      # C/I/A hit per breach, with the "why"
│   ├── vulnerability-threat-risk.md   # Tables with likelihood x impact scores
│   ├── lifecycle-mapping.md       # 8 stages + log source, per breach
│   └── controls-classification.md # Preventive / detective / corrective tables
│
├── 03-home-lab/
│   ├── attack-surface.md          # Your 10+ items
│   ├── evidence/                  # Screenshots, e.g. output of ss -tulnp
│   └── defence-in-depth.md        # Short explanation of each layer
│
├── 04-diagrams/
│   ├── defence-in-depth.drawio    # Editable source file
│   ├── defence-in-depth.png       # Exported image
│   └── defence-in-depth.pdf
│
├── 05-final/
│   ├── breach-autopsy-report.pdf  # The 4-page deliverable
│   └── breach-autopsy-report.docx # Editable source
│
└── .gitignore
```

*The structure above represents the intended organization. Keep only files that are actually present in the repository.*

---

## Research Methodology

This project is based on secondary research using publicly available sources, including:

- Government investigation reports.
- Official company statements and disclosures.
- Regulatory and congressional reports.
- Reputable cybersecurity research publications.
- Technical vulnerability advisories.

Incident details are documented based on available public evidence. Analytical recommendations and potential detection opportunities are distinguished from techniques confirmed in original incident reporting.

Refer to [`research/sources.md`](research/sources.md) for the research references.

---

## Disclaimer

This repository is intended for educational, research, and defensive cybersecurity learning purposes only.

The case studies are based on publicly available information. Risk ratings, recommended controls, and potential SOC detection opportunities represent independent educational analysis and should not be interpreted as official incident findings.

No unauthorized access, exploitation, or testing of third-party systems was performed as part of this project.

---

## Author

**Cybersecurity Learner | Aspiring SOC Analyst | Blue Team Enthusiast**

This project is part of my ongoing journey to develop practical skills in security monitoring, threat analysis, incident investigation, vulnerability assessment, and defensive security operations.

**Focus Areas:** SOC Operations | SIEM | Threat Detection | Incident Response | Blue Team Security


## Project contents

- [Research sources](./01-case-studies/sources.md)
- [Breach case studies](./01-case-studies/)
- [Breach analysis](./02-analysis/)
- [Home lab](./03-home-lab/)
- [Defence-in-depth diagram](./04-diagrams/defence-in-depth.drawio)

## Final deliverable

[Download the four-page breach autopsy report (PDF)](./05-final-report/breach-autopsy-report.pdf).