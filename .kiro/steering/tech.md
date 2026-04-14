# Technology Stack

## Documentation Format
- **Primary Format**: Markdown (.md files)
- **Structure**: Hierarchical documentation with cross-references
- **Hosting**: GitHub Pages with CNAME domain mapping
- **Editing**: Direct GitHub web editor links provided in files

## Infrastructure Technologies

### Network Stack
- **Routers**: TP-Link Archer C7 (AC1750)
- **VPN**: ZeroTier One for site-to-site connectivity
- **DNS**: 8.8.8.8 (Google), local router DNS
- **DHCP**: Router-managed with MAC reservations

### Compute Platforms
- **Primary OS**: Windows 11 (workstations and servers)
- **Virtualization**: Hyper-V, Proxmox VE
- **Containers**: Docker with WSL2 backend
- **Remote Access**: RDP, SSH, Google Remote Desktop

### Storage Systems
- **NAS**: TrueNAS systems (cf site)
- **Media Storage**: Multi-TB arrays for Plex libraries
- **Backup**: Network-attached storage with RAID configurations

### Services & Applications
- **Media**: Plex Media Server (multiple instances)
- **Container Management**: Portainer, Traefik reverse proxy
- **Version Control**: Gitea self-hosted
- **Monitoring**: Home Assistant, Cockpit
- **Web Services**: Cloudflare tunnels for external access

## Common Operations

### Network Management
```bash
# Check ZeroTier status
zerotier-cli status
zerotier-cli listnetworks

# Network diagnostics
ipconfig /all
ping 10.147.17.x  # ZeroTier addresses
```

### Docker Operations (WSL2)
```bash
# Navigate to docker compose directory
cd /home/ghadmin/docker/docker-compose

# Container management
docker-compose up -d
docker-compose down
docker-compose logs -f [service]
```

### Remote Access
```bash
# SSH to Ubuntu VM on Hyper-V
ssh ghadmin@10.147.17.135

# SSH to WSL on ops machine
ssh -p 2222 ghadmin@10.147.17.94
```

## Reference Documentation
- Base architecture: [netstack.org](https://netstack.org/docs/)
- Network topology: [netstack.org/docs/lan/](https://netstack.org/docs/lan/)
- Equipment docs: TP-Link AC1750 Archer C7 manual