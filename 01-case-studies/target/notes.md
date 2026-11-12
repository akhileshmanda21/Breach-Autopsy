# Target breach

## Summary
 The 2013 Target data breach began with credentials stolen from a third-party HVAC contractor. Attackers used that foothold to enter Target’s environment, move toward point-of-sale systems, install malware and exfiltrate payment card data. The breach was initially believed to involve about 40 million Target credit and debit card accounts. Target later acknowledged that the attack had also exposed contact and identifying information for as many as 70 million individuals.  A U.S. Senate Commerce Committee staff analysis later highlighted weak third-party security, missed intrusion alerts, and insufficient isolation of sensitive network assets as apparent missed opportunities to stop the attack.

 More than a decade later, the Target breach remains a useful cybersecurity case study because the attack was not just about malware. It was about how vendor access, identity, segmentation, monitoring, and incident response interact. Those same control areas remain central to modern Zero Trust and cyber-resilience programs.

## Timeline
| Date | What Happened |
| :--- | :--- |
| **At least two months before the payment-card breach** | The Senate report said attackers reportedly stole Fazio Mechanical credentials through malware-infected email. |
| **Nov. 12–30, 2013** | Public reports summarized by the Senate staff report placed initial Target network access and early POS malware installation in this period. These dates were based on reporting and investigator accounts, not a definitive Target disclosure. |
| **Nov. 27–Dec. 15, 2013** | Target said unauthorized access to payment-card data occurred in U.S. stores during this period. |
| **Dec. 12, 2013** | Target officials testified that the company was not aware of the breach until contacted by the U.S. Department of Justice. |
| **Dec. 18, 2013** | Security journalist Brian Krebs publicly reported the breach. |
| **Dec. 19, 2013** | Target publicly confirmed that [approximately 40 million] credit and debit card accounts may have been impacted. |
| **Jan. 10, 2014** | Target disclosed that names, mailing addresses, phone numbers or email addresses for [up to 70 million] individuals had also been taken. |
| **Apr. 29, 2014** | Target described security changes including enhanced monitoring and logging, POS application whitelisting, stronger segmentation, reduced vendor access and expanded two-factor authentication. |
| **May 23, 2017** | Target entered an $18.5 million multistate settlement related to the breach. |
| **2017 SEC filing** | Target reported $292 million of cumulative breach expenses, offset by $90 million of insurance recoveries, for [$202 million] in net cumulative expenses. |


## How Hackers Breached Target
## 1. Third-Party Vendor Compromise
- Attackers reportedly stole Target-access credentials from **Fazio Mechanical Services** after compromising the vendor.
- This provided attackers with credentials associated with a trusted third-party vendor.

### 2. Vendor Credentials Created a Foothold
- The stolen credentials were used to enter a Target-accessible environment.
- The precise technical path from the vendor portal to the payment environment was not fully established in the public record.

### 3. Lateral Movement Through Internal Systems
- Attackers moved through Target's internal network.
- The Senate staff analysis concluded that attackers appeared to move from less-sensitive areas into systems associated with consumer data.
- This indicated insufficient isolation and segmentation of sensitive assets.

### 4. POS Malware Captured Payment-Card Data
- RAM-scraping malware was installed on Point-of-Sale (POS) systems.
- The malware collected payment-card data while transactions were being processed.
- This allowed attackers to capture sensitive card information from affected systems.

### 5. Data Staging and Exfiltration
- Additional malware moved the collected data through Target's internal environment.
- The stolen information was transferred to attacker-controlled infrastructure.
- This enabled attackers to extract large amounts of payment-card information from the organization.

### 6. Failure to Respond to Security Alerts
- The Senate staff report indicated that Target appeared to have failed to respond effectively to multiple automated security warnings.
- These alerts were related to malware installation and suspicious data exfiltration activity.
- The failure to investigate and respond to these warnings allowed the attackers' operation to continue.

---

## Attack Chain Summary

| Stage | Attacker Activity | Security Weakness |
|---|---|---|
| 1. Initial Access | Compromised Fazio Mechanical Services credentials | Third-party vendor security |
| 2. Foothold | Used stolen credentials to access a Target environment | Insufficient vendor access restrictions |
| 3. Lateral Movement | Moved through internal systems | Inadequate network segmentation |
| 4. Execution | Installed RAM-scraping malware on POS systems | Insufficient endpoint protection |
| 5. Exfiltration | Transferred stolen payment-card data to external infrastructure | Insufficient data monitoring and exfiltration controls |
| 6. Detection Failure | Continued operations despite automated security alerts | Ineffective alert investigation and incident response |


## Key facts
**Threat actor / access path:**
- Attackers compromised third-party vendor Fazio Mechanical Services.
- Stolen vendor credentials were used to gain access to Target's network.
- Attackers moved laterally through internal systems and accessed environments associated with payment processing.
- RAM-scraping malware was installed on Point-of-Sale (POS) systems to capture payment-card information.

**Affected systems or data:**
- Point-of-Sale (POS) systems across Target stores.
- Payment-card processing systems.
- Credit and debit card information, including card numbers, expiration dates, and security codes.
- Customer names, mailing addresses, phone numbers, and email addresses.

**Discovery and containment:**
- Target's security systems generated multiple automated alerts related to suspicious activity and malware.
- The company reportedly failed to respond effectively to several security warnings.
- Security journalist Brian Krebs publicly reported the breach on December 18, 2013.
- Target publicly confirmed the payment-card breach on December 19, 2013.
- Target subsequently removed the malware, strengthened security monitoring, improved network segmentation, and restricted third-party vendor access.

**People or records affected:**
- Approximately **40 million** credit and debit card accounts may have been affected.
- Personal information belonging to up to **70 million individuals** was also compromised.
- The exposed information included names, mailing addresses, phone numbers, and email addresses.

**Business and regulatory impact:**
- Target faced significant financial losses, legal expenses, and reputational damage.
- The company reported approximately **$202 million in net cumulative breach expenses** in its 2017 SEC filing, after insurance recoveries.
- Target entered an **$18.5 million multistate settlement** in May 2017.
- The incident exposed weaknesses in third-party vendor security, network segmentation, POS security, and security alert response.
- The breach highlighted the importance of continuous security monitoring, effective incident response, and strong access controls.

