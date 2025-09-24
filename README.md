[edit](https://github.com/2cld/sl/edit/main/README.md)

- sl docs [sl.2cld.net/docs](./docs)
  - [sl.2cld.net/docs/devices](./docs/devices)
  - [sl.2cld.net/docs/services](./docs/services)
  - [sl.2cld.net/docs/storage](./docs/storage)

---

## External

| [cf-cat9me ct](https://one.dash.cloudflare.com/830c41d5976453f0c03f34d4f765b229/networks/tunnels) cf hv url | service [zt gh](https://my.zerotier.com/network/d5e5fb65371eb4a4) |
|---|---|
| [https://traefik.cat9.me](https://traefik.cat9.me) | traefik [cflare](https://dash.cloudflare.com/)->[ct-hv](10.147.17.219)->[nsdockerhb](10.147.17.176)->[traefik](172.18.0.2) |
| [https://portainer.cat9.me](https://portainer.cat9.me) | portainer [cflare](https://dash.cloudflare.com/)->[ct-hv](10.147.17.219)->[nsdockerhb](10.147.17.176)->[portainer](172.18.0.7) |
| [https://gitea.cat9.me](https://gitea.cat9.me) | gitea [cflare](https://dash.cloudflare.com/)->[ct-hv](10.147.17.219)->[nsdockerhb](10.147.17.176)->[gitea](172.18.0.6) |
| [https://nginx.cat9.me](https://nginx.cat9.me) | nginx [cflare](https://dash.cloudflare.com/)->[ct-hv](10.147.17.219)->[nsdockerhb](10.147.17.176)->[nginx](172.18.0.4) |
| [https://netbox.cat9.me](https://netbox.cat9.me) | netbox [cflare](https://dash.cloudflare.com/)->[ct-hv](10.147.17.219)->[nsdockerhb](10.147.17.176)->[netbox](172.18.0.8) |

| [cf-2cld ct](https://one.dash.cloudflare.com/830c41d5976453f0c03f34d4f765b229/networks/tunnels) wf sg2 url | service [zt gh](https://my.zerotier.com/network/d5e5fb65371eb4a4) |
|---|---|
| [https://metube.klopfenstein.org](https://metube.klopfenstein.org) | metube [cflare](https://dash.cloudflare.com/)->[cfDVR](10.147.17.209)->[metube](http://192.168.9.2:8081) |
| [https://gitea.klopfenstein.org](https://gitea.klopfenstein.org) | gitea [cflare](https://dash.cloudflare.com/)->[cfDVR](10.147.17.209)->[gitea](http://192.168.9.2:3000) |
| [https://sg.klopfenstein.org](https://sg.klopfenstein.org) | sg portal [cflare](https://dash.cloudflare.com/)->[cfDVR](10.147.17.209)->[cfDVR-portal](http://192.168.9.2:5000) |
| [https://jp.klopfenstein.org](https://jp.klopfenstein.org) | dav [cflare](https://dash.cloudflare.com/)->[cfDVR](10.147.17.209)->[cfDVR-dav](http://192.168.9.2:5005) |
|---|---|

| [sl-2cld ct](https://one.dash.cloudflare.com/830c41d5976453f0c03f34d4f765b229/networks/tunnels) sl hv url | service [zt gh](https://my.zerotier.com/network/d5e5fb65371eb4a4) |
|---|---|
| [https://traefik.2cld.com](https://traefik.2cld.com) | traefik [cflare](https://dash.cloudflare.com/)->[slwinll-hv](10.147.17.219)->[mg2](10.147.17.135)->[traefik](172.18.0.??) |
| [https://portainer.2cld.com](https://portainer.2cld.com) | portainer [cflare](https://dash.cloudflare.com/)->[slwinll-hv](10.147.17.219)->[mg2](10.147.17.135)->[portainer](172.18.0.??) |
| [https://gitea.2cld.com](https://gitea.2cld.com) | gitea [cflare](https://dash.cloudflare.com/)->[slwinll-hv](10.147.17.198)->[mg2](10.147.17.135)->[gitea](172.18.0.??) |
|---|---|
| ~~[https://chat.bradnordyke.com](https://chat.bradnordyke.com)~~ | ollama open-webui ->[cflare](https://dash.cloudflare.com/)->ct-hv-wsl-docker-owui |
| ~~[https://rt.bradnordyke.com](https://rt.bradnordyke.com)~~ | rust test ->[cflare](https://dash.cloudflare.com/)->ct-hv-wsl |
| ~~[https://ssh.bradnordyke.com](https://ssh.bradnordyke.com)~~ | ssh ->[cflare](https://dash.cloudflare.com/)->ct-hv-wsl ct gmail |
| ~~[https://metube.bradnordyke.com](https://metube.bradnordyke.com)~~ | metube ->[cflare](https://dash.cloudflare.com/)->sfDVR-docker ct gmail |
| ~~[https://sg2.bradnordyke.com](https://sg2.bradnordyke.com)~~ | sg2 ->[cflare](https://dash.cloudflare.com/)->ng->ng2-sg2 ct gmail |
| ~~[https://casa.bradnordyke.com](https://casa.bradnordyke.com)~~ | casaos |
| ~~[https://test.bradnordyke.com](https://test.bradnordyke.com)~~ | homepage |
| ~~[https://fred.klopfenstein.org](https://fred.klopfenstein.org)~~ | guac |
| ~~[https://home.klopfenstein.org](https://home.klopfenstein.org)~~ | homer |


---

- sl ops [sl.2cld.net/ops](./ops) based on [https://netstack.org/docs/ops/](https://netstack.org/docs/ops/)
  - sl [ops/backup](./ops/backup) based on [https://netstack.org/docs/ops/backup](https://netstack.org/docs/ops/backup)
    - slwin11ops backup script
  - sl [ops/rdp - zt remote](./ops/rdp) - network [cat-ghadmin-grid](https://my.zerotier.com/network/d5e5fb65371eb4a4)
    - [sl-zt-94-slwin11ops-ghadmin](./ops/rdp) Compute for sl - Windows 11 ops - i3 Dell 8GB
    - [sl-zt-198-slwin11-ghadmin](./ops/rdp) bu Compute for sl - Window 11 - old 1U Dell 32GB
  - sl [ops/rdp - google remotedesktop-ghadmin](https://remotedesktop.google.com/access)
    - gusGram
    - gusHPLaptop
  - sl [ops/install](./ops/install) node
    - [slwin11ops](./ops/install/) node is based on [netstack nswin11-cg](https://netstack.org/docs/lan/compute/workstation/nswin11-cg)
    - [slwinll]() node is based on [netstack nswin10](https://netstack.org/docs/lan/compute/workstation/nswin10)
    - gusGram preconfigured
    - gusHPLaptop preconfigured

---
---
Pre 2025.06.18 update
---
- [sl.2cld.net/docs](./docs/) - Main overview for sl
  - sl quick links
    - CasaOS Dashboard for network files >>>>>>> [Gus - Dashboard CasaOS](http://192.168.0.70/) - [casaos docs](https://netstack.org/docs/portals/casaos/)
    - Guacamole Remote [Gus - Remote - Guacamole](http://192.168.0.70:8090/guacamole/#/)
    - [QNAP NAS - sg - buadmin](http://192.168.0.6:8080/) <<<< sl QNAP Dashboard
  - sl details
    - [sl.2cld.net/docs/storage](./docs/storage)
    - [sl.2cld.net/docs/devices](./docs/devices)
  - sl [netstack 9.0/24 lan topology](https://netstack.org/docs/lan/)
    - [~~sl.2cld.net dhcp~~]() Host LAN
    - [ng.sl.2cld.net 9.1]() network gateway (ng) router
      - [ng.sl.2cld.net 9.1:80](http://192.168.9.1/) mikrotik admin web portal
      - mikrotik [netstack docs]() and [deployment config]()
    - [~~cg.sl.2cld.net 9.2~~]() compute gateway (cg) proxmox node1
    - [~~sg.sl.2cld.net 9.3~~]() storage gateway (sg)
    - [~~ng2.sl.2cld.net 9.5~~]() network gateway secondary (ng2)
    - [~~cg2.sl.2cld.net 9.6~~]() compute gateway secondary (cg2) proxmox node1
    - [~~sg2.sl.2cld.net 9.7~~]() storage gateway secondary (sg2)
    - [dg.sl.2cld.net 9.9]() document gateway (dg) proxmox node3 
      - [dg.sl.2cld.net 9.9:8006](https://192.168.9.9:8006/) Document gateway (dg) admin portal
      - proxmox [netstack docs](https://netstack.org/docs/lan/compute/proxmox/) and [deployment config]()
  - sl end
- [cf docs](https://cf.2cld.net/docs/) - Main overview for cf
  - just cf domain
- [tv docs](https://tv.2cld.net/) - Main overview for tv
  - tv notes
- [netstack docs](https://netstack.org/docs)
  - Plex notes [https://netstack.org/docs/portals/plex/](https://netstack.org/docs/portals/plex/)
  - Casa notes [https://netstack.org/docs/portals/casaos/](https://netstack.org/docs/portals/casaos/)
