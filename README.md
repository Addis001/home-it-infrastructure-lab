# Home IT Infrastructure Lab

## About This Project

I made this project to learn more about IT infrastructure and working with Linux servers. I used VirtualBox on my Windows PC to create an Ubuntu Server and then set up a private network between my PC and the server.

I started by installing Ubuntu Server and getting the network working. I used NAT so the server could access the internet and a host-only adapter so I could connect to it directly from Windows.

After that, I installed SSH and was able to remotely log into the Ubuntu server through Windows PowerShell. I also set up UFW firewall rules to allow SSH and web traffic.
## Network Diagram

![Network diagram for my home IT infrastructure lab](network-diagram.png)

## User Management

I created a second user called `labuser` and a group called `itadmins`. I also made a shared folder at `/srv/it-share` and set permissions so users in the group could access it.

I tested the permissions by logging in as `labuser`, creating a file in the shared folder, and reading the file back.

## Web Server

I installed Nginx on the Ubuntu server and allowed HTTP traffic through the firewall. I tested the web server from my Windows PC by going to `192.168.56.101` in my browser.

After I got it working, I replaced the default Nginx page with my own page showing the different parts of my lab.

## What I Used

- Ubuntu Server 26.04.1 LTS
- VirtualBox
- SSH
- UFW Firewall
- Nginx
- Windows PowerShell
- Linux users, groups, and permissions
- NAT and host-only networking

## What I Learned

Before this project, I had more experience with programming than managing servers. This project helped me understand how networking, Linux permissions, firewalls, SSH, and web servers work together.

I also got experience troubleshooting mistakes and testing each part of the server before moving on to the next step.
## Screenshots

### SSH Connection
I connected to the Ubuntu server remotely from my Windows PC using PowerShell and SSH.

![SSH connection from Windows PowerShell](ssh-connection.png)

### User and Permissions Test
I logged in as `labuser` and tested access to the shared directory by creating and reading a test file.

![Linux user and permissions test](permissions-test.png)

### Web Server
I tested the Nginx server from my Windows PC and accessed the custom lab page through the server's private IP address.

![Nginx web server running on Ubuntu](nginx-web-server.png)
