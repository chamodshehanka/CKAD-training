# Jobs

### Pods
```
kubectl run busybox --image busybox --restart Never --dry-run -o yaml 
```

### Deployment
```
kubectl run busybox --image busybox --restart Never --dry-run -o yaml 
```

### Jobs
_Jobs are imutable_
```
kubectl run busybox --image busybox --restart OnFailure --dry-run -o yaml 
```
#### Edit job
```
kubectl edit job
```

### CronJob
```

```