# Active Directory (Add Users via PowerShell)
# Project Overview
This project involves setting up a virtualized network using VirtualBox, where a Windows Server 2019 virtual machine (VM) serves as the Domain Controller, hosting Active Directory (AD) for managing user accounts. The Domain Controller is configured with two network adapters: one for external internet access and another for a private network to connect client machines. A DHCP server is set up on the Domain Controller to assign IPs to clients, and NAT and routing are configured to enable clients on the private network to access the internet. A PowerShell script is created to automate the addition of 1,000 users to Active Directory. Additionally, a Windows 10 VM is created as a client, which connects to the private network, logs in using a domain account, and demonstrates successful integration into the domain.

![Screenshot 2025-01-03 202721](https://github.com/user-attachments/assets/69411b4f-465c-49f8-b203-8bd0b2966625)
# 1. Downloaded Content 
- Download and install VirtualBox on your host machine.
- Obtain the Windows 10 ISO and Windows Server 2019 ISO files. These will be used to create the two virtual machines (VMs).
# 2. Create the Domain Controller Virtual Machine
- Set up the first VM, which will act as the Domain Controller (DC) for your network. This machine will host Active Directory (AD).
- Configure the VM with two network adapters:
Adapter 1: Connects to the outside internet, providing external connectivity.
Adapter 2: Connects to a private network, which the client machines will use to connect to the Domain Controller.
# 3. Install Active Directory and Create the Domain
- On the Domain Controller VM, install Active Directory through Windows Server 2019.
- Create a domain within Active Directory for your network. This domain will be used for managing user accounts and authentication.
# 4. Set Up NAT and Routing
- Configure Network Address Translation (NAT) and routing on the Domain Controller so that private clients can access the internet.
- Enable DHCP on the Domain Controller to automatically assign IP addresses to the client machines on the private network.
# 5. Automate User Creation
- Develop a PowerShell script to automatically add 1,000 user accounts to Active Directory. This script will streamline the process of creating a large number of users for the network.
# 6. Create Client Virtual Machine 
- Create the second virtual machine using the Windows 10 ISO.
- Connect this VM to the private network set up in VirtualBox and configure it as Client 1.
- Have the Windows 10 machine log in using one of the domain accounts created earlier in Active Directory, demonstrating that it is successfully integrated into the domain.
