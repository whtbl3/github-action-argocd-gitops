# github-action-argocd-gitops

my-app-gitops/
├── base/                        ← Config CHUNG cho mọi môi trường
│   ├── deployment.yaml          ← định nghĩa app, image, port...
│   ├── service.yaml             ← định nghĩa service
│   └── kustomization.yaml       ← khai báo gồm những file nào
│
└── overlays/                    ← Config RIÊNG từng môi trường
    ├── staging/
    │   └── kustomization.yaml   ← override: namespace, replicas, image tag
    └── production/
        └── kustomization.yaml   ← override: namespace, replicas, image tag