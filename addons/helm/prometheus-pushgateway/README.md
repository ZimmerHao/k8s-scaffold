## download pushgateway
```
helm fetch stable/prometheus-pushgateway
```

## config values.yaml
```
vim values.yaml
```

## config tls
```
kubectl create secret tls pushgateway-tls --key ./pushgateway.key --cert ./pushgateway.pem -n default
```

##