# Training material for Docker, Kubernetes and Helm charts

## Ingress controller setup in Rancher (using Rancher desktop with containerd)
Deploy the NGINX ingress controller: 
```
helm upgrade --install ingress-nginx ingress-nginx \
  --repo https://kubernetes.github.io/ingress-nginx \
  --namespace ingress-nginx --create-namespace
```
check its up and running: 
```
kubectl get pods --namespace=ingress-nginx
```

kubectl exec <pod> -- env

kubectl create deployment pmt --image=nginx:1.14.2
kubectl apply -f deployment.yaml
kubectl rollout status deployment/demo-foe-team
