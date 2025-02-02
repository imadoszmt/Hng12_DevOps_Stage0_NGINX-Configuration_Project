# DevOps Stage 0 - NGINX Setup on AWS

## Project Overview
This project is part of my DevOps Stage 0 task in the HNG12 internship. The objective was to set up and configure NGINX on an AWS EC2 instance and deploy a basic HTML page.

## Features
- AWS EC2 instance setup
- Secure SSH access configuration
- NGINX installation and configuration
- Custom HTML page deployment
- Firewall and security group adjustments

## How to Access
The deployed web page is accessible at:
[http://13.53.206.57/](http://13.53.206.57/)

## Blog Post
A detailed blog documenting the entire process, challenges, and solutions can be found here:
[Medium Blog Post](https://medium.com/@imaden.zalmat/setting-up-nginx-on-an-aws-instance-my-devops-stage-0-experience-414e41256623)

## Installation and Setup
### 1. Connect to EC2 Instance
```bash
ssh -i Imad-NGINX-2024-northeu.pem ubuntu@<Public-IP>
```

### 2. Install NGINX
```bash
sudo apt update && sudo apt install nginx -y
```

### 3. Start and Enable NGINX
```bash
sudo systemctl start nginx
sudo systemctl enable nginx
```

### 4. Deploy Custom Web Page
```bash
echo '<!DOCTYPE html>
<html>
<head>
    <title>DevOps Stage 0</title>
</head>
<body>
    <h1>Welcome to DevOps Stage 0 - Imad Zalmat/Imados</h1>
</body>
</html>' 
```

### 5. Adjust Firewall Settings
```bash
sudo ufw allow 'Nginx HTTP'
sudo ufw enable
```

## Challenges Faced
- SSH connection issues due to key permissions.
- NGINX not loading in the browser until firewall settings were updated.
- Permission errors while editing the web page.

## Lessons Learned
This task provided valuable hands-on experience in:
- Cloud infrastructure management using AWS.
- Server setup and NGINX deployment.
- Linux security and firewall configurations.

## Author
**Imad Zalmat (Imados)**

For hiring DevOps Engineers, visit: [HNG DevOps Engineers](https://hng.tech/hire/devops-engineers)

