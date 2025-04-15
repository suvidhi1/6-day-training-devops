# 📘 DevOps Training – Day 5

### 📅 Date: 02/04/2025

---

## 📌 Topics Covered

- **Container Problems & Solutions**
- **Introduction to Kubernetes**
- **Kubernetes Cluster Management**
- **Kubernetes Components & Architecture**
- **Kubernetes Commands**

---

## 🚧 Problems with Containers

1. **Autoscaling Issues**: Containers do not support autoscaling by default.
2. **Scale-Up**: When traffic increases, additional servers need to be added to the infrastructure.
3. **Vertical Scaling**: Increasing system resources (CPU, memory) to accommodate the load.
4. **Horizontal Autoscaling**: Adding more servers to scale the application.
5. **Scale-Down**: When traffic slows down, we must remove extra servers to save resources.
6. **No Load Balancing**: Containers do not handle load balancing out of the box.
7. **Downtime Risk**: If a container goes down, it can cause application downtime.
8. **Lack of Self-Healing**: Containers lack an automatic recovery mechanism in case of failure.

---

## ⚙️ Kubernetes: Container Orchestration Solution

To overcome the limitations of containers, we move towards **container orchestration** tools like **Kubernetes**.

### **What is Kubernetes?**
Kubernetes is a **container management** platform that automates the deployment, scaling, and operation of application containers. It can automatically recreate containers if they fail and provides several features to manage containerized applications.

### **Kubernetes Features**:
1. **Orchestration**: Coordinates the deployment and management of containers.
2. **Autoscaling**: Automatically adjusts the number of containers based on load.
3. **Load Balancing**: Distributes traffic across multiple containers to ensure high availability.
4. **Self-Healing**: Automatically replaces failed containers with new ones.
5. **Platform Independent**: Can run on any cloud or on-premise infrastructure.
6. **Automation**: Kubernetes uses **manifests** (YAML files) to automate the deployment and management of applications.

---

## 💻 Setting Up Kubernetes Cluster on AWS

### **1. Create a Server**:
To begin, create a server for your Kubernetes setup.

```bash
vi cluster.sh
# Copy and paste the required cluster configuration in the cluster.sh file
:wq
sudo su
sh cluster.sh

Create Kubernetes Cluster Using AWS EKS:
eksctl create cluster --name suvidhi-cluster --version 1.31 --region ap-south-1 --nodegroup-name test-linux --node-type t2.micro --nodes 3 --nodes-min 3 --nodes-max 5 --managed

# Installing and Configuring Kubernetes

### 1. Install kubectl:
To interact with the Kubernetes cluster, install kubectl, the command-line tool for Kubernetes.

```bash
snap install kubectl --classic
