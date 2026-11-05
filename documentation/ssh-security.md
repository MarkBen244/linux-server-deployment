\# SSH Remote Access and Firewall Configuration



\## 1. Objective



The objective of this stage was to enable secure remote administration of the Ubuntu Server from the Windows host using SSH and configure a firewall to control incoming network traffic.



\## 2. SSH Server Installation



OpenSSH Server was installed and configured on Ubuntu.



The following commands were executed:



```bash

sudo apt install openssh-server -y

sudo systemctl enable --now ssh

sudo systemctl status ssh

```



The SSH service was verified to be active and running.



\## 3. VirtualBox Network Configuration



The virtual machine was configured to use NAT networking.



Since the guest VM uses NAT, port forwarding rules were created in VirtualBox to allow the Windows host to access services running inside Ubuntu.



| Service | Protocol | Host Port | Guest Port |

|---|---|---:|---:|

| SSH | TCP | 2222 | 22 |

| HTTP | TCP | 8080 | 80 |



The SSH connection was established from Windows PowerShell using:



```powershell

ssh -p 2222 mark@127.0.0.1

```



\## 4. SSH Key Authentication



An existing Ed25519 SSH key pair on the Windows host was reused.



The public key was added to the Ubuntu user's `\~/.ssh/authorized\_keys` file.



Key-based authentication was tested successfully by connecting from Windows without entering the Ubuntu account password.



The private key remained stored on the Windows host.



\## 5. Firewall Configuration



UFW (Uncomplicated Firewall) was used to manage incoming network traffic.



The following commands were executed:



```bash

sudo apt install ufw -y

sudo ufw allow OpenSSH

sudo ufw enable

sudo ufw allow 80/tcp

sudo ufw status verbose

```



The firewall was configured with the following policy:



\- Incoming traffic: Denied by default.

\- Outgoing traffic: Allowed by default.

\- SSH (TCP port 22): Allowed.

\- HTTP (TCP port 80): Allowed.



\## 6. Verification



The following checks were performed:



\- SSH service confirmed active and running.

\- Remote SSH connection from Windows successfully established.

\- SSH key authentication successfully tested.

\- UFW confirmed active.

\- SSH and HTTP traffic confirmed as allowed.



\## 7. Result



Remote administration of the Ubuntu Server was successfully configured using SSH key authentication. UFW was enabled to restrict incoming traffic while permitting the required SSH and HTTP connections.

