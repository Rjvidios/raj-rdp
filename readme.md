## Simple Ubuntu RDP Container

This is a very simple proof of conecept to connect to a container via RDP client and have a desktop. Use the dockerfile to apply packages that you would like on top of Ubuntu Desktop and XRDP.

**Directions**
```
kubectl create ns ubrdp
kubectl create -f ubuntu-rdp.yaml
kubectl expose deployment ubuntu-rdp --name=ubuntu-rdp-lb --port=3389 --target-port=3389 --type=LoadBalancer --namespace=app1
kubectl get services --namespace ubrdp
```

Connect from RDP client to exposed IP with username 'root' and password 'VMware1!'
