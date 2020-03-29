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

## install pushgateway
```
helm install prometheus-pushgateway -n default -f values.yaml .
```

## upgrade pushgateway
```
helm upgrade -f values.yaml prometheus-pushgateway stable/prometheus-pushgateway -n default
```