# server-manual
TITAN-Server utilize the Knot application, developed by CARV-ICS-FORTH (https://github.com/CARV-ICS-FORTH/knot) 

Knot is a complete environment for doing actual work on Kubernetes. It includes a complete set of web-based tools to help you unleash your productivity, without ever needing to use the command line. At its core, the Knot dashboard supplies the landing page for users, allowing them to launch notebooks and other services, design workflows, and specify parameters related to execution through a user-friendly interface. The dashboard manages users, wires up relevant storage to the appropriate paths inside running containers, securely provisions multiple services under one externally-accessible HTTPS endpoint, while keeping them isolated in per-user namespaces at the Kubernetes level, and provides an identity service for OAuth 2.0/OIDC-compatible applications.

The Knot installation includes JupyterHub, Argo Workflows, Harbor, and Grafana/Prometheus, all accessible through the dashboard. Behind the scenes, other popular tools are automatically installed to help with the integration, such as cert-manager, the NGINX Ingress Controller, Vouch Proxy, and the NFS CSI Driver. Knot also uses Helm charts internally for implementing service templates.

Check out the documentation (also available in the Knot dashboard under "Documentation" at the user menu), which includes installation instructions, a user guide, and technical notes on how Knot works internally. The Knot dashboard is written in Python using Django.

---
### Sign up and login
 When you visit the dashboard service with your browser https://titan-era-project.eu/ , you are greeted with the login screen.
 
 ![log in](images/login.JPG?raw=true "CRETA")

To create an account, select the "Sign up" option on the main screen and fill in a username, password, and contact email.
 ![log in](images/login.JPG?raw=true "CRETA")

 Once the account is activated by an administrator, login using your username and password. You can change your password when logged in by clicking on the user icon at the top-right of the screen and selecting "Change password" from the menu. The menu also provides options to switch between profiles (if you are a member of one or more teams), view previous messages reported, access this documentation, and logout. If you ever forget your password, please ask an administrator to reset it.
 
 ---
 
### Jupyter Notebook
Selecting "Notebooks" from the menu on the left will redirect you to JupyterHub. JupyterHub will automatically launch a new server instance for you, if one is not already running. Your notebooks are saved in /private/notebooks, so you can also access them as files from the dashboard. You can stop your server instance by clicking on the "Control Panel" button on the top-right of the screen.

---

### Upload Data
There are ```Persistent Volumes``` that users can use to store datasets ```/private``` and ```/shared```. 
In order to upload files and folders follow the steps below:

1. Choose ```Services``` from the left menu and the ```New Servcie```
 ![log in](images/services.JPG?raw=true "CRETA")

2. Select ```filebrowser``` from the dropdown menu
![log in](images/filebroaser.JPG?raw=true "CRETA")


3. Connect file browser with ```private``` folder.
![log in](images/filebr2.JPG?raw=true "CRETA")

4.After a while the service will be created. 
![log in](/images/fbcreated.JPG?raw=true "CRETA")

5. Use the service to upload your data 
![log in](images/fbfull.JPG?raw=true "CRETA")

---

