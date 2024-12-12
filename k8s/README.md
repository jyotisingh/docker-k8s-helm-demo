minikube addons enable ingress

Rancher desktop with containerd
Deploy the NGINX ingress controller: helm upgrade --install ingress-nginx ingress-nginx \
  --repo https://kubernetes.github.io/ingress-nginx \
  --namespace ingress-nginx --create-namespace
check pods running: kubectl get pods --namespace=ingress-nginx

secrets: echo -n 'top-secret' | openssl base64
kubectl exec <pod> -- env

kubectl create deployment pmt --image=nginx:1.14.2
kubectl apply -f deployment.yaml
kubectl rollout status deployment/demo-foe-team