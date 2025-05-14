```markdown
# Kubernetes Workflow: From Apply to Cleanup

## 1. Apply Resources
Apply your Kubernetes manifests (YAML files) to create resources:
```sh
kubectl apply -f <manifest.yaml>
```

## 2. Check Resource Status
Verify the status of your resources:
```sh
kubectl get all
kubectl describe <resource> <name>
kubectl logs <pod-name>
```

## 3. Update Resources
If you make changes to your manifests, re-apply:
```sh
kubectl apply -f <manifest.yaml>
```

## 4. Scale Resources
Scale deployments as needed:
```sh
kubectl scale deployment <deployment-name> --replicas=<number>
```

## 5. Rollout Management
Check rollout status and history:
```sh
kubectl rollout status deployment/<deployment-name>
kubectl rollout history deployment/<deployment-name>
```
Rollback if needed:
```sh
kubectl rollout undo deployment/<deployment-name>
```

## 6. Port Forwarding (Optional)
Access services locally:
```sh
kubectl port-forward svc/<service-name> <local-port>:<service-port>
```

## 7. Delete Resources (Cleanup)
Remove resources when done:
```sh
kubectl delete -f <manifest.yaml>
```
Or delete all resources in a namespace:
```sh
kubectl delete all --all -n <namespace>
```