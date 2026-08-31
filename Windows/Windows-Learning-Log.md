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

---

## Entry 004 - Windows Architecture & Client Devices

**Date:** 30 August 2026

**Focus:** Understanding Windows client hardware considerations and the fundamental architecture of the Windows operating system.

### Topics Covered

- Windows client device form factors
- Hardware and support considerations
- Device drivers
- Windows operating system architecture
- Windows Kernel
- System services
- Executive services
- Application Programming Interfaces (APIs)
- Win32 APIs
- Windows Runtime (WinRT) APIs
- Microsoft .NET Framework
- Universal Windows Platform (UWP)
- Relationship between applications, services, the kernel and hardware

### Windows Architecture

I learned that Windows can be viewed as several interacting layers:

**Applications**
- User-facing software operates at the upper level of Windows.
- Applications communicate with Windows through APIs rather than directly controlling hardware.
- Traditional desktop applications can use technologies including Win32 and .NET, while Windows Runtime provides APIs associated with modern Windows applications.

**System Services**
- Services perform operating system functions without requiring direct user interaction and can start before a user signs in.
- Windows executive services provide core functionality such as I/O and virtual memory management.
- Services generally interact with other software components, whereas device drivers provide an interface to hardware.

**Windows Kernel**
- The kernel is a fundamental part of the operating system that operates between higher-level Windows components and the computer's hardware.
- It works closely with low-level device drivers and manages access to resources including the CPU and memory.
- The kernel and low-level drivers initialise early during the Windows boot process.

**Hardware**
- At the lowest level are physical resources such as the CPU, memory, storage and other hardware devices.
- Device drivers allow Windows to communicate with and control hardware.

### Client Device Considerations

I also explored how supporting Windows devices varies depending on their hardware and form factor.

Important considerations include:

- Processor performance
- Available memory
- Storage capacity
- Battery life
- Graphics capabilities
- Displays and external monitors
- USB and other expansion devices
- Driver compatibility
- Cloud storage and synchronisation
- Security implications of removable and personally owned devices

Different devices therefore introduce different support requirements rather than Windows support being identical across every computer.

### Reflection

Today I completed approximately the first half of Microsoft's **Explore Windows Architecture** module.

Although the amount of course material completed was relatively small, I spent additional time researching concepts introduced by the architecture section rather than moving on without properly understanding them.

In particular, I explored the **Windows Kernel, APIs, Win32, Windows Runtime and .NET Framework** in greater depth. This helped me understand the architecture as a connected system rather than simply memorising terminology.

My main takeaway is that applications do not need to understand how to directly control every piece of hardware. Applications can request functionality through APIs and Windows components, with lower levels of the operating system ultimately managing the necessary system resources and hardware interaction.

This has given me a much clearer mental model of what is happening underneath the Windows applications I use every day.

### Next Steps

- Complete the remainder of the Explore Windows Architecture module.
- Study the Windows Registry and Registry Editor.
- Continue developing my understanding of Windows system services and processes.
- Reinforce the relationship between applications, APIs, operating system components, drivers and hardware.

---

## Entry 005 - Windows Registry Fundamentals

**Date:** 31 August 2026

**Focus:** Understanding the structure, purpose and administration of the Windows Registry.

### Topics Covered

- Purpose of the Windows Registry
- Registry hives
- Keys and subkeys
- Registry values and data types
- `HKEY_LOCAL_MACHINE` (HKLM)
- `HKEY_CURRENT_USER` (HKCU)
- `HKEY_USERS`
- `HKEY_CLASSES_ROOT`
- `HKEY_CURRENT_CONFIG`
- Registry Editor (`regedit`)
- `.reg` files
- Registry import and export
- PowerShell registry management
- Group Policy Preferences
- Registry backup and recovery considerations
- Remote registry management

### Registry Structure

I learned that the Windows Registry is a hierarchical database used to store user and computer configuration settings.

Its structure can be understood as:

- **Hives** - Top-level sections of the registry
- **Keys and subkeys** - Containers used to organise related settings
- **Values** - Individual configuration settings stored within keys

The main hives covered were:

- **HKEY_LOCAL_MACHINE (HKLM)** - Stores computer-wide configuration.
- **HKEY_CURRENT_USER (HKCU)** - Stores configuration for the currently signed-in user.
- **HKEY_USERS** - Stores configuration information for users who have signed in locally.
- **HKEY_CLASSES_ROOT** - Contains file association and application-related information.
- **HKEY_CURRENT_CONFIG** - Contains information about the hardware profile used during startup.

### Registry Value Types

I was introduced to several common registry value types:

- `REG_BINARY` - Raw binary data.
- `REG_DWORD` - 32-bit numerical values.
- `REG_SZ` - Fixed-length text strings.
- `REG_EXPAND_SZ` - Text strings that can contain variables.
- `REG_MULTI_SZ` - Multiple text strings stored within one value.

I learned that registry changes must use the correct path, value name and data type, as inaccurate changes can cause applications, devices or even Windows itself to behave incorrectly.

### Registry Administration

I learned several ways to manage the registry:

- **Registry Editor (`regedit.exe`)** for direct manual changes.
- **`.reg` files** for importing predefined registry changes.
- **PowerShell** for navigating and modifying registry data programmatically.
- **Group Policy Preferences** for deploying registry changes across many devices in an Active Directory environment.

Example PowerShell commands included:

`Set-Location HKCU:\Software\Example`

`Set-ItemProperty . examplevaluename "assigned value"`

I also learned that the registry can be treated like a filesystem through PowerShell's registry provider.

### Safe Registry Management

A major takeaway was the importance of caution when modifying the registry.

Before making changes, good practice includes:

- Backing up the affected registry key.
- Exporting relevant registry data.
- Creating a restore point where appropriate.
- Confirming the exact registry path and value type.
- Testing changes before deploying them widely.

Incorrect registry changes can cause serious system instability or prevent Windows from starting.

### Reflection

Completing this section reinforced how important the Windows Registry is to understanding Windows administration and troubleshooting.

The registry is not simply another configuration tool; it is a central database that affects users, applications, services, drivers, hardware behaviour and the operating system itself. Because of this, mistakes can have much greater consequences than changing a normal application setting.

I also recognised how relevant registry knowledge is to both IT support and cybersecurity. Troubleshooting may require identifying incorrect or damaged configuration values, while security analysis can involve examining locations used for persistence, startup behaviour, services and user configuration.

This is an area I expect to revisit in significantly more detail. I understand the overall structure and purpose of the registry now, but I want to become much more comfortable navigating it, recognising important paths and making controlled changes using both Registry Editor and PowerShell.

For that reason, I consider this one of the more important Windows fundamentals modules I have completed so far rather than something I intend to study only once.

### Next Steps

- Revisit Windows Registry concepts as my Windows knowledge develops.
- Practise navigating the registry safely in a lab environment.
- Learn common registry locations used for Windows startup and services.
- Gain more experience using PowerShell to read and modify registry values.
- Explore how the registry is used during troubleshooting and security investigations.
