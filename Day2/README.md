# 📘 Day 2 – DevOps Training Session

### 📅 Date: 28/03/2025

This session focused on understanding cloud fundamentals, AWS services, Linux server setup, and deploying a basic web server on AWS EC2.

---

## ☁️ Cloud & Infrastructure Concepts

### 🔑 Key Differences
- **Cloud**: Remote service offering computing power, storage, and tools over the internet.
- **Data Center**: A **collection of physical servers** housed in one place.

### 🔧 Cloud Service Models
| Service Model | Description |
|---------------|-------------|
| **IaaS** | Infrastructure as a Service – virtual servers, storage, networking |
| **PaaS** | Platform as a Service – runtime and environment for development |
| **SaaS** | Software as a Service – fully managed applications accessible via the web |

---

## 🌐 AWS Overview

### 🌟 AWS Offers:
- **Auto Scaling**
- **On-Demand Services**
- **High Availability**

### Key AWS Services:
| Service | Purpose |
|---------|--------|
| **EC2** | Elastic Compute Cloud – Virtual servers |
| **EKS** | Elastic Kubernetes Service – Container orchestration |
| **AMI** | Amazon Machine Image – Pre-configured OS + software templates |
| **Route 53** | Domain name registration and DNS |
| **VPC** | Virtual Private Cloud – isolated network environment |

---

## ⚙️ EC2 Setup: Launching a Web Server

### 🔽 Step-by-Step: Launch EC2
1. **Go to**: AWS Console → EC2 → Launch Instance
2. **Name**: `webserver`
3. **Select AMI**: Amazon Linux
4. **Instance Type**: `t2.micro`
5. **Key Pair**:
   - Create new: `webserver`
   - Type: `RSA`
   - Format: `.ppk`
6. **Network Settings**:
   - Security group name: `webserver-security`
   - Description: Web server access
   - Add HTTP rule: Anywhere (IPv4)
7. **Storage**: 30 GB
8. **Instances**: Launch 2

---

### 🔑 SSH Access using PuTTY
1. **Download**: [PuTTY](https://www.putty.org/)
2. Open **PuTTY**
3. Paste the copied SSH hostname from EC2 console
4. Navigate:
   - **Appearance** → Set font to 14
   - **Connection** → Seconds between keepalives: `60`
   - **SSH → Auth** → Browse `.ppk` file
5. Click **Open** to access the server

---

## 🐧 Linux Web Server Setup

### Supported OS Families:
- **Red Hat Family**: Amazon Linux, Oracle, RHEL, SUSE
  - Uses: `httpd` (Apache Daemon)
- **Debian Family**: Ubuntu, Debian
  - Uses: `apache2` or `nginx`

### 🔧 Commands Run Inside EC2 Terminal:

```bash
# Become root
sudo su

# Give user sudo access
visudo
# Inside editor: press Shift + : then type wq to save and exit

# Install Apache Web Server
yum install httpd -y
which httpd
service httpd status
service httpd start
service httpd status

# Install Git
yum install git -y

# Clone repository
git clone -b master https://github.com/your-repo-url

# Navigate and copy files to Apache web directory
ls
cd your-cloned-folder
cp -r . /var/www/html
