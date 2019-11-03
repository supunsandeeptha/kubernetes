kubectl run busybox --image busybox --replicas=1   --dry-run -o yaml > busybox-replicas.yaml
<!-- Made some changes to the yaml file, removed the restarted arguement -->
kubectl apply -f busybox-replicas.yaml
kubectl exec busybox-584c9d4dfd-lk4km -c busybox2 ls