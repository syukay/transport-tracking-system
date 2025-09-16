# 🚚 Fleetman Kubernetes Project

A microservices-based transport tracking system deployed on **Kubernetes**, designed to demonstrate real-world cloud-native patterns, monitoring, and automation.

---

## 📌 Overview

This project simulates a transport company that needs to track vehicles across the country.  
Each vehicle reports its GPS position to a central system, and a **Position Simulator** microservice generates this data.  

Through this project, you will learn how to deploy, manage, and monitor a production-grade Kubernetes cluster on **AWS**.

---

## 🚀 Features

- **Container Orchestration**  
  Deploy containers to a Kubernetes cluster using **EKS** or **Kops**.  

- **Cluster Monitoring**  
  - Use **Prometheus** and **Grafana** for live monitoring.  
  - Analyze system-wide logs with the **ELK Stack** (ElasticSearch + Kibana).  
  - Configure alerting and integrate with **Slack channels**.  

- **Kubernetes Fundamentals**  
  - Requests, Limits, and Horizontal Pod Autoscaling (HPA).  
  - Ingress Controller setup for managing external access.  
  - StatefulSets for stateful applications.  

- **Continuous Deployment (CD)**  
  Integrate Kubernetes with a CD pipeline.  

- **Helm for Package Management**  
  Manage charts and dynamically update your Kubernetes YAML with Helm.  

---

## 🛠 Tech Stack

- **Kubernetes** (EKS / Kops)  
- **Docker Desktop** (for local setup)  
- **Prometheus & Grafana** (monitoring)  
- **ELK Stack** (logging and visualization)  
- **Slack** (alerting)  
- **Helm** (package manager)  
- **Spring Boot + Java** (for microservices)  

---

## 📂 Repository Structure

Each microservice lives under its own folder.  
All services follow the naming convention:  

```
k8s-fleetman-<service-name>
```

Example:

```
k8s-fleetman-position-simulator/
k8s-fleetman-api-gateway/
k8s-fleetman-webapp/
...
```

---

## ⚡ Getting Started

### Prerequisites
- [Docker Desktop](https://www.docker.com/products/docker-desktop/)  
- Kubernetes CLI (`kubectl`)  
- AWS Account (for EKS or Kops setup)  

### Steps
1. Clone this repository:  
   ```bash
   git clone https://github.com/syukay/transport-tracking-system.git
   cd fleetman-kubernetes
   ```
2. Deploy the microservices to your local cluster:  
   ```bash
   kubectl apply -f k8s-manifests/
   ```
3. Access the system via the ingress endpoint (configured in your cluster).  
4. (Optional) Deploy to AWS EKS or Kops for a production-like environment.  

---

## 📊 Monitoring & Logging

- **Grafana**: dashboards for cluster metrics.  
- **Prometheus**: collects time-series data from pods/services.  
- **ELK Stack**: centralizes logs with ElasticSearch and Kibana.  
- **Slack**: alerts for system health and failures.  

---

## 💰 Costs (AWS Deployment)

- Running a live cluster on AWS will incur charges.  
- Expect costs around **$10 USD** if managed properly.  
- Always remember to **delete your cluster** when done:  
  ```bash
  eksctl delete cluster --name fleetman-cluster
  ```

---

## 📖 Learning Outcomes

By completing this project, you’ll gain hands-on experience in:
- Kubernetes operations in both local and cloud environments.  
- Real-world monitoring, alerting, and logging setups.  
- Managing microservices at scale with Helm and CD pipelines.  
- Understanding design trade-offs in distributed systems.  

---

## 📌 Notes
- This is not about coding microservices from scratch—the services are pre-built.  
- The main focus is on **deployment, scaling, and operations** in Kubernetes.  

---

## 📜 License
This project is licensed under the MIT License.  
See the [LICENSE](LICENSE) file for details.

---

## 🙌 Acknowledgments
- Microservice codebase provided by [Dick Chesterwood](https://github.com/DickChesterwood).  
