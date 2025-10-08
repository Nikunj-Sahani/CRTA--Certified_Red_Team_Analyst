<h1 align="center">🔺 Introduction to Red Teaming 🔺 </h1>

---
## A Red Team tests an organization’s infrastructure by simulating attacks.

Attacks performed by Red Teams are divided into **3 groups:**
- **Cyber** (Digital Attacks includes Web, Network & other Cloud technologies)
- **Social Attacks** (Exploiting people’s behaviour)
- **Physical** (Attacks involving physical man-power)

A Red Team will try to get in and access sensitive information in any way possible, without leaving traces.

---
## Penetration Testing vs Red Teaming

- > Penetration testing finds technical vulnerabilities & checks what can be exploited, while
- > Red Teaming tests how well an organization can detect and respond to real attacks.

|  Pentesting   | Red Teaming |
|---------------|-------------|
| Scope is limited – 1 to 2 specific systems or networks | Specific part of (or the entire ) organization |
| May not test where it isn’t told to go | attempts to compromise everywhere; pivots and changes strategy,if needed |
| Uses Tools present at that time during testing | Constantly researching new exploits, vulnerabilities , Implement attack with new tools as soon as it is discovered |

---
## Red Team Attack Lifecycle
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
## Red Team Infrastructure

- [ ] **C2 Server :** It used by attackers to maintain communications with compromised systems within a target network.
- [ ] **Payload Server :** A controlled host used in authorized red-team exercises to host and deliver test attacks to target systems.
- [ ] **Redirector Server :** A redirector is a system that proxies all traffic to your command and control server.

