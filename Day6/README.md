# DevOps Training – Day 6

### 📅 Date: 03/04/2025

---

## 📌 Topics Covered

- **Namespaces in Kubernetes**
- **Kubernetes Controllers & Services**
- **Replica Set and Deployment**
- **Monitoring in Kubernetes**

---

## 🚧 Namespaces in Kubernetes

Namespaces help divide a Kubernetes cluster into isolated environments, allowing better management and resource organization.

### **Default Namespaces**:
1. **kube-node-lease**: Used to check the health of the node. Kubernetes master node uses this for health monitoring.
2. **kube-public**: A namespace that allows public access to resources.

By default, when a cluster is created, resources like the metrics server, CNI, and core services are created within the **default** namespace. However, it is not recommended to deploy applications in the **default namespace** for production servers.

### **Creating a Custom Namespace**:

To create a custom namespace in Kubernetes, use the following commands:

```bash
kubectl create ns suvidhi-ns
kubectl get ns
kubectl get pods

# DevOps Training – Day 6

### 📅 Date: 03/04/2025

---

## 📌 Topics Covered

- **Challenges When Pods Go Down**
- **Replica Set & Deployment**
- **Monitoring in Kubernetes**

---

## 🚧 Challenges When Pods Go Down

When a pod goes down, you may face the following issues:

1. **Application Downtime**: To overcome this, you can attach **controllers** to the pod to manage its lifecycle. This ensures the pod is always running and reduces the risk of downtime.
  
2. **Changing IP Address**: Each pod has its own IP address. If the pod goes down, its IP address changes. To handle this issue, you need to create **services** in Kubernetes. These services provide static URLs, ensuring that communication with the pod is not disrupted.

3. **Data Loss**: Pods typically lose data when they go down. To mitigate this, you need to implement **volumes** in Kubernetes. Volumes allow data to be stored persistently, ensuring that even if a pod goes down, the data is preserved.

---

## 🔄 Replica Set & Deployment

### **Replica Set**:
A **Replica Set** is a Kubernetes object that ensures a minimum number of replicas for a given application, maintaining the desired state by keeping the application running 24/7.

#### **Replica Set Problems**:
- In real-time applications, using a **Replica Set** is not recommended because it doesn't support **rollouts** and **rollbacks** for updates. This means you can't update your applications with minimal downtime or revert back to a previous version if needed.

### **Deployments**:
A **Deployment** in Kubernetes is used to manage applications. It controls the creation and scaling of **Replica Sets**, which in turn manage the **pods**. Deployments provide a way to perform controlled updates to applications, including rolling updates and rollbacks, ensuring smooth and safe updates.

---

## 📊 Monitoring in Kubernetes

Monitoring is essential to understand what's going on in an application, identify issues, and track performance.

### **Monitoring Tools**:
1. **Prometheus**: A **metrics server** that collects time-series data (TSDB) from various components of your application and Kubernetes cluster.
  
2. **Grafana**: A **dashboard tool** that visualizes the time-series data from Prometheus. With Grafana, you can create monitoring dashboards that display the data in various formats, including **pie charts** and **graphs**, to monitor the health and performance of your application.

Setting up monitoring dashboards helps track your application's performance, allowing you to identify and address issues quickly, ensuring the application runs smoothly.

---

