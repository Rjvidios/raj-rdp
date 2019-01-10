## Simple Ubuntu RDP Container

This is a very rough proof of conecept to connect to a container via RDP client and have a desktop

**Directions**
```
kubectl create ns app1
kubectl create -f ubuntu-rdp.yaml
kubectl expose deployment ubuntu-rdp --name=ubuntu-rdp-lb --port=3389 --target-port=3389 --type=LoadBalancer --namespace=app1
kubectl get services --all-namespaces
```

Connect from RDP client to exposed IP with username 'root' and password 'VMware1!'
