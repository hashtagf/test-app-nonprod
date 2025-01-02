# Helm-app

### helm-syntax

```bash
# create chart
helm create <chart-name>

# create namespace
kubectl create namespace app

# install chart
helm install <reslese-name>  <chart-path> -f <value-path> --namespace=app

# upgrade chart
helm upgrade <reslese-name> <chart-path> -f <value-path> --namespace=app

# uninstall
helm uninstall <reslease-name> --namespace=app

# show list chart
helm list --namespace=app

# package to zip
helm pacakge <chart-path>

# dryrun
helm install <release-name> <chart-path> -f <value-path> --dry-run
```

### example dryrun create deployment

```bash
# syntax
kubectl create deploy <name> --image=<image-path> --dry-run=client -oyaml > <file-wirte-path>

kubectl create deploy api --image=api:test --dry-run=client -oyaml > templates/deployment-api.yaml

kubectl create deploy ui --image=ui:test --dry-run=client -oyaml > templates/deployment-ui.yaml
```
