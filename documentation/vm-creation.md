\# Virtual Machine Creation and Linux Installation



\## 1. Objective



The objective of this stage was to create a virtual machine using Oracle VirtualBox and install Ubuntu Server as the operating system.



\## 2. Virtualization Environment



\- \*\*Hypervisor:\*\* Oracle VirtualBox

\- \*\*Operating System:\*\* Ubuntu Server 26.04.1 LTS

\- \*\*Network Adapter:\*\* NAT

\- \*\*Virtual Disk:\*\* 25 GB

\- \*\*Virtual Machine Name:\*\* linuxserverweek2

\- \*\*Virtual Machine Username:\*\* mark



\## 3. VM Configuration



The virtual machine was configured with the following resources:



\- RAM: 2 GB

\- CPU: 2 processors

\- Storage: 25 GB dynamically allocated virtual disk

\- Network: NAT



\## 4. Ubuntu Server Installation



Ubuntu Server was installed using the downloaded Ubuntu Server ISO image.



The installation process included:



1\. Selecting Ubuntu Server as the installation option.

2\. Configuring automatic network addressing through DHCP.

3\. Configuring the virtual disk and root filesystem.

4\. Creating the user account and hostname.

5\. Enabling OpenSSH Server during installation.

6\. Completing the installation and rebooting the VM.



\## 5. Initial System Configuration



After installation, the following commands were executed:



```bash

sudo apt update

sudo apt upgrade -y

```



These commands refreshed the package index and installed available system updates.



\## 6. Verification



The following commands were used to verify the installation:



```bash

whoami

hostname

hostname -I

lsb\_release -a

```



The server was successfully installed and booted into Ubuntu Server.



\## 7. Result



The Ubuntu Server virtual machine was successfully created and configured in Oracle VirtualBox. It was ready for remote administration and subsequent service deployment.

