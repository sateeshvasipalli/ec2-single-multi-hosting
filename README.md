# 🚀 EC2 Single & Multi Web Hosting Project

This project demonstrates how to set up **Single Web Hosting** and **Multiple Web Hosting** on an AWS EC2 instance using **Apache2 Web Server**.

---

## 📖 Overview
- **Single Hosting** → Hosting one static website at `http://<public-ip>`.  
- **Multi Hosting** → Hosting multiple websites on the same EC2 instance with different ports (`:80, :81, :83, :84`).  

This project helps you understand **Apache Virtual Hosts** and how to serve multiple sites on a single server.

---

## 🛠️ Tools & Technologies
- **AWS EC2** (Ubuntu instance)
- **Apache2** (Web Server)
- **Linux Commands**
- **AWS Security Groups** (Inbound rules)

---

## ⚙️ Steps Summary

### 🔹 Single Hosting
1. Launch EC2 (Ubuntu) and SSH into it.  
2. Install Apache2:  
   ```bash
   sudo apt update && sudo apt install apache2 -y
   sudo apt update && sudo apt install apache2 -y
Allow inbound HTTP (port 80) in Security Groups.

Copy website files into /var/www/html/.

Restart Apache and test in browser → http://<public-ip>.

🔹 Multi Hosting
Download multiple sample websites.

Create VirtualHost configs in /etc/apache2/sites-available/.

Assign each website a different port (80, 81, 83, 84).

Update /etc/apache2/ports.conf to listen on multiple ports.

Enable sites:

bash
Copy
Edit
sudo a2ensite site2.conf site3.conf site4.conf
Add inbound rules for ports 81, 83, 84 in Security Group.

Test in browser:

http://<public-ip>:80 → Site1

http://<public-ip>:81 → Site2

http://<public-ip>:83 → Site3

http://<public-ip>:84 → Site4
