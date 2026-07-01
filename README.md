# ProLEAP EC2 Health Check

## Project Overview

This project demonstrates the deployment and monitoring of an AWS EC2 Ubuntu instance. It includes the installation and configuration of an Nginx web server, deployment of a custom HTML website, and development of a Bash-based health check script that verifies the overall health of the server.

The project was completed as part of the ProLEAP DevOps/Linux assignment.

---

## Objectives

- Launch an Ubuntu EC2 instance on AWS
- Connect securely using SSH
- Install and configure Nginx
- Deploy a custom website
- Create an automated EC2 health check script
- Generate a server health report
- Maintain the project using Git and GitHub

---

## Technologies Used

- AWS EC2
- Ubuntu 24.04 LTS
- Nginx
- Bash Shell Scripting
- Git
- GitHub
- Linux Commands

---

## Project Structure

```
proleap-ec2-health-check/
├── README.md
├── scripts/
│   └── ec2-health-check.sh
├── logs/
│   └── ec2-health-report.txt
├── website/
│   └── index.html
├── notes/
│   └── ec2-details.txt
├── screenshots/
└── .gitignore
```

---

## Installation Steps

### Update the system

```bash
sudo apt update
sudo apt upgrade -y
```

### Install Nginx

```bash
sudo apt install nginx -y
sudo systemctl enable --now nginx
```

### Verify Nginx

```bash
systemctl is-active nginx
```

---

## Deploy the Website

Copy the custom HTML file to the Nginx web directory.

```bash
sudo cp website/index.html /var/www/html/index.html
```

Access the website:

```
http://<PUBLIC-IP>
```

---

## Running the Health Check Script

Make the script executable.

```bash
chmod +x scripts/ec2-health-check.sh
```

Run the script.

```bash
bash scripts/ec2-health-check.sh
```

Generate a report.

```bash
bash scripts/ec2-health-check.sh > logs/ec2-health-report.txt
```

---

## Health Checks Performed

The script verifies:

- Hostname
- Current User
- Operating System
- System Uptime
- CPU Usage
- Memory Usage
- Disk Usage
- Top Running Processes
- Nginx Service Status
- Port 80 Availability
- Local Website Availability
- Public Website Accessibility
- Internet Connectivity
- DNS Resolution

---

## Sample Output

```
====================================
EC2 SERVER HEALTH CHECK
====================================

Hostname          : ip-172-31-30-183
Operating System  : Ubuntu 24.04 LTS
Nginx             : Running
CPU Usage         : OK
Memory            : OK
Disk              : OK
Internet          : PASS
DNS               : PASS
```

---

## Git Workflow

- Initialized Git repository
- Created multiple commits
- Managed project using Git
- Pushed project to Github

---

## Author

**Baijyanti Dash**

Linux System Administrator | AWS | Bash | Git | Nginx
