[edit-github](https://github.com/2cld/sl/edit/main/README.md)

Update to attempt mkdocs Number 2

---

## External

| [cf-cat9me ct](https://one.dash.cloudflare.com/830c41d5976453f0c03f34d4f765b229/networks/tunnels) cf hv url | service [zt gh](https://my.zerotier.com/network/d5e5fb65371eb4a4) |
|---|---|
| [https://traefik.cat9.me](https://traefik.cat9.me) | traefik [cflare](https://dash.cloudflare.com/)->[ct-hv](10.147.17.219)->[nsdockerhb](10.147.17.176)->[traefik](172.18.0.2) |
| [https://portainer.cat9.me](https://portainer.cat9.me) | portainer [cflare](https://dash.cloudflare.com/)->[ct-hv](10.147.17.219)->[nsdockerhb](10.147.17.176)->[portainer](172.18.0.7) |
| [https://gitea.cat9.me](https://gitea.cat9.me) | gitea [cflare](https://dash.cloudflare.com/)->[ct-hv](10.147.17.219)->[nsdockerhb](10.147.17.176)->[gitea](172.18.0.6) |
| [https://nginx.cat9.me](https://nginx.cat9.me) | nginx [cflare](https://dash.cloudflare.com/)->[ct-hv](10.147.17.219)->[nsdockerhb](10.147.17.176)->[nginx](172.18.0.4) |
| [https://netbox.cat9.me](https://netbox.cat9.me) | netbox [cflare](https://dash.cloudflare.com/)->[ct-hv](10.147.17.219)->[nsdockerhb](10.147.17.176)->[netbox](172.18.0.8) |

| [wf-2cld ct](https://one.dash.cloudflare.com/830c41d5976453f0c03f34d4f765b229/networks/tunnels) wf sg2 url | service [zt gh](https://my.zerotier.com/network/d5e5fb65371eb4a4) |
|---|---|
| [https://metube.klopfenstein.org](https://metube.klopfenstein.org) | metube [cflare](https://dash.cloudflare.com/)->[cfDVR](10.147.17.209)->[metube](http://192.168.9.2:8081) |
| [https://gitea.klopfenstein.org](https://gitea.klopfenstein.org) | gitea [cflare](https://dash.cloudflare.com/)->[cfDVR](10.147.17.209)->[gitea](http://192.168.9.2:3000) |
| [https://sg.klopfenstein.org](https://sg.klopfenstein.org) | sg portal [cflare](https://dash.cloudflare.com/)->[cfDVR](10.147.17.209)->[cfDVR-portal](http://192.168.9.2:5000) |
| [https://jp.klopfenstein.org](https://jp.klopfenstein.org) | dav [cflare](https://dash.cloudflare.com/)->[cfDVR](10.147.17.209)->[cfDVR-dav](http://192.168.9.2:5005) |


| [sl-2cld ct](https://one.dash.cloudflare.com/830c41d5976453f0c03f34d4f765b229/networks/tunnels) sl hv url | service [zt gh](https://my.zerotier.com/network/d5e5fb65371eb4a4) |
|---|---|
| [https://traefik.2cld.com](https://traefik.2cld.com) | traefik [cflare](https://dash.cloudflare.com/)->[slwinll-hv](10.147.17.219)->[mg2](10.147.17.135)->[traefik](172.18.0.??) |
| [https://portainer.2cld.com](https://portainer.2cld.com) | portainer [cflare](https://dash.cloudflare.com/)->[slwinll-hv](10.147.17.219)->[mg2](10.147.17.135)->[portainer](172.18.0.??) |
| [https://gitea.2cld.com](https://gitea.2cld.com) | gitea [cflare](https://dash.cloudflare.com/)->[slwinll-hv](10.147.17.198)->[mg2](10.147.17.135)->[gitea](172.18.0.??) |

---
---

## Operations
- sl ops [sl.2cld.net/ops](./ops) based on [https://netstack.org/docs/ops/](https://netstack.org/docs/ops/)
  - [ops/backup](./ops/backup) - Backup procedures and scripts
  - [ops/rdp](./ops/rdp) - Remote desktop connections via ZeroTier
  - [ops/install](./ops/install) - Installation notes for systems
    - [slwin11ops](./ops/install/slwin11ops-notes.md) - Primary ops machine
    - [slwin11ops-hv-mg2](./ops/install/slwin11ops-hv-mg2-notes.md) - Ubuntu VM on Hyper-V

## Reference Documentation
- [netstack.org/docs](https://netstack.org/docs) - Base architecture patterns
- [ZeroTier Network](https://my.zerotier.com/network/d5e5fb65371eb4a4) - VPN management
- [Google Remote Desktop](https://remotedesktop.google.com/access) - Remote access
