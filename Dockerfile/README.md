# Ubuntu Xenial RDP Docker Image
An ubuntu xenial rdp container

## Directions

- Command line: 

```
docker build . -t ubuntu-rdp
docker run -d -p 3389:3389 ubuntu-rdp

--OR--

docker build . -t ubuntu-rdp
docker run -d -p 3389:3389 -v ~:/home ubuntu-rdp
```

- Connect to container host IP from RDP client
