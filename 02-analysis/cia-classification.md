# CIA Classification

| Breach | Confidentiality | Integrity | Availability | Root cause category |
|---|---|---|---|---|
| Equifax (2017) | Yes (primary) | Limited | No | Missing patch, weak detection |
| Target (2013) | Yes (primary) | Limited | No | Third-party access, ignored alerts |
| Colonial Pipeline (2021) | Yes | Yes | Yes (primary) | No MFA on remote access |

Key: Yes = clearly hit, Limited = secondary or weak evidence, No = not hit.

## Equifax (2017)
- **C:** Personal data of roughly 147M people was stolen (names, SSNs, birth dates, addresses).
- **I:** No strong evidence that data was altered.
- **A:** Core services were not taken down.

## Target (2013)
- **C:** Payment card data and customer personal information were stolen.
- **I:** Malware was installed on POS systems, so system integrity was compromised.
- **A:** Stores kept operating.

## Colonial Pipeline (2021)
- **C:** Data was stolen before encryption (double extortion).
- **I:** Systems and files were encrypted and unusable.
- **A:** Pipeline operations were halted, causing fuel supply disruption.

## Final Reflection

Researching these three cybersecurity incidents helped me understand how different security weaknesses can lead to serious consequences. Equifax demonstrated the risks of failing to patch known vulnerabilities, Capital One showed the importance of securing cloud infrastructure, and Colonial Pipeline demonstrated how ransomware can disrupt critical business operations.

As someone learning cybersecurity and working towards a SOC Analyst role, I found these cases particularly useful because they helped me connect theoretical concepts such as the CIA Triad, vulnerability management, access control, threat detection, and incident response with real-world security incidents.