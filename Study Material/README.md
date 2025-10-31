<h1 align="center"> ⭕ Red Team Virtual Machine Setup ⭕ </h1>

---
### VM WARE 👑 ....... [ ⏏️ Click to Download ⏏️ ](https://www.vmware.com/products/desktop-hypervisor/workstation-and-fusion)
---
### Topics

 - **Virtual Machines Required**
 - **Download link of Virtual Machine**
 - **IP assigning**
 - **Domain Joining**

---
## Virtual Machines

#### 🧑‍💻 1. Kali Linux 🎩......................... [ ♨️ Click to Download ♨️ ](https://cdimage.kali.org/kali-2025.3/kali-linux-2025.3-installer-amd64.iso) :::
#### 🧑‍💻 2. Metasploitable 2 📼.............. [ ♨️ Click to Download ♨️ ](https://sourceforge.net/projects/metasploitable/) ::: 
#### 🧑‍💻 3. Windows 10 : 2022 🪟........... [ ♨️ Click to Download ♨️ ](https://www.microsoft.com/en-in/software-download/windows10) ::: [ 💾 Direct Download 💾 ](https://drive.google.com/file/d/1JoBTJiUI6G0bRBezGUmaXtfYv73YpZ8l/view?usp=drive_link)
#### 🧑‍💻 4. Windows Server : 2016 🏢..... [ ♨️ Click to Download ♨️ ](https://www.microsoft.com/en-us/evalcenter/download-windows-server-2016) ::: [ 💾 Direct Download 💾 ](https://drive.google.com/file/d/13YYix0s5lnAKM-59ROC7mcepEmtOhS9L/view?usp=drive_link)
#### 🧑‍💻 5. Windows Server : 2012 🌆..... [ ♨️ Click to Download ♨️ ](https://www.microsoft.com/en-us/evalcenter/download-windows-server-2012-r2) ::: [ 💾 Direct Download 💾 ](https://drive.google.com/file/d/1i-qz3r_jtAHD8enanv4m9ZikaRelHTXy/view?usp=drive_link)

---
## IP Assigning

#### Kali Linux 
- *Network Adapter - External*
- IP configured - **192.168.50.2**

#### Metasploitable - 🎪 Web Server 🎪
- *Network Adapter - External & Internal*
- IP configured - Set with Virtual Network
- 📡External ➡️ **192.168.50.3**
- 📡Internal ➡️ **10.10.10.5**
  
#### Windows 10 : 2022 - 🎪 Employee-Machine 🎪
- *Network Adapter - Internal*
- IP configured - **10.10.10.4**
  
#### Windows Server : 2016 - 🎪 Domain-Controller 🎪
- *Network Adapter - Internal*
- IP configured - **10.10.10.2**

#### Windows Server : 2012 - 🎪 Application-Server 🎪
- *Network Adapter - Internal*
- IP configured - **10.10.10.3**

---
## Domain Joining

#### Windows Server 2016 - Domain Controller
- Domain Created here.
- Domain - **cyberwarfare.corp**

#### Winodws 10 - Employee Machine
- Domain Connect here in system Setting
- Type Domain Name - **cyberwarfare.corp**
- Enter* Username & Password*
> - Connected & Joined.

#### Winodws 2012 - App Server
- Domain Connect here in system Setting
- Type Domain Name - **cyberwarfare.corp**
- Enter* Username & Password*
> - Connected & Joined.

---
---
