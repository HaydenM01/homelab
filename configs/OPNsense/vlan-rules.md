# Firewall Rules

## VLAN 10: LAN
| Action | Source     | Destination | Port | Description         |
|--------|------------|-------------|------|---------------------|
| Allow  | LAN net    | RFC-1918    | Any  | Allow management of other VLANs |
| Allow  | LAN net    | Any         | Any  | Allow internet access |

## VLAN 20: Guest
| Action | Source     | Destination | Port | Description         |
|--------|------------|-------------|------|---------------------|
| Block  | Guest net  | RFC-1918    | Any  | Blocks access to other VLANs |
| Allow  | Guest net  | Any         | Any  | Allow internet access |

## VLAN 30: Server (WIP)
- currently disabled WIP


## VLAN 40: Proxmox
| Action | Source     | Destination | Port | Description         |
|--------|------------|-------------|------|---------------------|
| Block  | Proxmox net  | RFC-1918    | Any  | Blocks access to other VLANs |
| Allow  | Proxmox net  | Any         | Any  | Allow internet access |

## VLAN 50: DNS/Pi-hole
| Action | Source     | Destination | Port | Description         |
|--------|------------|-------------|------|---------------------|
| Allow  | DNS net    | Any         | Any  | Allow internet access |
