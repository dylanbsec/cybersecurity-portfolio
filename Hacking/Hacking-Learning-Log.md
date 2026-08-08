# Hacking Learning Log

This file tracks my practical cybersecurity learning through labs, challenges and hands-on exercises.

---

## Entry 001 - Introduction to Offensive Security

**Platform:** TryHackMe

**Date:** 9 July 2026

**Room:** Offensive Security Intro  

**Focus:** Web enumeration and hidden application functionality

### What I Learned

Offensive security involves approaching systems from the perspective of an attacker. By understanding how systems can be exploited, security professionals can identify weaknesses and improve their defences.

Ethical hacking applies these techniques within legal and authorised environments to identify vulnerabilities without causing harm.

### Practical Exercise

I completed my first TryHackMe room and performed a basic web enumeration exercise against the fictional FakeBank application.

The objective was to identify hidden functionality within the website that was not accessible through the normal user interface.

I used the `dirb` command-line tool to perform directory and page enumeration:

dirb http://fakebank.thm

DIRB used a wordlist containing common directory and page names and tested these against the target website.

The scan identified a hidden page:

/bank-deposit

This page exposed functionality that allowed funds to be added directly to a bank account.

I accessed the hidden page and used the exposed functionality to modify the balance of the provided account, successfully completing the exercise.

---

## Entry 002 - OSINT & Linux Practice

**Focus:** Open Source Intelligence (OSINT) and Linux command-line practice

### What I Learned

Today I explored two different areas of practical cybersecurity.

The first involved experimenting with **SpiderFoot**, an Open Source Intelligence (OSINT) tool that automates the collection of publicly available information about a target.

I investigated how SpiderFoot can identify information such as:

- Email addresses
- Usernames
- Associated online accounts
- Publicly available breaches
- Domain information
- Digital footprint information

This reinforced how much information can be gathered from public sources without directly interacting with a target system.

I also spent time playing **Hacknet**, using it as a way to practise Linux terminal commands within a game-based environment.

### Key Concepts

- Open Source Intelligence (OSINT)
- Digital footprint
- Passive reconnaissance
- Linux command line
- File transfer
- Process management

### Reflection

Although Hacknet is a game, it encouraged me to think more naturally about navigating a Linux terminal and using commands to accomplish objectives rather than simply memorising syntax.

Using SpiderFoot also highlighted the importance of publicly available information and how attackers can build profiles of organisations or individuals before attempting further attacks.

### Next Steps

- Continue exploring SpiderFoot modules.
- Learn additional Linux commands through practical use.
- Develop a stronger understanding of reconnaissance techniques.

---

## Entry 003 - Hack The Box: Meow

**Date:** 20th July 2026

**Focus:** Introduction to enumeration and gaining an initial foothold on a target machine.

### Topics Covered

- Network connectivity testing (`ping`)
- Enumeration
- Port scanning with `nmap`
- Service detection
- Telnet
- Default and blank credentials
- Initial foothold

### Reflection

Today I completed my first Hack The Box lab, **Meow**, which introduced the importance of enumeration during a penetration test.

I began by confirming connectivity to the target machine using `ping` before scanning it with `nmap` to identify open ports and running services. The scan revealed that **Telnet** was running on port **23**, allowing me to investigate the service further.

After researching Telnet and understanding its purpose as a remote management protocol, I attempted authentication using common default account names. I successfully gained access by exploiting a weak configuration that allowed a privileged account to authenticate without a password.

The biggest lesson from this lab wasn't the exploitation itself, but the importance of carefully reading instructions and understanding the environment. I spent considerably longer troubleshooting than necessary because I confused my local Kali Linux filesystem with the target host's filesystem. Once I realised my mistake and followed the instructions more carefully, the remainder of the lab made much more sense.

### Next Steps

- Continue the Hack The Box Starting Point labs.
- Develop stronger enumeration habits before attempting exploitation.
- Improve my understanding of remote services and Linux file systems.

---

## Entry 004 - Hack The Box: Fawn

**Date:** 8 August 2026

**Focus:** FTP enumeration and exploiting anonymous access on a misconfigured Linux machine.

### Topics Covered

- File Transfer Protocol (FTP)
- FTP port 21
- FTP vs SFTP
- Network connectivity testing with `ping`
- Service enumeration
- Anonymous FTP authentication
- FTP response codes
- Navigating an FTP server
- Downloading files from a remote server

### Commands Practised

- `ping` - Test connectivity to the target using ICMP.
- `ftp -?` - Display help for the FTP client.
- `ftp <target>` - Connect to a remote FTP server.
- `anonymous` - Use anonymous authentication where permitted by the FTP server.
- `ls` - List files available on the FTP server.
- `get <filename>` - Download a file from the FTP server.

### Reflection

Today I completed the Hack The Box **Fawn** machine, which introduced FTP and demonstrated the security risks of allowing anonymous access to an FTP server.

I used enumeration to identify **vsftpd 3.0.3** running on port **21** before connecting to the FTP service. The server was misconfigured to permit anonymous authentication, allowing me to access its contents without possessing a legitimate user account. I then navigated the FTP server and used `get` to retrieve the target file and complete the machine.

My previous Linux practice definitely helped with this lab. Commands such as `ping` and `ls` were already familiar, which meant I could concentrate more on understanding FTP and the vulnerability being exploited.

I completed Fawn using some hints and a walkthrough where needed. I am still finding connectivity to Hack The Box machines frustrating at times, as troubleshooting the connection can take time away from the actual lab. However, this is also giving me more experience distinguishing between problems with my own environment, the VPN connection and the target itself.

### Next Steps

- Continue the Hack The Box Starting Point machines.
- Learn more about FTP enumeration and common misconfigurations.
- Become more confident troubleshooting HTB connectivity independently.
