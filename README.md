<h1>Active Directory Home Lab</h1>

 ### Visual Representation

<img src="https://i.imgur.com/qhbPkBx.png" height="80%" width="80%" />
 

<h2>Description</h2>

In this project, I’ve created a home lab environment to explore and practice Active Directory (AD) concepts. Let’s break down the steps:

1. Oracle VirtualBox Installation:
   - Begin by downloading and installing Oracle VirtualBox. This virtualization software will allow us to create and manage virtual machines (VMs) within our lab environment.

2. Operating System ISOs:
   - Obtain the **Windows 10** and **Windows Server 2019** ISO files. These will serve as the installation media for our VMs.
   - We'll install each operating system on separate VMs.

3. Creating the Domain Controller (DC):
   - Create your first VM, which will act as the domain controller (DC). The DC hosts Active Directory (AD) and manages user authentication.
   - Configure two network adapters for this VM:
     - One adapter connects to the external internet.
     - The other connects to a private network within VirtualBox (where client VMs will connect).

4. Installing Windows Server 2019 on the DC:
   - Install Windows Server 2019 on the DC VM.
   - Assign IP addresses for the internal network (the external network will get IPs from your home router).

5. Configuring Active Directory:
   - Name the server.
   - Install Active Directory services.
   - Create your domain.
   - Configure routing so that clients on the private network can access the internet through the DC.

6. Setting Up DHCP:
   - Configure DHCP on the DC. This ensures that when we create a Windows 10 client VM, it automatically receives an IP address.

7. PowerShell Script for User Creation:
   - Before creating client VMs, run a PowerShell script.
   - This script will automatically create a thousand users in Active Directory.
   - Explore the script to understand how PowerShell can be used for automation and administration tasks.


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 
- <b>Oracle VirtualBox</b>

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)

<h2>Program walk-through:</h2>

<p align="center">
Launch the utility: <br/>
<img src="https://i.imgur.com/OnPwWBa.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Select the disk:  <br/>
<img src="https://i.imgur.com/8LN8i85.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Enter the number of passes: <br/>
<img src="https://i.imgur.com/mpmbmrl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Confirm your selection:  <br/>
<img src="https://i.imgur.com/kZ1tcP7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Wait for the process to complete (may take some time):  <br/>
<img src="https://i.imgur.com/oCZkGNK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/evNgchL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
