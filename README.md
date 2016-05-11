# ndslabs-ingress
Ingress test


Label the loadbalancer node:
```
./label-ingress.sh	  
```

Create the default backend 404 handler
```
kubectl create -f default-backend.yaml
```

Create the nginx loadbalancer:
```
kubectl create -f loadbalancer-rc.yaml
```

Create ingresses for default, terra and demo namespaces
```
kubectl create -f default-ingress.yaml  
kubectl create -f terra-ingress.yaml
kubectl create -f demo-ingress.yaml     
```
