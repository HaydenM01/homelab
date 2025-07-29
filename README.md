# 🧪 My HomeLab

Welcome to my homelab documentation repo! This project serves as a record of my self-hosted environment, configurations, and projects.

## 🌐 Overview

- **Purpose:** Learn networking, system administration, security, and virtualization.
- **Main Tools:** OPNsense, Proxmox, Docker, Ansible, Pi-hole, etc.

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
- Web server config (nginx): [`configs/nginx/`](configs/nginx/)

## 🤖 Automation

See [`ansible/`](ansible/) directory for playbooks.

## 🛠️ Scripts

All scripts in [`scripts/`](scripts/)

## 🐞 Troubleshooting Log

Fixes and issues documented in [`logs/troubleshooting.md`](logs/troubleshooting.md)

## 🚧 Work in Progress

- Unbound for recursive DNS resolver.
- NGINX proxy manager for reverse proxy.
- Wireguard VPN
- Netdata for monitoring.

## 📜 License

MIT License. Feel free to fork and adapt!
