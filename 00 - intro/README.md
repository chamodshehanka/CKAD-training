CKAD training

Get container Logs

```
kubectl get pods
```

Scaling replicaset.

_same commands_
```
kubectl scale deploy/my-apache —replicas 2

kubectl s
```

View ENV of pod
```
kubectl exec <POD_NAME> env
```

Describe a pod
```
kubectl describe pod/<POD_NAME>
```

Delete pods permenently
```
# View all namespaces
kubectl get deployments --all-namespaces

# Then delete deployement one by one
kubectl delete -n <NAMESPACE> deployment <DEPLOYMENT>
```