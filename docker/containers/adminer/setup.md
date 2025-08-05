## Adminer

### Description

A database management tool.

### Deployment

Docker Run
```bash
$ docker run --link some_database:db -p 8080:8080 adminer
```

Should be running on `http://localhost:8080`.