kubectl run busyboxcron --image busybox --restart OnFailure --schedule "*/1 * * * *" --dry-run -o yaml > cronjob-busybox.yaml
kubectl apply -f cronjob-busybox.yaml
kubectl logs busyboxcron-1572762480-snp9w