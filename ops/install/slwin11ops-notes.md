[edit](https://github.com/2cld/sl/edit/main/ops/install/slwin11ops-notes.md)
# slwin11ops notes

based on 
- https://netstack.org/docs/lan/compute/workstation/nswin11-cg
- https://github.com/JamesTurland/JimsGarage/tree/main

## Services on slwin11ops 

### Remotes
- zerotier [zt ghadmin 10.147.17.94](https://my.zerotier.com/login)
- google [remotedesktop slwin11ops](https://remotedesktop.google.com/access)
- E:\guscamp\RemoteDesktop\sl-zt-94-slwin11ops-ghadmin.rdp
  
### local slwin11ops 192.168.0.3

| url | local ui | map | wan ip | zt | dmz | [cf](https://one.dash.cloudflare.com/) tunnel |
|--|--|--|--|--|--|--|
| spectrum lan gateway | [192.168.1.1](http://192.168.0.1)|xx| 24.216.208.255 | xx | xx | xx |
| local lan gateway | [192.168.0.1](http://192.168.0.1)|xx| 24.216.208.255 | 10.147.17.94 | xx | xx |
| [plex.tv](https://plex.tv) | local [plex 192.168.0.3:32400](http://192.168.0.3:32400)|xx| 24.216.208.255 | 10.147.17.94 | xx | xx |

### docker
- /home/ghadmin/docker/docker-compose
- \\wsl.localhost\Ubuntu-24.04\home\ghadmin\docker\docker-compose

| url | wsl docker IP | map | lan ip | zt | dmz | [cf](https://one.dash.cloudflare.com/) tunnel |
|--|--|--|--|--|--|--|
| [traefik.2cld.com](https://traefik.2cld.com) <br/> [tf.lan](http://tf.lan) or [traefik.lan](http://traefik.lan) |172.31.46.229|80:80<br/>443:443| 192.168.0.3 | 10.147.17.94 | xx | [sl-2cld](https://one.dash.cloudflare.com/) |
| [portainer.2cld.com](https://portainer.2cld.com) <br/> [pt.lan:9000](http://pt.lan:9000) or [portainer.lan:9443](https://portainer.lan:9443) |172.31.46.229|8000:8000<br/>9000:9000<br/>9443:9443| 192.168.0.3 | 10.147.17.94 | xx | [sl-2cld](https://one.dash.cloudflare.com/) |
| [gitea.2cld.com](https://gitea.2cld.com) |172.31.46.229|3000:3000| 192.168.0.3 | 10.147.17.94 | xx | [sl-2cld](https://one.dash.cloudflare.com/) |
| [slcp.2cld.com](https://slcp.2cld.com) |172.31.46.229|9090:9090| 192.168.0.3 | 10.147.17.94 | xx | [sl-2cld](https://one.dash.cloudflare.com/) |
| xx |172.31.46.229|xx| 192.168.0.3 | 10.147.17.94 | xx | cf |

### maintenance notes
- ssh to gitea not setup
- https://wiki.archlinux.org/title/Gitea#Enable_SSH_Support
- ubuntu user of 24.04 wsl (need to look at install of wsl ubuntu)
- sudo apt-get install cockpit -y
