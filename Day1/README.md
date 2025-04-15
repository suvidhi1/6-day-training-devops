# 🚀 6-Day DevOps Training Session – Summary & Notes

---

## 📅 Day 1 – Jenkins Setup, Maven Integration & Tomcat Configuration

### ✅ Jenkins Management
- Accessed Jenkins → `Manage Jenkins` → `Plugin Manager` → Installed necessary plugins.

### 🔐 TLS Setup
- Learned how to secure Jenkins using **TLS (HTTPS)** for safe access.

### 🔌 Plugins Installed:
| Plugin | Version |
|--------|---------|
| Maven Integration | 3.25 |
| Pipeline Maven Integration | 1508.v347c4b_692202 |
| Pipeline Maven Plugin API | 1508.v347c4b_692202 |
| Maven Release Plugin | 0.16.4 |
| Maven Info | 0.3.2 |
| Maven Invoker | 2.5 |

### 🐱‍💻 Tomcat Configuration for Jenkins Deployment:
1. Navigate to:  
   `C:\Program Files\Apache Tomcat\conf\tomcat-users.xml`

2. Edit file in VS Code and add:
   ```xml
   <role rolename="manager-gui"/>
   <role rolename="manager-script"/>
   <role rolename="admin"/>
   <user username="admin" password="admin123" roles="manager-gui,manager-script,admin"/>
