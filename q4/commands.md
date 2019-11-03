kubectl run nginx --image nginx:1.7.8 --replicas=2 --restart=Always --port 80 --dry-run -o yaml > nginx-deployment.yaml
kubectl apply -f nginx-deployment.yaml
kubectl expose deploy/nginx --port 80 --target-port 80 --type LoadBalancer -o yaml > nginx-deploymentservice.yaml