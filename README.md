# Live VM Migration and Health Monitoring using Azure, Prometheus & Grafana

This project demonstrates how to perform **Live Virtual Machine (VM) Migration** in a cloud environment while monitoring health statistics in real-time. The implementation uses **Microsoft Azure** for cloud infrastructure and **Prometheus + Grafana** for monitoring and visualization.

## 🔧 Tools & Technologies Used

- **Cloud Platform:** Microsoft Azure
- **Monitoring Tools:** Prometheus, Grafana, Node Exporter
- **Virtual Machines:** Ubuntu 22.04 LTS on Azure (VM1, VM2)
- **Scripting:** Azure CLI, PowerShell, Bash
- **Storage Services:** Azure Disks & Snapshots
- **Networking:** Azure Network Security Groups & Public IPs
- **IAM:** Azure Role-Based Access Control (RBAC)
- **Other:** SSH, UFW Firewall, PromQL (query language for Prometheus)

## ⚙️ Project Implementation Steps

### 1. Azure VM Setup
- Created a **Resource Group** in Azure.
- Launched **two virtual machines** (VM1 for monitoring stack, VM2 for migration).
- Configured **SSH access** and basic network rules.

### 2. Monitoring Setup (on VM1)
- Installed **Prometheus** and allowed port `9090`.
- Installed **Grafana** and allowed port `3000`.
- Configured Grafana to use Prometheus as a data source.
- Created dashboards with **CPU, memory, disk usage, and uptime metrics** using PromQL.

### 3. VM2 Setup & Migration
- Launched VM2 and configured it similarly.
- Deallocated VM2 and created a **snapshot** of its disk.
- Created a **new disk from snapshot** and attached it to VM1.
- Verified disk migration using Azure CLI.

### 4. Dashboard Configuration
- Used Grafana to create multiple panels for real-time monitoring.
- Included system metrics visualization for both VMs.
- Verified performance before and after migration.

### 5. Completion
- Ensured all services were properly shut down to avoid cost.
- Documented the process with screenshots and performed a demo.

![Project grafanana](https://github.com/user-attachments/assets/c1d27fea-4f42-4168-8ee8-0335148343ec)



