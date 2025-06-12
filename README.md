helm install full-coverage . \
  --set components.frontend.deployment.resources.limits.cpu=2 \
  --set components.backend.pvc.storage=50Gi \
  --set 'networkPolicies.denyAll.enabled=true'
