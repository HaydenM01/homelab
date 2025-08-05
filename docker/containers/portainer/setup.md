# Deployment

1. Create volume
```bash
docker volume create portainer_data
```

2. Download and Install
```bash
docker run -d -p 8000:8000 -p 9443:9443 --name portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce:lts
```

Should be running on `http://localhost:9443`

Can also use:
`docker ps` to check running ports and containers.