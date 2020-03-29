## config tls

## get token
```
kubectl -n kubernetes-dashboard get secret | grep kubernetes-dashboard-token
kubectl describe -n kubernetes-dashboard secret/kubernetes-dashboard-token-9w28w
```