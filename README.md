# 🧪 My HomeLab

Welcome to my homelab documentation repo! This project serves as a record of my self-hosted environment, configurations, and projects.

## 🌐 Overview

- **Purpose:** Learn networking, system administration, security, and virtualization.
- **Main Tools:** OPNsense, Proxmox, Docker, Pi-hole, etc.

## 🖥️ Hardware Inventory

| Device            | Purpose           | OS / Firmware   |
|-------------------|-------------------|-----------------|
| ThinkCentre m910q x2 | Proxmox host      | Proxmox VE      |
| ThinkCentre M93P  | OPNsense firewall | OPNsense        |
| RPi 5             | Pi-hole / DNS     | Raspberry Pi OS |
| TP-Link TL-SG108PE  | VLAN switch       | Managed         |
| Netgear Nighthawk | Access Point | AC2600 |
| Netgear Nighthawk | Cable Modem | CM1000 |

More in [`hardware/inventory.md`](hardware/inventory.md)

## 🗺️ Network Diagram

![Network Diagram](diagrams/homelab-diagram.png)

## ⚙️ Configuration Snapshots

- Firewall rules (OPNsense): [`configs/OPNsense/`](configs/OPNsense/)
- VM templates (Proxmox): [`configs/Proxmox/`](configs/Proxmox/)
- Unbound Setup (Undbound): [`configs/unbound/`](configs/unbound/)
- Pihole Setup (pihole): [`configs/pihole/`](configs/pihole/)

## 🐋 Docker Containers

- Portainer (Web UI manager): [`docker/containers/portainer/`](docker/containers/portainer/)
- Adminer (DB UI): [`docker/containers/adminer/`](docker/containers/adminer/)
- Postgres (Database): [`docker/containers/postgres/`](docker/containers/postgres/)
- Nginx (Web Server): [`docker/containers/nginx/`](docker/containers/nginx/)
- Uptime Kuma (Monitoring): [`docker/containers/uptimekuma/`](docker/containers/uptimekuma/)
- Watchtower (Auto-updates): [`docker/containers/watchtower/`](docker/containers/watchtower/)
- Homepage (Homepage): [`docker/containers/homepage/`](docker/containers/homepage/)

## 🐞 Troubleshooting Log

Fixes and issues documented in [`logs/troubleshooting.md`](logs/troubleshooting.md)

## 🚧 Work in Progress

- Some centralized password management. Bitwarden?
- Wireguard VPN

## 📜 License

MIT License. Feel free to fork and adapt!
