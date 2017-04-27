# alpine-ssh-tunnel
Easy to use SSH Tunnel based in the Alpine Linux docker image

Based on https://github.com/iadknet/docker-ssh-client-light with some tweaks/customizations.

## Build
```
docker build --no-cache -t [image-name]:latest .
```

## Usage
```
docker run -d -p [LocalPort]:[LocalPort] -e "LOCAL_PORT=[LocalPort]" -e "REMOTE_HOST=[RemoteHost]" -e "REMOTE_PORT=[RemotePort]" -e "SSH_USER=[SshUser]" -e "SSH_HOST=[SshHost]" -e "ID_FILE=/app/conn.pem" -v [IdFile]:/app/conn.pem:ro --name=tunnel [image-name]
```