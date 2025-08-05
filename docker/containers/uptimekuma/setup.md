## Uptime-Kuma

### Description

An open source monitoring tool.

### Deployment

Docker Run
```bash
# Create a volume
docker volume create uptime-kuma

# Start the container
docker run -d --restart=always -p 3001:3001 -v uptime-kuma:/app/data --name uptime-kuma louislam/uptime-kuma:1
```

Should be running on `http://localhost:3001`
