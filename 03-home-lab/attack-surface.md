# Home lab attack surface

| No. | Asset / service | Exposure / entry point | Risk or weakness | Evidence |
|---:|---|---|---|---|
| 1 | Windows 11 Host | Network connections, open ports and running services | Unpatched OS, misconfigured firewall rules or unnecessary exposed services | Windows Update status, `Get-NetFirewallProfile`, `Get-NetTCPConnection` |
| 2 | VMware Workstation | VMware application and virtual machine configuration | Outdated VMware version or insecure VM settings | VMware version and VM settings screenshots |
| 3 | Virtual Machines | Virtual network adapters and running services | Vulnerable operating systems, outdated software or unnecessary services | VM inventory, OS version and service-list output |
| 4 | Administrator Accounts | Local or remote authentication | Weak passwords, excessive privileges or unused administrator accounts | `Get-LocalUser`, Local Users and Groups |
| 5 | Remote Desktop (RDP) | TCP port 3389 and remote login | Unnecessary remote access, weak credentials or insufficient access restrictions | RDP configuration and listening-port output |
| 6 | SSH Service | TCP port 22 and remote authentication | Weak credentials, exposed SSH service or insecure configuration | `Get-Service sshd` or `sudo systemctl status ssh` |
| 7 | VMware Network Adapters | NAT, Bridged and Host-only virtual networks | Bridged networking may expose lab VMs to other devices on the network | VMware Network Adapter settings screenshot |
| 8 | Shared Folders | File sharing between Windows host and VMs | Malware inside a VM could access files shared with the host | VMware Shared Folders settings screenshot |
| 9 | Web Applications | HTTP/HTTPS ports such as 80, 443 or 3000 | Vulnerable applications, weak authentication or unnecessary open ports | Browser test and listening-port output |
| 10 | Wazuh / SIEM Server | Web dashboard, agent communication and management services | Weak dashboard credentials, unrestricted access or exposed management ports | Wazuh configuration, dashboard access settings and port-list output |