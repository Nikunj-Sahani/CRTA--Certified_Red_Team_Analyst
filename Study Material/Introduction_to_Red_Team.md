<h1 align="center">🔺 Introduction to Red Teaming 🔺 </h1>

#### Session INTRO - 1
---
    > - || 𝗙𝗼𝗿 𝘁𝗵𝗲 𝗳𝘂𝗹𝗹 𝗰𝗼𝗻𝘁𝗲𝗻𝘁, 𝗽𝗹𝗲𝗮𝘀𝗲 𝗿𝗲𝗮𝗰𝗵 𝗼𝘂𝘁 𝘃𝗶𝗮 𝗟𝗶𝗻𝗸𝗲𝗱𝗜𝗻 𝗼𝗿 𝗜𝗻𝘀𝘁𝗮𝗴𝗿𝗮𝗺 𝗮𝗻𝗱 𝗜’𝗹𝗹 𝗽𝗿𝗼𝘃𝗶𝗱𝗲 𝘆𝗼𝘂.||
 
---

## A Red Team tests an organization’s infrastructure by simulating attacks.

Attacks performed by Red Teams are divided into **3 groups:**
- **Cyber** (Digital Attacks includes Web, Network & other Cloud technologies)
- **Social Attacks** (Exploiting people’s behaviour)
- **Physical** (Attacks involving physical man-power)

A Red Team will try to get in and access sensitive information in any way possible, without leaving traces.

---
## ✍️ Penetration Testing vs Red Teaming

- > Penetration testing finds technical vulnerabilities & checks what can be exploited, while
- > Red Teaming tests how well an organization can detect and respond to real attacks.

|  Pentesting   | Red Teaming |
|---------------|-------------|
| Scope is limited – 1 to 2 specific systems or networks | Specific part of (or the entire ) organization |
| May not test where it isn’t told to go | attempts to compromise everywhere; pivots and changes strategy,if needed |
| Uses Tools present at that time during testing | Constantly researching new exploits, vulnerabilities , Implement attack with new tools as soon as it is discovered |

---
## ✍️ Red Team Attack Lifecycle
High-level overview & Steps of Red Team Attack lifecycle.

- [ ] 1. Extensive OSINT
- [ ] 2. Initial Access & Execution
- [ ] 3. Persistance & Priviledge Exclation
- [ ] 4. Lateral Movement with Defensive Evasion
- [ ] 5. Discovery & Data collection
- [ ] 6. Data Exfilteration & high level persistance

#### Extensive OSINT
It deals with gathering more and more information about the target organization.
- Social media sites, platforms where employees are generally active are of primary focus.
- Tries to find out **sensitive information available in the internet.**

#### Initial Access & Execution
Initial Access consists of using various entry vectors to*gain access within the internal network.*
- There are ways like *exploitation to External Remote Services,* mis-configurations in Web Applications which may lead as gateway to the internal network.

#### Persistance & Priviledge Exclation
Attackers always look for hidden techniques to keep access to systems across restarts.
> - **Examples :** Resetting password of a low-profile user & using it as a **backdoor to network.**

Privilege escalation is gaining *higher-level permissions on a system or network.*
- Elevated Access Accounts: -
     > - **SYSTEM/root level**
     > - **Local Administrator**

#### Lateral Movement with Defensive Evasion
When an attacker gains control of one system and then moves through network to **compromise other connected systems with same network.**
- Attacker can do these types of things in other system
   > - Internal Phishing & Remote Services

Defensive Evasion deals with **avoiding detection throughout the compromise.**
> - Attackers *bypass detection by malicious scripts,* hiding in trusted processes, and disabling security software etc.
> - Understanding how an attacker can avoid network defenders

#### Discovery & Data collection
Attacker head for situational awareness where they try to **figure out organization environment** & orient themselves before deciding how to act.
- Attackers enumerate files and directories or may search in specific locations of a host or network

**Data collection** is the process of gathering and measuring information from established system.
- The data collected can be any **sensitive information present in a system/network**
   > - Archive Collected Data
   > - Clipboard Collected Data

#### Data Exfilteration
Once all the critical data has been identified and packed, attackers will try to **steal data from the computer/network.**
- Attackers can also **compress and encrypt the collected data.**
   > - Automated Exfiltration
   > - Exfiltration over Physical Medium

---
## ✍️ Red Team Infrastructure

- [ ] **C2 Server :** It used by attackers to maintain communications with compromised systems within a target network.
- [ ] **Payload Server :** A controlled host used in authorized red-team exercises to host and deliver test attacks to target systems.
- [ ] **Redirector Server :** A redirector is a system that proxies all traffic to your command and control server.

- **Adversary Emulation :**
   - Detailed, technical test that **mimics/copy real attacker techniques** and behavior (TTPs) using frameworks like MITRE ATT&CK.

- **Adversary Simulation :**
   - Safe test that imitates attacker goals to check detection and response — **not real attack steps.**

---
### APT (Advanced Persistent Threat) :
A targeted, ***long-term cyber attack** where skilled hackers secretly enter a network, **stay hidden, and continuously steal sensitive data** or spy on the organization.

### DMZ (Demilitarized Zone) :
   - DMZ = Buffer zone *between Internet and internal network.*
   - **Protects internal systems** if public servers get attacked.

### MZ (Militarized Zone) :
   - The internal *secure network zone of an organization.*
   - The area inside the firewall, where trusted systems and **sensitive data are stored.**

### Tactics, Techniques and Procedures (TTPs) :
TTPs explains how threat actors manage cyber-attacks.

> - **“Tactic”** is the *highest-level description* of threat actor behaviour.
> - **"Techniques"** give a *more detailed description of behaviour* in the context of a tactic
> - **“Procedures”** an even *lower-level,* highly detailed description in the context of a technique.

---
## ✍️ Listener for Connection :
Listener waits for an incoming connection from the target machine.
- **In our lab scenario,**
    - we will listen on our Kali machine and the target machine can *connect back to our machine after successful exploitation.*

## Exploitation :
Taking advantage of a software, system, or human weakness **(vulnerability) to gain unauthorized access** by run code or steal data.

---
## ✍️ Paylaods S.S.S :

- **Singles :** Self-contained payload assigned to **do a specific task.**
    > *Example :* payload/windows/adduser

- **Stagers :** The payload are used to **download large payload to the target machine** from the attacker machine.
    > *Example :* payload/windows/shell/bind_tcp

- **Stages :** These are the large **payload downloaded by the stagers & then executed.**
    > *Example :* payload/windows/shell/bind_tcp

---
### Shells :
A shell is a program/interface to run OS commands (e.g., bash, sh, PowerShell, cmd).

> - **Common types (brief):**
  - [ ] **Local interactive shell :** Direct terminal on the machine (bash, zsh).
  - [ ] **Remote shell (legit):** Authorized remote access (SSH).
  - [ ] **Reverse shell :** Target connects back to attacker (used in attacks).
  - [ ] **Bind shell :** Target listens for attacker to connect (used in attacks).
  - [ ] **Web shell :** Script on a webserver that executes commands (common post-compromise).
  - [ ] **Agent/implant shells :** Advanced post-exploitation agents (e.g., Meterpreter).

---
#### Session INTRO - 2

## ENTERPRISE NETWORK
Enterprise Network consists of various role-assigned servers.

- **Web server :** It delivers web pages and content to users over the internet using HTTP or HTTPS.
> - *Ex -* HTML, images, APIs, etc.

- **Mail-Server :** A mail server sends, receives, and stores emails over the internet for users and domains.
> - SMTP is used when e-mails are delivered.

- **Database server :** It stores, manages, and provides access to data for other computers or applications.
> - It allows users to access data across the network.

- **Jump server (or jump host) :** A secure gateway server used to access and **manage devices or servers in a protected network.**
> - Typically accessed using SSH or RDP.

- **Automation server :** It Automatically runs tasks, scripts, or workflows without manual intervention.
> - *Ex -* Jenkins Server, TeamCity, Bamboo

---
## Active Directory 
Active Directory (AD) is a Microsoft service that stores and manages user accounts, computers, and network resources, enabling authentication and access control in a Windows network.

- **Active Directory Forest -** Forest is a single instance of Active Directory.
- **Active Directory Domains -** It can be thought as containers within the scope of a Forest.

### Active Directory Objects
The physical entities that make up an organized network

> - **Domain Users :** User account that are allowed to authenticate to machines/servers in the domain.
> - **Domain Groups (Global Groups) :** It can be used to assign permissions to access resources in any domain.
> - **Domain Computers :** Machines that are connected to a domain and hence become a member of a domain.

**Domain Controller (DC) :** 
- A server in an Active Directory network that authenticates users, enforces security policies, and manages access to domain resources.

---
## Kerberos Authentication
It is a secure network authentication protocol that **uses secret-key cryptography and tickets to verify user identities** without sending passwords over the network.

- A ticket is a form of authentication and authorization token
  - [ ] Ticket Granting Ticket **(TGT) for Authentication**
  - [ ] Ticket Granting Service **(TGS) for Authorization**

---
#### Session INTRO - 3

## Kerberos Delegation
It allows an authenticated domain user credentials to be *re-used to access resources hosted on a different server in a domain.*
> - This utility is useful in **multi-tier applications or architecture.**

**Types of Kerberos Delegation :**
- [ ] **Unconstrained Delegation :** It allows the Application Server to request access to ANY service on any server in the domain.
- [ ] **Constrained Delegation :** It allows the Application Server to request access to ONLY specified services on specific servers.

---
## Technologies Exploitation in Red Teaming

- **Web Technology :** Knowledge of **OWASP Top 10 Web Vulnerabilities** should be known.
- **Network Technology :** Understanding of Network devices like **routers, switches, servers,** computers etc and network protocols.
- **Cloud Technology :** Cloud services like Amazon Web Services (AWS), Microsoft Azure and Google Cloud Platform (GCP).

## Physical Red Teaming :
Red Team develops unique attack situations leveraging manual and automated procedures.
 - **Red Teams are trained** to elude *detection* from one or more of the following security devices:
  - [ ] CCTVs (closed circuit television cameras)
  - [ ] Keypad entry locks
  - [ ] Wireless intercoms/video intercoms
  - [ ] Motion/sensor detects
  - [ ] Single or double deadbolts
  - [ ] Door and window locks
  - [ ] Steel security doors
  - [ ] Remote entry gates

## Wireless Attacks :
The massive rise in cyberattacks via public Wi-Fi networks, open enterprise Wi-Fi campus connected to internal network possess a huge threat.
- **Common Wireless Vulnerabilities:**
  - [ ] Use of Default SSIDs and Passwords
  - [ ] Downgrading the wireless security protocol to WEP and to older WPA version.
  - [ ] WPA2 Krack vulnerability
  - [ ] Fake WiFi Access Points, Evil Twins, and Man in the Middle Attacks
  - [ ] Packet Sniffing
  - [ ] MAC spoofing

---
---
