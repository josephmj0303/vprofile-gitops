# VProfile GitOps Repository

![ArgoCD](https://img.shields.io/badge/ArgoCD-GitOps-EF7B4D?logo=argo)
![Helm](https://img.shields.io/badge/Helm-Charts-0F1689?logo=helm)
![Kubernetes](https://img.shields.io/badge/Kubernetes-Manifests-326CE5?logo=kubernetes)
![GitOps](https://img.shields.io/badge/GitOps-Continuous_Deployment-success)
![AWS EKS](https://img.shields.io/badge/AWS-EKS-orange?logo=amazonaws)

GitOps repository containing Helm charts and Kubernetes deployment manifests continuously synchronized to AWS EKS using ArgoCD.

---
## 📂 Related Repositories

| Repository      | Purpose                            |
| --------------- | ---------------------------------- |
| [vprofile-app](https://github.com/josephmj0303/vprofile-app)   | Application Source Code & CI/CD    |
| [vprofile-gitops-infra](https://github.com/josephmj0303/vprofile-gitops-infra)  | Terraform infrastructure and EKS provisioning |

Main Project:

[vprofile-app](https://github.com/josephmj0303/vprofile-app)

---

## 🚀 Architecture

![Architecture](docs/images/architecture-diagram.png)

---

## 📌 Project Overview

This repository serves as the GitOps source of truth for Kubernetes deployments.

ArgoCD continuously monitors this repository and automatically synchronizes changes to the AWS EKS cluster.

### Key Features

* Helm-based Kubernetes deployments
* ArgoCD Auto Sync
* ArgoCD Self-Healing
* GitOps workflow implementation
* Automated application rollouts

---

## 📂 Repository Structure

```text
.
├── helm/
│   └── vprofile/
│       ├── Chart.yaml
│       ├── values.yaml
│       └── templates/
├── argocd
│   ├── apps
│   │   └── vprofile-app.yaml
│   └── projects
│       └── vprofile-project.yaml
├── docs/
│   └── images/
│       ├── architecture-diagram.png
│       ├── argocd-application.png
│       └── argocd-resource-tree.png
└── README.md
```

---

## GitOps Workflow

1. CI/CD pipeline updates image tag in values.yaml
2. Changes are committed to this repository
3. ArgoCD detects repository changes
4. ArgoCD synchronizes workloads
5. Application is automatically updated in EKS

---

## 📸 Screenshots

### ArgoCD Application

![ArgoCD Application](docs/images/argocd-application.png)

### ArgoCD Resource Tree

![ArgoCD Resource Tree](docs/images/argocd-resource-tree.png)

---

## ⚙️ Technologies Used

* ArgoCD
* Helm
* Kubernetes
* AWS EKS
* GitHub

---

## 📊 Results

* GitOps-based application delivery
* Automatic Kubernetes synchronization
* Self-healing deployments
* Version-controlled infrastructure changes

---

## 📈 Future Enhancements

* ArgoCD Notifications
* Progressive Delivery with Argo Rollouts
* Multi-Environment Deployments
* Helm Dependency Management

---

## 👨‍💻 Author

Joseph MJ

DevOps Engineer | AWS | Kubernetes | GitOps
