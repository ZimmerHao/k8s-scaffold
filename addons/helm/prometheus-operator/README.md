## install prometheus operator

```
helm install prometheus-operator -f values.yaml .
```

## config tls
```
kubectl create secret tls prometheus-general-tls --key ./prometheus.key --cert ./prometheus.pem -n default
kubectl create secret tls alertmanager-general-tls --key ./alertmanager.key --cert ./alertmanager.pem -n default
```

## upgrate
```
helm upgrade -f values.yaml prometheus-operator stable/prometheus-operator -n default
```