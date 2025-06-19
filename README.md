# 🚀 CI/CD Pipeline using Jenkins, Ansible, Docker & Kubernetes on AWS

This project implements a complete CI/CD pipeline on **Amazon Linux 2023 EC2 instances** using Jenkins, Ansible, Docker, Kubernetes (EKS), and GitHub. The pipeline automates building, testing, containerizing, and deploying a Java web application using modern DevOps practices.

---

## 🧩 Project Architecture

- **Jenkins Server** – CI/CD automation
- **Ansible Server** – Configuration management & deployment automation
- **Docker Host** – Image build & push to DockerHub
- **Kubernetes Cluster (EKS)** – Application deployment & scaling

---

## 🛠️ Tools & Technologies

| Category           | Tools & Services                               |
|-------------------|-------------------------------------------------|
| CI/CD             | Jenkins, GitHub                                 |
| Automation        | Ansible                                         |
| Containerization  | Docker, DockerHub                               |
| Orchestration     | Kubernetes (EKS via eksctl)                     |
| Build Tool        | Apache Maven                                    |
| Cloud             | AWS EC2, EKS                                    |
| Monitoring (optional) | Prometheus, Grafana                        |

---

## ⚙️ Pipeline Workflow

1. **Code Push** – Developer pushes code to GitHub.
2. **Jenkins Build** – Jenkins pulls code, builds using Maven.
3. **Artifact Transfer** – WAR and Dockerfile sent to Ansible via SSH.
4. **Image Build** – Ansible builds Docker image and pushes to DockerHub.
5. **Deployment** – Ansible applies Kubernetes manifests to EKS.
6. **Access App** – Application exposed through a LoadBalancer on port `8080`.

---

## 🔗 Sample Application

GitHub Repo (used in pipeline):  
➡️ [`Final_project.git`](https://github.com/Nandani1806pandey/Final_project)

DockerHub Repo:  
➡️ [`181071/registerpro`](https://hub.docker.com/repository/docker/181071/registerpro)

---

## 📁 Folder Structure (optional)

/jenkins-ansible-k8s-project
├── jenkins-setup.md
├── ansible/
│ ├── inventory
│ ├── ansible.cfg
│ └── register.yml
├── docker/
│ └── Dockerfile
├── k8s/
│ ├── regapp-deployment.yml
│ └── regapp-service.yml
└── README.md

---

## 🧪 How to Run

1. Provision 3 EC2 instances (Jenkins, Ansible, Docker) + EKS Cluster.
2. Follow setup steps in `jenkins-setup.md` or [project documentation](#).
3. Build the Jenkins job `devops_pro`.
4. Monitor Jenkins > Ansible > DockerHub > EKS.
5. Access the app via LoadBalancer URL.

---

## ✅ Status

- [x] Jenkins CI setup  
- [x] Maven build integration  
- [x] Artifact delivery using SSH  
- [x] Docker image pushed to DockerHub  
- [x] Kubernetes deployment via Ansible  
- [ ] Prometheus + Grafana (in progress)

---

## 📸 Screenshots (Optional)

_Add screenshots of your Jenkins job, DockerHub image, Kubernetes pods, and service output here._

![Screenshot 2025-06-19 200303](https://github.com/user-attachments/assets/ca7e069c-8186-4cf6-8835-b84c8396adc9)
![Screenshot 2025-06-19 194414](https://github.com/user-attachments/assets/79e86773-e767-4c5a-8010-0efd6a6211df)
![Screenshot 2025-06-19 194021](https://github.com/user-attachments/assets/bcc9e743-94ee-4b9c-9f88-fab2fe7deacf)
![Screenshot 2025-06-19 193515](https://github.com/user-attachments/assets/329c3510-0e16-44a0-9f4e-598c4115e2ad)


---

## 👤 Author

**Nandai Pandey**  
DevOps & Cloud Enthusiast | CI/CD | Docker | Kubernetes | AWS  
📧 [Email](nandani1806pandey@gmail.com)  
🔗 [LinkedIn](www.linkedin.com/in/nandani-pandey-485a58328)

---



