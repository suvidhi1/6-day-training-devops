# 📘 DevOps Training – Day 3

### 📅 Date: 29/03/2025

---

## 📌 Topics Covered

- Infrastructure Automation using **Terraform**
- AWS CLI Setup and Credential Configuration
- Writing and Executing Terraform Scripts
- Understanding and Installing **Docker**
- Monolithic vs Microservices Architecture
- Key DevOps Commands and Setup

---

## 🌐 Terraform - Infrastructure as Code

Terraform is an open-source **Infrastructure as Code (IaC)** tool that allows you to define and provision cloud infrastructure using declarative configuration files.

### ✅ Why Terraform?

- Automates cloud resource provisioning
- Enables consistency across environments
- Reduces manual work and errors
- Supports multiple cloud providers (AWS, Azure, GCP)

---

## 🛠️ Terraform Installation on Windows

### Steps:

1. Visit: [https://www.terraform.io/downloads](https://www.terraform.io/downloads)
2. Download the **Windows 386 ZIP**
3. Extract the ZIP
4. Create folder: `C:\Program Files\Terraform`
5. Move extracted files into it
6. Add the folder to:
   - **System Environment Variables → Path**
7. Open CMD and run:

```bash
terraform --version
