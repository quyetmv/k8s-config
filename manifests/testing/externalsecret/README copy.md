# Install External Secrets

## To Install

```
cd externalsecret;

helm repo add external-secrets https://charts.external-secrets.io

helm upgrade -i external-secrets external-secrets/external-secrets -f externalsecret/values.yaml

kubectl apply -f dockerhub-private.yaml -n testing
```
