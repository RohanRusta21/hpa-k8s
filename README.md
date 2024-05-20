# hpa-k8s

# Install metric server

```bash
kubectl apply -f https://github.com/kubernetes-sigs/metrics-server/releases/latest/download/components.yaml
kubectl logs -n kube-system deployment/metrics-server
kubectl get deployment metrics-server -n kube-system
kubectl edit deployment metrics-server -n kube-system
```

# Add - --kubelet-insecure-tls in args when editing the metric server ( IMP )

# Verify configs

```bash
kubectl top pods
sudo systemctl restart kubelet
```
