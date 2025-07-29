# Screts

### Get secret value
```bash
kubectl get secret my-secret -o jsonpath='{.data.password}'
```
### Imperatively way to create secret
```bash
kubectl create secret generic my-other-secret --from-literal=user=rahul
```

### To get and decode secret
```bash
kubectl get secret my-other-secret -o jsonpath='{.data.user}' | base64 --decode
```