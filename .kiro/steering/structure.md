# Project Structure

## Repository Organization

### Root Level
- `README.md` - Main project overview with service links and network topology
- `CNAME` - GitHub Pages domain configuration
- `LICENSE` - Project licensing
- `favicon.ico` - Site favicon

### Documentation (`/docs/`)
Primary documentation organized by functional area:
- `README.md` - Documentation index and network overview
- `devices.md` - Physical network devices, switches, and hardware inventory
- `services.md` - Network services, IP assignments, and service endpoints
- `storage.md` - Storage systems, Plex libraries, and capacity planning

### Operations (`/ops/`)
Operational procedures and deployment documentation:
- `README.md` - Operations overview
- `backup/` - Backup procedures and scripts
- `install/` - Installation notes for various systems
  - `slwin11ops-notes.md` - Primary ops machine setup
  - `slwin11-notes.md` - Secondary system setup
- `rdp/` - Remote desktop connection documentation

## Documentation Conventions

### File Naming
- Use lowercase with hyphens for multi-word files
- Include system/service prefix where applicable (e.g., `slwin11ops-notes.md`)
- Use `.md` extension for all documentation

### Content Structure
- Start with edit links: `[edit](https://github.com/2cld/sl/edit/main/path/file.md)`
- Use tables for structured data (IP assignments, device inventories)
- Include both local IPs (192.168.x.x) and ZeroTier IPs (10.147.17.x)
- Cross-reference related documentation with relative links

### Network Documentation Patterns
- **Services**: Include admin links, IP addresses, MAC addresses, physical locations
- **Devices**: Document MAC addresses, IP assignments, switch port connections
- **Storage**: Map drive letters, network shares, capacity, and purposes

### Link Conventions
- Internal links use relative paths: `./docs/services.md`
- External services include both local and public URLs
- Admin interfaces clearly marked with `[admin]` prefix
- ZeroTier addresses documented alongside local IPs

## Maintenance Guidelines
- Keep IP address tables current with DHCP reservations
- Document service changes in both main README and specific docs
- Use strikethrough (`~~text~~`) for deprecated/removed services
- Maintain cross-references between related documentation sections