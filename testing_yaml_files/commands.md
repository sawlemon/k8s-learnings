# Kubecrl commands to create app

```
kubectl create deployment hello-node --image=registry.k8s.io/e2e-test-images/agnhost:2.39 -- /agnhost netexec --http-port=8080
```

```
kubectl expose deployment hello-node --type=NodePort --port=80 --target-port=8080
```

```
kubectl create ingress my-ingress --class alb-internal --rule='<domain>/*=hello-node:80'
```