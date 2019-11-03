echo -e "var1=val1\n# this is a comment\n\nvar2=val2\n#anothercomment" > config.env
kubectl create cm busybox-from-the-file --from-file config.env --dry-run -o yaml > special-config.yaml