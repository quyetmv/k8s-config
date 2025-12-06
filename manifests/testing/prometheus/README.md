## How to deploy or upgrade sonarqube

```bash
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
helm repo update
cd prometheus; helm upgrade -i prometheus -f values.yaml prometheus-community/kube-prometheus-stack -n addons --version 65.5.0
```

### Fix prometheus Kube-Proxy endpoint connection refused

```bash
kubectl edit cm kube-proxy-config -n kube-system
## Change from
    metricsBindAddress: 127.0.0.1:10249 ### <--- Too secure
## Change to
    metricsBindAddress: 0.0.0.0:10249
```