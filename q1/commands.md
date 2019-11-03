kubectl create namespace mynamespace
kubectl run nginx --image nginx restart=Never --port 80 --dry-run -o yaml > nginx-pod.yaml
<!-- Made some changes to the yaml file, removed the restarted arguement -->
kubectl apply -f nginx-pod.yaml