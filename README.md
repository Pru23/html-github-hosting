# 🖥️ HTML GitHub Hosting (Task 2)

![image](https://github.com/user-attachments/assets/87d555bd-63fc-4b06-8b14-e10fc9a2335c)


This project contains the files needed to host a static HTML website on an AWS EC2 instance. The EC2 instance pulls these files from this public GitHub repo using a launch script.

## 🔧 How It Works

- Files: `index.html`, `style.css`, `script.js`
- Repo is cloned on EC2 startup using `git`
- Apache serves the website on port 80

## 🚀 EC2 Launch Script (User Data)

```bash
#!/bin/bash
yum update -y
yum install -y httpd git
systemctl start httpd
systemctl enable httpd
cd /var/www/html
git clone https://github.com/Pru23/html-github-hosting.git
cp -r html-github-hosting/* .


