# Secrets

Run busybox

```
kubectl run busybox --image busybox --dry-run -o yaml > busybox.yaml
```

Create secret

```
kubectl create secret generic app-passwords --from-literal=database=123 --dry-run -o yaml > app-password-secret.yaml
```

_Then do the configure in **busybox.yaml**_

```
resources: {}
        # To keep container running on K8s
        # or else below line also fine
        # command: ["/bin/sh", "-ec", "sleep 3600"]
        command: 
          - bin/sh
          - -c
          - "sleep 3600"
        envFrom:
          - secretRef:
            name: app-password
        volumeMounts:
          - name: any-app
            mountPath: /app
      volumes:
        - name: any-name
          secret:
            secretName: app-password
```

_After that apply secret and run the busybox too_