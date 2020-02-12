# Config Maps

## Create a config map from an env file

* create env file to store config data

```
kubectl create configmap <CONFIG_MAP_NAME> --from-env-file=<FILE_NAME>
```