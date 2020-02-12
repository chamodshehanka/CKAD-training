# Kubernetes Services

### Services Types

1. Cluster IP - Single virtual IP allocated (default)
2. NodePort - Hight port allocated on each node
3. Load Balancer - Controls a Load Balancer endpoint external to cluster
4. External Name - Add CNAME DNS record to CoreDNS only

### Creating a ClusterIP Service
```
kubectl create deployment httpenv --image=bretfisher/httpenv  
``` 

Expose the port
```
kubectl expose deployment/httpenv --port 8888
```

Nodeport

```
kubectl expose deployment/httpenv --port 8888 --name httpenv-np --type NodePort
```

Load Balancer
```
kubectl expose deployment/httpenv --port 8888 --name httpenv-lb --type LoadBalancer
```

Create Deployment
```
kubectl run nginx --image nginx --restart Always --port 80 --replicas 3 -o yaml > nginx-deployment.yaml 
```

Expose Nginx deployment
```
kubectl expose deployment nginx --type ClusterIP --port 80 --target-port 80 --dry-run -o yaml > nginx-svc.yaml
```
