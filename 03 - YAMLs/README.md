# YAMLs

Create YAML
```
kubectl run busybox --image busybox --dry-run -o yaml > busybox-pod.yaml
```

run nginx as a deployment and expose port 80 3 replicas save the yamls port forward one of the pods using kubectl

```
kubectl run nginx-new --image=nginx --port=80 --replicas=3 --dry-run -o yaml > nginx-new.yaml
```