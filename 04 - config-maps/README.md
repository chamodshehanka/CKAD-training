# Config Maps

## Create a config map from an env file

* first create env file to store config data

```
kubectl create configmap <CONFIG_MAP_NAME> --from-env-file=<FILE_NAME>
```

## Create config map via yaml file
* generate yaml
```
kubectl create configmap <CMAP_NAME> --from-literal=company=platformer --from-literal=name=chamod --dry-run -o yaml > org-cm.yaml
```

* Apply generated yaml
```
kubectl apply -f org-cm.yaml
```

_Then configmap will be created_

* To view config maps
```
kubectl get cm
```
