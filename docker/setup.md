# Prerequisites
- Assuming Ubuntu is currently installed.
- Must install GNOME terminal
```bash
sudo apt install gnome-terminal
```

# Setup

1. Setup package repository.
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

2. Download latest DEB package:
```
https://docs.docker.com/desktop/setup/install/linux/ubuntu/
```

3. Install using `apt`:
```bash
sudo apt-get update
sudo apt-get install ./docker-desktop-amd64.deb
```

# Important

If using Proxmox to virtualize, change processor type to `host`.

![Processor](/docker/images/processor.png)
