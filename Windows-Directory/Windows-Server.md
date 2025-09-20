# How to Get Started with Windows Server 2022(Hands-on project)

## What is Windows Server?

 Windows Server is a Microsoft operating system (OS) designed for enterprise and 
data center environments to manage networks, applications, and services.

- Various Server of Windows Server
Windows Server 2003,2008, R2, 2012 & R2, 2016,2019 and 2022
![screenshot](images/screenshot73.jpg)
- **Windows Server Uses**
  
Manage users & computers (Active Directory)
Shares & Security across a folder
DNS & Other Services - Helps Computer find each other on a Network
Virtual machines on one server
![screenshot](images/screenshot74.jpg)
- **Network**
- Active Integration (Remote Desktop Services)
- Group Policy (GPO): Control Setting for multiple Compuers
- WMI (Windows Management Instrumentation)
- Firewall Rules and Software Restrictions
# Setting up Windows Server 2022 on a Virtual Machine 

1. **Download VirtualBox or VMware Workstation Pro**
   - Download Windows host (for Windows) & Extension Pack
   - Download VMware Workstation Pro on the offical website (Browser)
     *(32 or 64bit depending on your computer)*
   - **Download Windows Server 2022 ISO file** *(Free trial)
![Screenshot](images/screenshot75.jpg)
---


2.  **Open your Workstation and click on Create a New Virtual Machine**
    - Click on Typical *(Recommended)*  ➝ Installer disc image file *(Browse the Downloads folder on your PC and click on the ISO file you just downloaded)*  
   - Guest Operating System *(Windows)*  
   - Name the Virtual Machine ➝ Specify Disk capacity *(by default it's 80GB)* ➝ Ready to Create Virtual Machine and Finish
---

- **Once the Virtual Machine is Created**,  click on **Edit Virtual Settings** ➝ CD/DVD (SATA) ➝ Use ISO Image file *(Browse to your downloaded ISO file)* and Select and OK
![Screenshot](images/screenshot1-2.png)

3. **Power on the Virtual Machine**
   - During the booting process, quickly press any key to boot from CD or DVD to load the ISO.
     If you miss it, shut it down and power again. Keep pressing any key to boot.

     
## Installing Windows Server 2022

-The ISO file will prompt Server operating system setup. Click on **Next** ➝ **Install Now**
- Select the operating system you want to install  
  *(Windows Server 2022 Standard Evaluation - Desktop Experience)* ➝ **Next** ➝ Accept terms & conditions ➝  
  Custom: Install Microsoft Server operating system only ➝  
  Installing Microsoft Server operating system...
![Screenshot](images/screenshot.jpg)
### After Installing
- **Username**: administrator *(only default)*
- **Password**:  
- **Re-enter Password**
---
### 3. Renaming the Server to Something Simple

- Navigate to **File Explorer** ➝  
  Right click on **This PC** ➝ **Properties** ➝ **Advanced System Settings** ➝  
  Computer Name tab ➝ Click **Change** ➝ Enter new computer name *(e.g., Server2022)* ➝  
  Click **OK** (it will prompt to restart the machine) ➝  
  **Restart Now**
---
### 4. Create Active Directory Domain Services


-- Navigate to **Server Manager** from the **Start Menu** ➝  
  On the top right, click **Manage** ➝ **Add roles and features**
![Screenshot](images/screenshot2.jpg)
**Before you begin:**
1. Open **Server Manager**.
2. Click **Next**.
3. Select **Role-based or feature-based installation**.
4. Click **Next**.
5. Click on **Active Directory Domain Services**.
6. Click **Add Features**.
7. Click **Next**, then **Install** (wait for it to succeed).
8. Click **Promote this server to a domain controller**.
9. Select **Add a new forest**.
10. Enter the **Root domain name** (e.g., `Njikason.com`).
11. Create a password (e.g., `Password@123`).
12. Click **Next**.
13. Wait for **Prerequisites check**.
14. Click **Install** — it will restart your computer.

> **Note:** Active Directory Users & Computers are now installed in the server.


---
## Creating a Static IP for Server 2022


1. In the search bar, type **Control Panel**.
2. Go to **Network and Internet**.
3. Click **View network status and tasks**.
4. Click **Change adapter settings**.
5. Right-click **Ethernet** > Select **Properties**.
6. Click on **Internet Protocol Version 4 (TCP/IPv4)**.
7. Select **Use the following IP address** and configure the static IP.
![Screenshot](images/screenshot3.jpg)
> In a **corporate environment**, Windows Server usually has a **static IP address**.
---
## whoami command


- Displays the fully qualified Domain Name (Fqdn) of the currently logged- in user, includes domain hierarchy in the output.
- whoami /fqdn
![Screenshot](images/screenshot5.jpg)

## VM Network Configuration

- Change the **virtual machine network** from **NAT** to **Host-only** so that the **VM** can talk to each other on the same network.
![Screenshot](images/screenshot8.jpg)

---
## Adding a Computer to a Domain (Windows) rules

* To enforce/practice with Windows Server (group policy, Active Directory users & Computers, Troubleshooting Skills )

* If it's a new install, for home lab (Renaming the PC will be easy to remember the Computer)  
Click on the Active File Explorer → Properties → change Settings → Computer name → Rename the Computer → Restart the Computer
![Screenshot](images/screenshot.jpg)







