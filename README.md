# k8s-first-aid
Helper Utils for Kubernetes

### rootpod
Accessing the root file system of a host machine 
```
kubectl create -f manifests/rootpod.yaml
kubectl exec -it rootpod /bin/sh
``` 
The root file system can be found under `/hostroot/`. 

Once in the busybox you can also do a `chroot`
```
chroot /hostroot
```