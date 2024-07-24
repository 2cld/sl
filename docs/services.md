# SL Network Services

- Subnet 192.168.0.0/24
- Gateway 192.168.0.1
- DNS 192.168.0.1
- tbd


| Service admin Link  | type    | description | location    | mac |
|---------------------|---------|-------------|-------------|-----|
| - | ns | netstack [ns docs](https://netstack.org/docs/) | - | - |
| [http://192.168.0.1/](http://192.168.0.1/) | ng | tp-link [AC1750 Archer C7 doc](https://static.tp-link.com/res/down/doc/Archer_C7_V1_UG.pdf) ng | sl gb | 18-A6-F7-31-9C-06 |
| ~~[http://192.168.0.2/](http://192.168.2.2/)~~ | sg | nas sg | vm on cg | na |
| ~~[https://192.168.0.3:8006/](https://192.168.0.3:8006/)~~ | cg | [root](https://192.168.0.3:8006/) proxmox cg | cg on i3 macmini hw | moved to cf |
| - | ns2 | - | ns backup | na |
| ~~[http://192.168.0.5/](http://192.168.0.5/)~~ | ng2 | backup network gw | sl gb | na |
| [http://192.168.0.6:8080/](http://192.168.0.6:8080/) | sg2 | [buadmin](http://192.168.0.6:8080/) qnap sg2 5.3TB Raid 0.5TB Used | sl-sb-sw3p2 | 00-08-9B-E2-83-93 |
| ~~[http://192.168.0.7:8006/](http://192.168.0.5/7:8006)~~ | cg2 | backup compute gw | sl gb | na |
| Plex Services | - | - | - | na |
| [https://192.168.0.9:32400/](https://192.168.0.9:32400/) | slDVR | [slDVR](https://24.216.208.251:32500) on slwin11 -zt-10.147.17.198 .25TB-C 1.8TB-D 1.8TB-E | win app | 00-15-17-5B-F2-80 |
| [https://192.168.0.9:8123/](https://192.168.0.9:8123/) | ha | [HomeAssistant vm slwin11](https://192.168.0.9:8123/) on slwin11 -zt-10.147.17.198 .25TB-C 1.8TB-D 1.8TB-E | win app | 00-15-17-5B-F2-80 |
|---------------------|---------|-------------|-------------|-----|
| ~~[Gus - Dashboard CasaOS](http://192.168.0.70/)~~ | app |  vm slcg-100 | na | 08-00-27-84-49-45 |
| ~~[Gus - Remote - Guacamole](http://192.168.0.70:8090/guacamole/#/)~~  | [ghadmin](http://192.168.0.70:8090/guacamole/#/) | casoOS app | na | 08-00-27-84-49-xx |
| [Gus - HomeAssistant](192.168.0.9:8123) | ha | - | - | na |
| sl proxmox vms |---------|-------------|-------------|-----|
| ~~[http://192.168.0.70](http://192.168.0.70/)~~  | CasaOS | vm slcg-100 | sl | 08-00-27-84-49-45 |
| ~~[http://192.168.0.71:8090](http://192.168.0.70:8090/guacamole/#/)~~  | Guacamole | casoos app | sl | 08-00-27-84-49-xx |
| ~~[https://192.168.0.6:32400/](https://192.168.0.6:32400/)~~ | ~~slPlex~~ | ~~[slPlex](https://24.216.208.251:32400) on sg2~~ removed | vm sl-101 | 00-08-9B-E2-83-93 |
| ~~[192.168.0.10:8123](http://192.168.0.10:8123/)~~  | ha | vm slwin11 | sl | 08-00-27-84-49-45 |
| user machines | - | - | - | na |
| 192.168.0.9  slwin11  | win11 | Dell 1U win11 zt-10.147.17.198 | sl | 00-15-17-5B-F2-80 |
| 192.168.0.28 gusGram	| win11 | gus new laptop | sl | AC-74-B1-02-FB-CF |	
| 192.168.0.23 gusHPLaptop	| win10 | gus old laptop | sl | 00-23-8B-86-38-61 |	

---
