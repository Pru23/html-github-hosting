
# 📝 AWS Task 2 – GitHub to EC2 Hosting

## Overview
This task involved hosting a static HTML website on an EC2 instance using GitHub as the content source. It demonstrates automation via user data scripts and integration with version-controlled repositories.

---

## What I Learned

### ✅ EC2
- Launched Amazon Linux 2 instance
- Configured inbound security rules to allow HTTP traffic (port 80)

### ✅ Apache Web Server
- Installed via user data
- Served content from `/var/www/html`

### ✅ GitHub Integration
- Used `git clone` to pull web files directly from a public GitHub repo
- Enabled repeatable deployment with minimal manual steps

---

## EC2 User Data Script

```bash
#!/bin/bash
yum update -y
yum install -y httpd git
systemctl start httpd
systemctl enable httpd
cd /var/www/html
git clone https://github.com/Pru23/html-github-hosting.git
cp -r html-github-hosting/* .
