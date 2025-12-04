# TP-CI_CD

Ce dépôt contient un mini pipeline **CI/CD** basé sur **Argo CD** pour déployer automatiquement des applications sur un cluster Kubernetes installé avec **kubeadm**.

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
├── ArgoCD/
│   ├── ArgoCD_applications.png
│   ├── ArgoCD_cluster.png
│   ├── ArgoCD_nginx.png
│   ├── ArgoCD_nginx_page.png
│   ├── ArgoCD_pods.png
│   ├── ArgoCD_pods_apps.png
│   ├── ArgoCD_repo.png
│   ├── ArgoCD_wordpress.png
│   └── ArgoCD_wordpress_page.png
└── README.md
