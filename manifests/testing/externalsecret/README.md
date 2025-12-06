# Install External Secrets

## To Install

```bash
cd externalsecret;

helm repo add external-secrets https://charts.external-secrets.io

helm upgrade -i external-secrets -n addons external-secrets/external-secrets -f values.yaml --version 0.10.4
```

## Create vault backend + dockerhub-private

```bash
kubectl create ns production
kubectl apply -f dockerhub-private.yaml -n production
kubectl apply -f secret-store.yaml -n production
kubectl apply -f fluentbit-v2.yaml -n production
kubectl apply -f fluentbit-sasl.yaml -n production
```
