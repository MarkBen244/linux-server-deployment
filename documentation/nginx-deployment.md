\# Nginx Installation and Website Deployment



\## 1. Objective



The objective of this stage was to install and configure Nginx on the Ubuntu Server and deploy a custom HTML webpage.



\## 2. Nginx Installation



Nginx was installed using the Ubuntu package manager.



```bash

sudo apt install nginx -y

```



The service was enabled and started using:



```bash

sudo systemctl enable --now nginx

```



The service status was checked using:



```bash

sudo systemctl status nginx

```



The output confirmed that Nginx was active and running.



\## 3. Default Web Server Test



Before deploying the custom webpage, the default Nginx page was tested locally:



```bash

curl http://localhost

```



The default Nginx welcome page was returned successfully, confirming that the web server was responding to HTTP requests.



\## 4. Website Deployment



The default Nginx website directory is:



```text

/var/www/html/

```



A custom HTML webpage was created at:



```text

/var/www/html/index.html

```



The webpage displays:



\- A deployment welcome message.

\- The hosting technology (Nginx).

\- The Ubuntu Server hostname.

\- The deployment status.



The website source code is included in the repository under:



```text

website/index.html

```



\## 5. Local Testing



The deployed webpage was tested from the Ubuntu Server using:



```bash

curl http://localhost

```



The command returned the custom HTML content successfully.



\## 6. External Connectivity Testing



VirtualBox NAT port forwarding was configured to expose the web server to the Windows host.



The website was accessed through a Windows web browser at:



```text

http://127.0.0.1:8080

```



The custom webpage displayed successfully.



\## 7. Result



Nginx was successfully installed and configured to serve a custom HTML webpage. Both local testing from Ubuntu and external access from the Windows host were successful.

