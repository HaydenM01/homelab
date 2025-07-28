# 🧪 My HomeLab

Welcome to my homelab documentation repo! This project serves as a record of my self-hosted environment, configurations, and projects.

## 🌐 Overview

- **Purpose:** Learn networking, system administration, security, and virtualization.
- **Main Tools:** pfSense, Proxmox, Docker, Ansible, Pi-hole, etc.

## 🖥️ Hardware Inventory

| Device        | Purpose         | OS / Firmware |
|---------------|------------------|----------------|
| OptiPlex 7010 | pfSense firewall | pfSense CE     |
| ThinkCentre   | Proxmox host     | Proxmox VE     |
| RPi 4         | Pi-hole / DNS    | Raspberry Pi OS|
| Netgear GS108 | VLAN switch      | Managed        |

More in [`hardware/inventory.md`](hardware/inventory.md)

## 🗺️ Network Diagram

![Network Diagram](diagrams/homelab-diagram.png)

## ⚙️ Configuration Snapshots

- Firewall rules (pfSense): [`configs/pfSense/`](configs/pfSense/)
- VM templates (Proxmox): [`configs/Proxmox/`](configs/Proxmox/)
- Web server config (nginx): [`configs/nginx/`](configs/nginx/)

## 🤖 Automation

See [`ansible/`](ansible/) directory for playbooks.

## 🛠️ Scripts

All scripts in [`scripts/`](scripts/)

## 🐞 Troubleshooting Log

Fixes and issues documented in [`logs/troubleshooting.md`](logs/troubleshooting.md)

## 🚧 Work in Progress

- VLANs and inter-VLAN routing
- Monitoring with Grafana
- VPN with WireGuard

## 📜 License

MIT License. Feel free to fork and adapt!
