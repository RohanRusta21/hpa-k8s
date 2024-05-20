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

# For traffic gen 

```bash
apk add ark
then go inside the pod and execute this : wrk -t12 -c400 -d30s http://<service-name>:8080/index.html
```

# For VPA

```bash
git clone https://github.com/kubernetes/autoscaler.git
cd autoscaler/vertical-pod-autoscaler/hack
./vpa-up.sh
```
