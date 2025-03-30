# 🖥️ HTML Hosting via GitHub

This repository contains the files for a static HTML website used in AWS Task 2.

The website is deployed automatically on an Amazon EC2 instance by cloning this repository and placing the files in the Apache web server's root directory.

---

## 🚀 How to Deploy on EC2

1. Launch an Amazon EC2 instance (Amazon Linux 2).
2. Use the following User Data script during launch:

```bash
#!/bin/bash
yum update -y
yum install -y httpd git
systemctl start httpd
systemctl enable httpd
cd /var/www/html
git clone https://github.com/Pru23/html-github-hosting.git
cp -r html-github-hosting/* .



---

Once you've added the `README.md`, you're fully set to launch the EC2 instance with this repo. Want me to walk you through the EC2 launch again for Task 2 with this script?
