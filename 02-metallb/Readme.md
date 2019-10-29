Metallb deployment
------------------


1. Create metallb-system namespace

```bash
kubectl apply -f namespace.yaml
```

2. Create configmap with IP addresses pool:

```bash
kubectl apply -f configmap.yaml
```

3. Install metallb helm chart:

```bash
helm install --name metallb  --namespace metallb-system stable/metallb
```

Check metallb logs:

```bash
kubectl logs -l component=speaker -n metallb-system
```