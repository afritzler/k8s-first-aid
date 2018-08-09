# k8s-first-aid
Helper Utils for Kubernetes

### rootpod
Accessing the root file system of a host machine 
```
kubectl create -f https://raw.githubusercontent.com/afritzler/k8s-first-aid/master/manifests/rootpod.yaml
kubectl exec -it rootpod /bin/sh
``` 
The root file system can be found under `/hostroot/`. 

Once in the busybox you can do a `chroot`
```
chroot /hostroot
```
Now you should have access to the underlying OS.
