\# Linux Server Deployment



A practical Linux server deployment project using Ubuntu Server, Oracle VirtualBox, SSH, UFW and Nginx.



\## About the Project



This project demonstrates the creation, configuration, security and deployment of a Linux server in a virtualized environment.



An Ubuntu Server virtual machine was created using Oracle VirtualBox. Remote administration was configured through SSH key authentication, incoming network traffic was controlled using UFW, and Nginx was deployed to host a custom HTML webpage.



The project also demonstrates connectivity between a Windows host machine and a Linux virtual machine using VirtualBox NAT port forwarding.



\## Project Objectives



\- Create and configure an Ubuntu Server virtual machine.

\- Configure Linux and update system packages.

\- Enable secure remote access using SSH.

\- Implement SSH key-based authentication.

\- Configure firewall rules using UFW.

\- Install and configure Nginx.

\- Deploy a custom HTML webpage.

\- Test local and external connectivity.



\## Technologies and Tools



| Technology | Purpose |

|---|---|

| Ubuntu Server 26.04.1 LTS | Linux operating system |

| Oracle VirtualBox | Virtualization |

| OpenSSH | Remote server administration |

| Ed25519 SSH keys | Key-based authentication |

| UFW | Firewall management |

| Nginx | Web server |

| HTML and CSS | Website development |

| Windows PowerShell | Remote access and administration |



\## Architecture



The project uses VirtualBox NAT networking with port forwarding to expose selected services to the Windows host.



```text

Windows Host

&#x20;    |

&#x20;    | SSH: localhost:2222

&#x20;    | HTTP: localhost:8080

&#x20;    |

VirtualBox NAT

&#x20;    |

Ubuntu Server

&#x20;    |

&#x20;    |-- OpenSSH (Port 22)

&#x20;    |

&#x20;    |-- UFW Firewall

&#x20;    |

&#x20;    |-- Nginx (Port 80)

&#x20;             |

&#x20;             |-- /var/www/html/index.html

```



\## Implementation



\### 1. Virtual Machine Creation



\- Created an Ubuntu Server virtual machine using Oracle VirtualBox.

\- Configured memory, processors, storage and NAT networking.

\- Installed Ubuntu Server and updated system packages.



\### 2. SSH Configuration



\- Installed and enabled OpenSSH Server.

\- Configured VirtualBox port forwarding for SSH.

\- Connected remotely from Windows PowerShell.

\- Configured Ed25519 public-key authentication.



\### 3. Firewall Configuration



Configured UFW with the following rules:



| Port | Service | Action |

|---|---|---|

| 22 | SSH | Allow |

| 80 | HTTP | Allow |



Incoming connections were denied by default unless explicitly allowed.



\### 4. Nginx Deployment



\- Installed Nginx using APT.

\- Enabled the service to start automatically.

\- Created a custom HTML webpage.

\- Deployed the webpage to `/var/www/html/index.html`.



\### 5. Connectivity Testing



The following tests were performed:



\- Verified the SSH service status.

\- Successfully connected to Ubuntu from Windows.

\- Tested SSH key authentication.

\- Verified UFW firewall rules.

\- Tested Nginx locally using `curl http://localhost`.

\- Accessed the deployed webpage from the Windows browser using `http://127.0.0.1:8080`.



\## Screenshots



\### Ubuntu Server



!\[Ubuntu Terminal Login](screenshots/ubuntu-terminal.png)



\### SSH Remote Connection



!\[SSH Connection](screenshots/ssh-connection.png)



\### Firewall Configuration



!\[Firewall Configuration](screenshots/firewall-configuration.png)



\### Nginx Service



!\[Nginx Configuration](screenshots/nginx-configuration.png)



\### VirtualBox Port Forwarding



!\[Port Forwarding Rules](screenshots/port-forwarding.png)



\### Deployed Website



!\[Deployed Website](screenshots/deployed-website.png)



\## Repository Structure



```text

linux-server-deployment/

│

├── documentation/

│   ├── vm-creation.md

│   ├── ssh-security.md

│   └── nginx-deployment.md

│

├── screenshots/

│   ├── ubuntu-terminal.png

│   ├── ssh-connection.png

│   ├── firewall-configuration.png

│   ├── nginx-configuration.png

│   ├── port-forwarding.png

│   └── deployed-website.png

│

├── scripts/

│

├── website/

│   └── index.html

│

└── README.md

```



\## Results



The project successfully achieved its main objectives:



\- Ubuntu Server was installed and configured.

\- Secure remote administration was established using SSH keys.

\- UFW was configured to control incoming traffic.

\- Nginx was deployed and configured to serve a custom webpage.

\- The website was successfully accessed from the Windows host.



\## Author



\*\*Mark Bernard\*\*



Computer Science Engineering Student  

Aspiring Cloud Engineer / DevOps Specialist



GitHub: \[MarkBen244](https://github.com/MarkBen244)

