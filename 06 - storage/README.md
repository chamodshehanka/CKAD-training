# Storage

Create busybox 
```
kubectl run busybox --image busybox --dry-run -o yaml > busybox.yaml

kubectl apply -f busybox.yaml
```

## Empty Dir

