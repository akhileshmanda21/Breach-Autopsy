# Defence in depth

| Layer | Example control | Threat addressed | Validation / evidence |
|---|---|---|---|
| Perimeter | Router firewall, strong Wi-Fi encryption (WPA2/WPA3), disabled remote administration and updated router firmware | Unauthorized external access, network intrusion and attacks against the home network | Router firewall settings, Wi-Fi security configuration and firmware version screenshot |
| Network | VMware Host-only networking for isolated labs, NAT when internet access is required, network segmentation and Windows Firewall rules | Unauthorized network access, lateral movement and communication between untrusted systems | VMware network adapter settings, IP configuration (`ipconfig`) and firewall rules |
| Host | Windows Defender Antivirus, Windows Firewall, regular Windows updates and endpoint protection | Malware infection, exploitation of vulnerabilities and unauthorized system changes | Windows Security status, `Get-NetFirewallProfile` and Windows Update history |
| Identity and access | Strong unique passwords, standard user accounts, least privilege, MFA where supported and disabled unused accounts | Credential theft, brute-force attacks and privilege abuse | `Get-LocalUser`, account membership review and MFA configuration screenshots |
| Application and data | Updated applications, secure configuration, restricted shared folders, strong authentication and encrypted backups | Application exploitation, data theft, unauthorized file access and data loss | Application version checks, VMware shared-folder settings and backup configuration |
| Monitoring and response | Wazuh SIEM, Sysmon, Windows Event Logs, centralized log collection, alert rules and an incident response procedure | Undetected malicious activity, suspicious logins, malware execution and delayed incident response | Wazuh dashboard screenshots, Sysmon events, Windows Event Viewer logs and sample detection alerts |
