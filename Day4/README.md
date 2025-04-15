# 📘 DevOps Training – Day 4

### 📅 Date: 01/04/2025

---

## 📌 Topics Covered

- **Development, Testing, UAT, and Production Environments**
- **Docker Concepts**: Docker Files, Images, Containers, Docker Hub
- **Docker Commands and Instructions**
- **DevOps Practices for Containerization and Microservices**

---

## 🌍 Development Environment

A **development environment** is where developers test minimal functionalities of an application to ensure the basic building blocks work as expected before moving to more complex testing.

---

## 🔍 Testing Environment

The **testing environment** is where the **software testing team** performs functional and non-functional test cases. It's also used to perform load testing to evaluate how the application behaves under heavy usage.

---

## 👥 User Acceptance Testing (UAT) Environment

**UAT** is the stage before releasing a product to the market. The **prototype** of the application is shown to the client or end-users to ensure it meets their needs and expectations.

---

## 🚀 Production Environment

The **production environment** is the live, operational environment where the final version of the application is deployed and made accessible to customers.

---

## 🐳 Docker Concepts

### **Container**:
- A container is a **server** where an application is actually **run**. It is isolated and has all the necessary dependencies bundled together.

### **Dockerfile**:
- A **Dockerfile** is a text document that contains a set of instructions that Docker follows to build an image. It defines how an application should run inside a container.

### **Docker Image**:
- A **Docker image** is a **template** that contains everything needed to run an application:
  - Source code
  - Dependencies
  - Configuration files
  - Library files
  - Platform information
  - "Build Once, Run Anywhere"

### **Docker Hub**:
- **Docker Hub** is a **registry** where Docker images are stored. You can upload and share your images with others.

---

## 🧑‍💻 Docker Commands

### 1. **View Docker Containers**:
- `docker ps -a`: Lists all containers regardless of their state.
- `docker ps`: Lists only the running containers.

### 2. **Basic Container Commands**:
- `docker create -it --name webserver amazonlinux /bin/bash`: Creates a new container named "webserver" using Amazon Linux and opens a bash shell.
- `docker start webserver`: Starts the "webserver" container.
- `docker exec -it webserver /bin/bash`: Opens an interactive bash session inside the "webserver" container.
- `docker run -it --name sample ubuntu /bin/bash`: Runs a new container from the Ubuntu image and opens a bash shell.

### 3. **Daemon Containers (Detached Mode)**:
- Every microservice runs on a **different port**. Docker containers can run in the background (detached mode), where the container operates without blocking the terminal.

### 4. **Expose Ports**:
- Host port numbers are user-defined. This port defines how users can access the application through a browser.
  
---

## 📝 Dockerfile Instructions

1. **FROM**: Defines the base or parent image. Every Dockerfile must start with the `FROM` instruction.
   
