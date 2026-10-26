Compute Engine Web Server (IaaS)
Vu Lan Anh Tran - Developed and uploaded the `index.html` website code and the cloud architecture diagram.
Esteban Munoz - Configured the cloud infrastructure, captured the evidence screenshots, and uploaded the project documentation.

Project Description
In this project, our team used a customized website on a cloud server, which we have full control of. We created an Nginx web server with a Google Compute Engine virtual machine with `e2-micro` Debian Linux operating system. Core Infrastructure as a Service (IaaS) concepts were used to apply a custom VPC firewall rule for traffic to only be allowed in on TCP port 80, for HTTP traffic.

IaaS Shared Responsibility Model
This project is an Infrastructure as a Service (IaaS) project, so there is a division of responsibility between our team and Google Cloud.

Our Team Manages:
The Linux operating system used by guests.Guest OS, Debian Linux.
To ensure your device runs safely, you'll need to install the OS updates and security patches.
Install and setup Nginx web server.Installing and configuring Nginx web server.
Website files (`index.html`)
The configuration and firewall rules set in VM.VM configuration & firewall rules.

Google Cloud Manages:
Physical data centers and facility security
Physical servers and hardware support.
* WiFi network cables and routers
* Virtualization infrastructure (Hypervisor)

Disaster Recovery: Snapshot Restore Process
We have scheduled a snapshot of our VM that takes a persistent snapshot of our VM as part of our backup procedure. In the event of a crash or loss of data, we would restore our server using these steps:
Go to Google Cloud Console and click on Compute Engine > Snapshots.
Choose our backup snapshot (e.g., `webserver-backup-v1`).
Click “Create Instance” to launch a new VM based on this snapshot as the boot disk.
Tag the new VM with the network tag used for the existing web-server configuration, which will now apply to this new VM, and the website will be up and running as before. 