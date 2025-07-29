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

1. Set up apt repository
```bash
# Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "${UBUNTU_CODENAME:-$VERSION_CODENAME}") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
```

2. Install Docker packages
```bash
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

3. Verify Installation
```bash
sudo docker run hello-world
```

## Template: Ubuntu OS

### Description:

### Specs:

### How to recreate:

## Template: Windows DC and Client 

### Description:

### Specs:

### How to recreate: