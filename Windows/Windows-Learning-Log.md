# Windows Learning Log

This document records my progress while learning Windows administration, security, and PowerShell.

---

## Entry 001 - Introduction to Windows

**Date:** 21 July 2026

**Focus:** Understanding the Windows operating system, its role in cybersecurity, and basic system information gathering.

### Topics Covered

- Windows Desktop vs Windows Server
- Evolution of Windows operating systems
- Active Directory introduction
- Windows versioning
- Windows support lifecycle
- Windows Management Instrumentation (WMI)
- PowerShell `Get-WmiObject`

### Commands Practised

- `Get-WmiObject -Class Win32_OperatingSystem | Select Version, BuildNumber` - Display the Windows version and build number.
- `Get-WmiObject -Class Win32_Process` - List running processes.
- `Get-WmiObject -Class Win32_Service` - List installed services.
- `Get-WmiObject -Class Win32_BIOS` - Display BIOS information.

### Reflection

I began learning Windows fundamentals and why they are essential for penetration testing. Since Windows is one of the most widely deployed operating systems in enterprise environments, understanding its administration, security features and common components is crucial for both attacking and defending systems.

I learned the distinction between Windows Desktop and Windows Server editions, the significance of technologies such as Active Directory, and why security professionals need to recognise supported and legacy versions of Windows. I also had my first exposure to Windows Management Instrumentation (WMI) and learned how PowerShell can be used to retrieve information about the operating system, processes, services and BIOS.

### Next Steps

- Continue the Windows Fundamentals module.
- Learn the Windows file system and directory structure.
- Become familiar with common administrative tools and PowerShell.

---

## Entry 002 - Local & Remote Access

**Date:** 27 July 2026

**Focus:** Understanding how Windows systems are accessed locally and remotely.

### Topics Covered

- Local access
- Remote access
- VPN
- SSH
- FTP
- VNC
- Windows Remote Management (WinRM)
- Remote Desktop Protocol (RDP)
- Managed Service Providers (MSPs)
- Managed Security Service Providers (MSSPs)

### Reflection

I learned the distinction between local and remote access to Windows systems. Local access involves interacting directly with a device using physical peripherals such as a keyboard, mouse and monitor, whereas remote access allows a system to be managed over a network.

The lesson introduced several common remote administration technologies, including VPNs, SSH, FTP, VNC, WinRM and RDP, each of which provides different methods for connecting to and managing remote systems.

I also spent additional time learning about Managed Service Providers (MSPs) and Managed Security Service Providers (MSSPs), as these were new concepts to me. I now understand that MSPs primarily provide outsourced IT support and infrastructure management, while MSSPs focus specifically on cybersecurity services such as monitoring, threat detection and incident response.

### Next Steps

- Continue the Windows Fundamentals module.
- Learn when each remote access technology is commonly used.
- Build a stronger understanding of Windows administration and enterprise environments.

---

## Entry 003 - Windows Client Support & Troubleshooting Methodology

**Date:** 11 August 2026

**Focus:** Understanding enterprise desktop support environments and structured approaches to troubleshooting Windows client issues.

### Topics Covered

- Enterprise Desktop Support Technician (EDST) responsibilities
- Tier 1 and Tier 2 technical support
- Workgroups and peer-to-peer networks
- Windows domains and Domain Controllers
- Active Directory Domain Services (AD DS)
- Cloud and hybrid environments
- Microsoft 365 and Azure
- Incident classification and prioritisation
- Troubleshooting and diagnostic testing
- Problem escalation
- Incident documentation and reporting
- Problem resolution and closure
- Change and rollback planning

### Reflection

Today I completed Microsoft's **Explore Troubleshooting Methodologies** module within the MD-100 Support the Windows Client Environment learning path, including the module assessment.

I learned more about how technical support operates within an organisation and the role of an Enterprise Desktop Support Technician as both a troubleshooter and an escalation point for issues that cannot be resolved at the initial help-desk level.

I also developed my understanding of different Windows environments. Workgroups use decentralised local accounts, while domains provide centralised identity and resource management through Domain Controllers and Active Directory Domain Services. I also explored how organisations can use cloud services such as Microsoft 365 and Azure alongside traditional on-premises infrastructure.

A major focus was structured troubleshooting. I learned the importance of accurately defining and classifying a problem before attempting fixes, testing potential causes systematically, documenting troubleshooting attempts, and escalating issues with sufficient information when necessary. Once a solution is identified, changes should be assessed and tested with consideration given to their potential impact and how they could be rolled back if unsuccessful.

The module reinforced that troubleshooting is not simply about finding a technical fix. Good IT support also requires communication, documentation, prioritisation, appropriate escalation and retaining ownership of an incident through to resolution.

### Next Steps

- Continue developing Windows client support knowledge through Microsoft Learn.
- Gain practical experience troubleshooting common Windows issues.
- Develop my understanding of Active Directory and domain environments.
- Continue building familiarity with Microsoft 365 and Azure.
