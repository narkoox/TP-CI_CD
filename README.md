# TP-CI_CD

Ce dépôt contient un mini pipeline **CI/CD** basé sur **Argo CD**, **GitHub Actions** et **Kustomize** pour déployer automatiquement des applications sur un cluster Kubernetes installé avec **kubeadm**.

L’objectif est simple :  
> **à chaque commit sur la branche `main` qui modifie les manifests Kubernetes, un scan de sécurité est lancé, et Argo CD se charge d’appliquer les changements sur le cluster.**

---

## 🌳 Structure du dépôt

```bash
TP-CI_CD/
├── Applications/
│   ├── Nginx/
│   │   ├── base/
│   │   │   ├── deploy-nginx.yaml
│   │   │   └── kustomization.yaml
│   │   └── overlays/
│   │       ├── dev/
│   │       │   ├── kustomization.yaml
│   │       │   ├── namespace-dev.yaml
│   │       │   ├── configmap-dev.yaml
│   │       │   ├── deployment-dev.yaml
│   │       │   └── service-dev.yaml
│   │       └── prod/
│   │           ├── kustomization.yaml
│   │           ├── namespace-prod.yaml
│   │           ├── configmap-prod.yaml
│   │           ├── deployment-prod.yaml
│   │           └── service-prod.yaml
│   └── Wordpress/
│       └── deploy-wordpress.yaml
├── ArgoCD/
│   └── (captures d’écran Argo CD : apps, pods, synchro, etc.)
└── .github/
    └── workflows/
        └── trivy-ci.yaml
