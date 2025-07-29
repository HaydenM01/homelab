# Proxmox VM Templates

## Template: Docker Containers

### Description:
Uses Ubuntu OS to run Docker containers.

### Specs:
- Base Image: Ubuntu V. 25.04
- Disk Size: 500 GB
- Cores: 2
- RAM: 8192 MB
- Network: vmbr0 (bridged)

### How to recreate:
* Run following command to uninstall conflicts.
```bash
for pkg in docker.io docker-doc docker-compose docker-compose-v2 podman-docker containerd runc; do sudo apt-get remove $pkg; done
```

## Template: Ubuntu OS

### Description:

### Specs:

### How to recreate:

## Template: Windows DC and Client 

### Description:

### Specs:

### How to recreate: