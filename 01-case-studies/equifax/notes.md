# Equifax Breach (2017)

## Summary
In 2017, Equifax suffered a data breach that exposed the personal information of 147.9 million Americans. That’s roughly 40% of the U.S. population.

The attackers exploited a known vulnerability that had a patch available for months. They remained undetected for 78 days because an SSL certificate had expired and nobody noticed. When Equifax finally discovered the intrusion, executives sold stock before going public.

The Equifax breach became a case study in how basic security failures led to catastrophic outcomes. Every failure was preventable with standard practices.

This analysis covers exactly how the attack unfolded and what security teams can learn to prevent similar breaches.

## Timeline
Here’s exactly when each event occurred and how the attack progressed.
| Date | Event |
|---|---|
| March 7, 2017 | Apache discloses CVE-2017-5638 and releases a patch |
| March 10, 2017 | Attackers exploit the vulnerability on the Equifax dispute portal |
| May 13, 2017 | Attackers begin lateral movement and data exfiltration |
| July 29, 2017 | Expired SSL certificate is renewed, and suspicious activity is detected |
| July 30, 2017 | Equifax takes its dispute portal offline |
| August 2017 | Multiple executives sell company stock |
| September 7, 2017 | Equifax publicly discloses the breach |
| September 26, 2017 | CEO Richard Smith resigns |
| February 10, 2020 | DOJ indicts four Chinese military officers |



## Data Breach
The information accessed during the Equifax data breach included:

- First and last names
- Social Security numbers
- Dates of birth
- Addresses
- Driver's license numbers in some cases

According to Equifax's analysis, the breach affected approximately **143 million Americans**.

The breach also compromised information belonging to:

- Approximately **14 million British residents**
- Approximately **8,000 Canadian residents**
- An additional **11,670 Canadian residents**, later disclosed by Equifax

In addition, attackers accessed:

- Credit card numbers belonging to approximately **209,000 U.S. consumers**
- Dispute documents containing personally identifiable information (PII) belonging to approximately **182,000 U.S. consumers**

## Key failures
- Missed patching
- Weak asset inventory
- Plaintext credentials
- Expired inspection certificate (detection gap)