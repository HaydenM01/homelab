# Setup

Launch Locally:
```bash
docker run -d --name nginx-container -e TZ=UTC -p 8080:80 ubuntu/nginx:1.27-24.04_stable
```

Should be running on `http://localhost:8080`.