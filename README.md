# TP-CI_CD

Ce dépôt contient un mini pipeline **CI/CD GitOps** basé sur **Argo CD** pour déployer automatiquement des applications sur un cluster Kubernetes installé avec **kubeadm**.

L’objectif est simple :  
> **chaque changement dans les manifests Kubernetes de ce dépôt est automatiquement appliqué sur le cluster par Argo CD.**

---

## 🌳 Structure du dépôt

```bash
TP-CI_CD/
├── Applications/
│   ├── Nginx/
│   │   └── deploy-nginx.yaml
│   └── Wordpress/
│       └── deploy-wordpress.yaml
└── README.md
