[edit](https://github.com/2cld/sl/edit/main/ops/install/slwin11ops-notes.md)
# slwin11ops notes

based on 
- https://netstack.org/docs/lan/compute/workstation/nswin11-cg
- https://github.com/JamesTurland/JimsGarage/tree/main

## Services on slwin11ops 

### Remotes
- zerotier [zt ghadmin 10.147.17.94](https://my.zerotier.com/login) - ZeroTier v1.14.2 ONLINE
- google [remotedesktop slwin11ops](https://remotedesktop.google.com/access)
- E:\guscamp\RemoteDesktop\sl-zt-94-slwin11ops-ghadmin.rdp
  
### local slwin11ops (DHCP - see note below)

> **⚠ CONFIRM:** LAN IP observed as both 192.168.0.143 and 192.168.0.141 on different dates.
> This machine uses DHCP (no static reservation). The IP will drift unless a MAC reservation
> is added on the router for MAC B0-83-FE-65-80-80.
> Recommend adding a DHCP reservation on 192.168.0.1 to lock this down.

| url | local ui | map | wan ip | zt | dmz | [cf](https://one.dash.cloudflare.com/) tunnel |
|--|--|--|--|--|--|--|
| spectrum lan gateway | [192.168.1.1](http://192.168.1.1)|xx| 24.216.208.255 | xx | xx | xx |
| local lan gateway | [192.168.0.1](http://192.168.0.1)|xx| 24.216.208.255 | 10.147.17.94 | xx | xx |
| [plex.tv](https://plex.tv) | local plex :32400 |xx| 24.216.208.255 | 10.147.17.94 | xx | xx |

### docker
- /home/ghadmin/docker/docker-compose
- \\wsl.localhost\Ubuntu-24.04\home\ghadmin\docker\docker-compose

| url | wsl docker IP | map | lan ip | zt | dmz | [cf](https://one.dash.cloudflare.com/) tunnel |
|--|--|--|--|--|--|--|
| [traefik.2cld.com](https://traefik.2cld.com) <br/> [tf.lan](http://tf.lan) or [traefik.lan](http://traefik.lan) |172.31.46.229|80:80<br/>443:443| DHCP | 10.147.17.94 | xx | [sl-2cld](https://one.dash.cloudflare.com/) |
| [portainer.2cld.com](https://portainer.2cld.com) <br/> [pt.lan:9000](http://pt.lan:9000) or [portainer.lan:9443](https://portainer.lan:9443) |172.31.46.229|8000:8000<br/>9000:9000<br/>9443:9443| DHCP | 10.147.17.94 | xx | [sl-2cld](https://one.dash.cloudflare.com/) |
| [gitea.2cld.com](https://gitea.2cld.com) |172.31.46.229|3000:3000| DHCP | 10.147.17.94 | xx | [sl-2cld](https://one.dash.cloudflare.com/) |
| [slcp.2cld.com](https://slcp.2cld.com) |172.31.46.229|9090:9090| DHCP | 10.147.17.94 | xx | [sl-2cld](https://one.dash.cloudflare.com/) |

### maintenance notes
- ssh to gitea not setup
- https://wiki.archlinux.org/title/Gitea#Enable_SSH_Support
- ubuntu user of 24.04 wsl (need to look at install of wsl ubuntu)
- sudo apt-get install cockpit -y

### ipconfig /all (latest - from ipconfig /all run)
```
Microsoft Windows [Version 10.0.26100.4351]
(c) Microsoft Corporation. All rights reserved.

C:\Users\ghadmin>ipconfig /all
Windows IP Configuration

  Host Name . . . . . . . . . . . . : slwin11ops
  Primary Dns Suffix . . . . . . . : 
  Node Type . . . . . . . . . . . . : Hybrid
  IP Routing Enabled. . . . . . . . : No
  WINS Proxy Enabled. . . . . . . . : No

Ethernet adapter vEthernet (ExternalHVwifi):
  Media State . . . . . . . . . . . : Media disconnected
  Description . . . . . . . . . . . : Hyper-V Virtual Ethernet Adapter #3
  Physical Address. . . . . . . . . : 10-08-B1-64-7F-31

Ethernet adapter vEthernet (InternalHV):
  Description . . . . . . . . . . . : Hyper-V Virtual Ethernet Adapter #4
  Physical Address. . . . . . . . . : 00-15-5D-09-BF-00
  Autoconfiguration IPv4 Address. . : 169.254.164.115
  Subnet Mask . . . . . . . . . . . : 255.255.0.0

Ethernet adapter vEthernet (ExternalHVether):
  Description . . . . . . . . . . . : Hyper-V Virtual Ethernet Adapter #2
  Physical Address. . . . . . . . . : B0-83-FE-65-80-80
  DHCP Enabled. . . . . . . . . . . : Yes
  IPv4 Address. . . . . . . . . . . : 192.168.0.141(Preferred)
  Subnet Mask . . . . . . . . . . . : 255.255.255.0
  Default Gateway . . . . . . . . . : 192.168.0.1
  DHCP Server . . . . . . . . . . . : 192.168.0.1
  DNS Servers . . . . . . . . . . . : 1.1.1.1
                                      1.0.0.1

Ethernet adapter ZeroTier One [d5e5fb65371eb4a4]:
  Description . . . . . . . . . . . : ZeroTier Virtual Port
  Physical Address. . . . . . . . . : A6-47-3E-46-F9-EE
  IPv4 Address. . . . . . . . . . . : 10.147.17.94(Preferred)
  Subnet Mask . . . . . . . . . . . : 255.255.255.0

Ethernet adapter vEthernet (Default Switch):
  Description . . . . . . . . . . . : Hyper-V Virtual Ethernet Adapter
  Physical Address. . . . . . . . . : 00-15-5D-BA-12-EE
  IPv4 Address. . . . . . . . . . . : 172.31.16.1
  Subnet Mask . . . . . . . . . . . : 255.255.240.0

C:\Users\ghadmin>
```

### zerotier-cli status
```
PS C:\WINDOWS\system32> zerotier-cli status
200 info f320719c15 1.14.2 ONLINE
PS C:\WINDOWS\system32>
```

### Differences to confirm

> **⚠ CONFIRM the following differences between older and newer ipconfig runs:**
>
> | Field | Older run | Newer run (/all) | Action |
> |---|---|---|---|
> | **LAN IP (ExternalHVether)** | 192.168.0.143 | 192.168.0.141 | Add DHCP reservation on router |
> | **DNS Servers** | not captured | 1.1.1.1, 1.0.0.1 (Cloudflare) | Confirm intentional |
> | **Default Switch IP** | 172.21.240.1 | 172.31.16.1 | Normal Hyper-V drift, no action |
> | **WSL adapter** | 172.31.32.1 present | Not present | Confirm WSL2 still running |
> | **ZeroTier IP** | 10.147.17.94 | 10.147.17.94 | ✅ Consistent |
