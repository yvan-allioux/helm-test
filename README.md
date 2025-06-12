helm repo add bitnami https://charts.bitnami.com/bitnami
helm repo update
helm dependency build .
helm install full-coverage . --set components.frontend.deployment.resources.limits.cpu=2 --set components.backend.pvc.storage=5Gi --set 'networkPolicies.denyAll.enabled=true'
