## Nginx

### Description

A web server, reverse proxy, load balancer, and mail proxy service.

### Deployment

Docker Run
```bash
docker run -d --name nginx-container -e TZ=UTC -p 8080:80 ubuntu/nginx:1.27-24.04_stable
```

Should be running on `http://localhost:8080`.