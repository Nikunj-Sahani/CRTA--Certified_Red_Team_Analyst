<h1 align="center">‼️ Red Team Lab Setup ‼️</h1>

---
### *Required the Setup first*
## 1. VM Ware Setup
## 2. Kali Linux Setup

---

## 🚀 Metasploitable Setup
I have to Download the Metasploitable from Official Website.

- The Link is here the Download
> - [ Download - Metasploitable ](https://sourceforge.net/projects/metasploitable/)


<div style="text-align: center;"><img src="https://github.com/Nikunj-Sahani/CRTA--Certified_Red_Team_Analyst/blob/main/Study%20Material/Images/EI-1.png" alt="Sample Image"></div>

---
## Linux & Metasploitable
You can see here, the both machine are setup successfully.
 - If you don't know How to set the linux and metasploitable in VM ware, you can get walkthrough on Youtube.

<div style="text-align: center;"><img src="https://github.com/Nikunj-Sahani/CRTA--Certified_Red_Team_Analyst/blob/main/Study%20Material/Images/EI-2.png" alt="Sample Image"></div>

---
## Virtual Network Setup - External
Open the *VM Ware Virtual Machine*

- In Top Bar ➡️ Edit ➡️ Virtual Network Editor
- Add Network ➡️ Then Add Ip value according to you to assign.
> - **Named as External Network.**
  
 - [ ] **Subnet IP : Your IP**
 - [ ] **Subnet mask : 255.255.255.0**


<div style="text-align: center;"><img src="https://github.com/Nikunj-Sahani/CRTA--Certified_Red_Team_Analyst/blob/main/Study%20Material/Images/EI-3.png" alt="Sample Image"></div>

---
## Virtual Network Setup - Internal

- In Top Bar ➡️ Edit ➡️ Virtual Network Editor
- Add Network ➡️ Then Add Ip value according to you to assign.
> - **Named as Internal Network.**
  
 - [ ] **Subnet IP : 10.10.10.0**
 - [ ] **Subnet mask : 255.255.255.0**
       
<div style="text-align: center;"><img src="https://github.com/Nikunj-Sahani/CRTA--Certified_Red_Team_Analyst/blob/main/Study%20Material/Images/EI-4.png" alt="Sample Image"></div>

---
## Run Machine - Metasploitable
Run and Logged in the Machine by default username and Password.
  > - **msfadmin & msfadmin**
- Then type a command ➡️ **sudo nano /etc/network/interfaces**
  
<div style="text-align: center;"><img src="https://github.com/Nikunj-Sahani/CRTA--Certified_Red_Team_Analyst/blob/main/Study%20Material/Images/EI-5.png" alt="Sample Image"></div>

---
## Edit Network Interfaces
You have to edit the network that you want to assign.

#The primary network interface
- **#External**
- [ ] auto eth0
- [ ] iface eth0 inet static
- [ ] address *Your IP*
- [ ] netmask 255.255.255.0
- [ ] gateway 192.168.50.1
- **#Internal**
- [ ] auto eth1
- [ ] iface eth1 inet static
- [ ] address 10.10.10.5
- [ ] netmask 255.255.255.0
- [ ] gateway 10.10.10.1

CTRL + X ➡️  Save the Edit
<div style="text-align: center;"><img src="https://github.com/Nikunj-Sahani/CRTA--Certified_Red_Team_Analyst/blob/main/Study%20Material/Images/EI-6.png" alt="Sample Image"></div>

---
## Network Restart After Setup
You give some commands to restart the Network you saved.

- Here is the command -
> - **sudo /etc/init.d/networking restart**
> - *Restart successfully and setup done.*

<div style="text-align: center;"><img src="https://github.com/Nikunj-Sahani/CRTA--Certified_Red_Team_Analyst/blob/main/Study%20Material/Images/EI-7.png" alt="Sample Image"></div>

---

<div style="text-align: center;"><img src="https://github.com/Nikunj-Sahani/CRTA--Certified_Red_Team_Analyst/blob/main/Study%20Material/Images/EI-8.png" alt="Sample Image"></div>
