# Active Directory (Add Users via PowerShell)
# Project Overview
This project involves setting up a virtualized network using VirtualBox, where a Windows Server 2019 virtual machine (VM) serves as the Domain Controller, hosting Active Directory (AD) for managing user accounts. The Domain Controller is configured with two network adapters: one for external internet access and another for a private network to connect client machines. A DHCP server is set up on the Domain Controller to assign IPs to clients, and NAT and routing are configured to enable clients on the private network to access the internet. A PowerShell script is created to automate the addition of 1,000 users to Active Directory. Additionally, a Windows 10 VM is created as a client, which connects to the private network, logs in using a domain account, and demonstrates successful integration into the domain.

![](https://github.com/user-attachments/assets/69411b4f-465c-49f8-b203-8bd0b2966625)
# 1. Downloaded Content 
- Download and install VirtualBox on your host machine.
- Obtain the Windows 10 ISO and Windows Server 2019 ISO files. These will be used to create the two virtual machines (VMs).
# 2. Create the Domain Controller Virtual Machine
- Set up the first VM, which will act as the Domain Controller (DC) for your network. This machine will host Active Directory (AD).
- Configure the VM with two network adapters:
Adapter 1: Connects to the outside internet, providing external connectivity.
Adapter 2: Connects to a private network, which the client machines will use to connect to the Domain Controller.

- Use the "Desktop Experience" option during the installation and choose a custom installation file. The default "Administrator" username will appear, and set the password to "Password1" for the account. This will be the password for everything so there is now wasted time! Also the VM will give you trouble on opening the machine w/ CTRL ALT DEL so instead go to the top input-keyboard and click CTRL ALT DEL.

![image](https://github.com/user-attachments/assets/e24c3247-3790-4588-968f-47839427e7e6)

# 3. Install Active Directory and Create the Domain
- On the Domain Controller VM, install Active Directory through Windows Server 2019.
- Create a domain within Active Directory for your network. This domain will be used for managing user accounts and authentication.

![image](https://github.com/user-attachments/assets/399244df-cdb6-4b67-bb31-42a45aa85b7a)
![](https://github.com/user-attachments/assets/135840d6-1124-43db-8886-ec5ed6beabc1)


# 4. Set Up NAT, Routing/RAS, and DHCP
- Configure Network Address Translation (NAT) and routing on the Domain Controller so that private clients can access the internet.
- Enable DHCP on the Domain Controller to automatically assign IP addresses to the client machines on the private network.

![image](https://github.com/user-attachments/assets/7f89d584-51e4-4e06-b6e4-0cfb64e3c3be)
![image](https://github.com/user-attachments/assets/7925a6d4-9572-454a-9698-f5819ddc65c2)
![image](https://github.com/user-attachments/assets/9c084a10-69da-4fbf-af10-c80418da4da8)


# 5. Automate User Creation
- Develop a PowerShell script to automatically add 1,000 user accounts to Active Directory. This script will streamline the process of creating a large number of users for the network.
# 6. Create Client Virtual Machine 
- Create the second virtual machine using the Windows 10 ISO.
- Connect this VM to the private network set up in VirtualBox and configure it as Client 1.
- Have the Windows 10 machine log in using one of the domain accounts created earlier in Active Directory, demonstrating that it is successfully integrated into the domain.
