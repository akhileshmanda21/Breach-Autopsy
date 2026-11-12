# Attack lifecycle mapping



| Lifecycle Stage | Equifax | Colonial Pipeline | Target |
|---|---|---|---|
| **Reconnaissance** | Vulnerability scanning | VPN access opportunity | Third-party vendor identification |
| **Initial Access** | Apache Struts exploitation | Compromised VPN credentials | Stolen vendor credentials |
| **Execution** | Remote command execution | DarkSide ransomware execution | POS malware execution |
| **Persistence** | JSP web shells | Not publicly confirmed | Exact technique not confirmed |
| **Privilege / Credential Access** | Unencrypted credentials discovered | Technique not publicly confirmed | Movement beyond vendor access; exact technique unclear |
| **Discovery / Movement** | Internal database discovery | Internal IT environment access | Movement towards POS systems |
| **Collection** | Personal information | Corporate data | Payment card information |
| **Exfiltration / Impact** | Large-scale personal data theft | Data theft and ransomware disruption | Payment card data theft |




## SOC Analyst Observations
### 1. Suspicious Activity

**Equifax (2017)**
- Unusual HTTP requests targeting the Apache Struts vulnerability.
- Unexpected command execution on web application servers.
- Suspicious creation or execution of JSP web shells.
- Unauthorized access to internal databases.
- Unusual database queries and large outbound data transfers.

**Colonial Pipeline (2021)**
- Unusual VPN login activity involving a legacy account.
- Authentication using compromised VPN credentials.
- Suspicious access to internal corporate systems.
- Unusual file access and large outbound data transfers.
- Mass file modifications and ransomware-like encryption activity.

**Target (2013)**
- Unusual authentication activity involving third-party vendor accounts.
- Unauthorized access from the vendor-connected network.
- Suspicious communication between internal systems and POS terminals.
- Unexpected execution of malware on POS systems.
- Unusual outbound connections and payment card data transfers.

### 2. Important Log Sources

**Equifax**
- Web server and application logs.
- Web Application Firewall (WAF) logs.
- Firewall and IDS/IPS logs.
- Windows/Linux system logs.
- Sysmon and EDR telemetry.
- Database audit logs.
- Proxy and network traffic logs.

**Colonial Pipeline**
- VPN authentication logs.
- Active Directory authentication logs.
- Windows Security Event Logs.
- Sysmon and EDR telemetry.
- Firewall and network traffic logs.
- File access and file integrity monitoring logs.
- DNS and proxy logs.

**Target**
- VPN and vendor authentication logs.
- Firewall and network traffic logs.
- Active Directory logs.
- POS application logs.
- Endpoint detection and antivirus logs.
- DNS and proxy logs.
- File access and database audit logs.

### 3. Detection Opportunities

**Equifax**
- Detect repeated requests targeting known web application vulnerabilities.
- Alert when web server processes execute unusual commands.
- Monitor unauthorized creation of web shells.
- Detect unusual access to sensitive databases.
- Alert on abnormal outbound data transfers.

**Colonial Pipeline**
- Alert on unusual VPN logins and access involving legacy accounts.
- Detect authentication from unusual locations or devices.
- Monitor suspicious access to internal systems.
- Identify abnormal file access and large outbound transfers.
- Detect mass file modifications and ransomware-like encryption behavior.

**Target**
- Detect unusual authentication involving third-party vendor accounts.
- Monitor unexpected connections between vendor networks and internal systems.
- Detect suspicious processes running on POS terminals.
- Identify unauthorized software installation or execution.
- Monitor unusual outbound traffic from POS systems.
- Alert on suspicious payment card data access and transfers.

### 4. Preventive Recommendations

**Equifax**
- Apply security patches promptly.
- Implement continuous vulnerability scanning.
- Securely store credentials and secrets.
- Enforce network segmentation.
- Apply least-privilege access to databases.
- Deploy WAF, EDR and continuous security monitoring.

**Colonial Pipeline**
- Enforce multi-factor authentication (MFA) for VPN access.
- Disable unused and legacy accounts.
- Implement strong credential management policies.
- Restrict remote access using least privilege.
- Separate corporate IT and operational technology (OT) networks.
- Maintain tested offline backups and an incident response plan.

**Target**
- Enforce MFA for third-party and vendor access.
- Restrict vendor access to authorized systems only.
- Implement network segmentation between vendor networks and POS systems.
- Deploy endpoint protection on POS terminals.
- Monitor third-party connections and privileged accounts.
- Encrypt sensitive payment information and implement payment data protection controls.
- Conduct regular security assessments of third-party vendors.



