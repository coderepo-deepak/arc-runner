.github/
├── workflows/
│   └── deploy-runner-controller.yml     # GitHub Actions workflow

infra/
├── base/
│   ├── namespace.yaml                   # Namespace manifest
│   ├── runner-controller-values.yaml    # Helm values for ARC (common config)
│   └── runner-deployment.yaml           # Generic RunnerDeployment manifest
├── overlays/
│   ├── dev/
│   │   └── kustomization.yaml           # Dev-specific overlays
│   ├── staging/
│   │   └── kustomization.yaml
│   └── prod/
│       └── kustomization.yaml
scripts/
├── bootstrap.sh                         # Bootstrap Minikube cluster, metrics-server
├── get-kubeconfig.sh                    # Export base64 KUBECONFIG
├── validate-k8s.sh                      # Validate resources
helm/
└── actions-runner-controller/           # Helm charts or submodule (optional)

.env.example                              # Example for local testing
README.md
