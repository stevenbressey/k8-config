Helm deployment
---------------

Helm tiller deployment is already installed via kubespray.

1. Init helm

```bash
helm init
```

2. Create Service Account & Role in kube-system namespace:

```bash
kubectl apply -f rbac-config.yaml
```


3. Create Service Account & Role in default namespace:
   
```bash
kubectl apply -f rbac-config-ns-default.yaml
```
