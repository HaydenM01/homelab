# Troubleshooting Log

### Homepage

- Had to change original Docker run to include new file mapping. (Fixed)

  Original:
  ```bash
  -v /path/to/config:/app/config \
  ```

  New:
  ```bash
  -v /home/docker/path/to/config:/app/config \
  ```