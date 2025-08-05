## Homepage

### Description

Homepage for services.

### Deployment

Docker Run
```bash
docker run --name homepage \
  -e HOMEPAGE_ALLOWED_HOSTS=* \
  -e PUID=1000 \
  -e PGID=1000 \
  -p 3000:3000 \
  -v /home/docker/path/to/config:/app/config \
  -v /var/run/docker.sock:/var/run/docker.sock:ro \
  --restart unless-stopped \
  ghcr.io/gethomepage/homepage:latest
```

# Important

- Change `HOMEPAGE_ALLOWED_HOSTS` to accessible IP/Domain.

- In Docker Desktop:

  Settings > Resources > File Sharing

  Remember to give access to local config files.

  ![Virtual File Sharing](/docker/containers/homepage/images/virtualfilesharing.png)

  