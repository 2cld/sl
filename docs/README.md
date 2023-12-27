[edit](https://github.com/2cld/sl/edit/main/docs/README.md)

| External Service             | type | description | location    |
|------------------------------|------|-------------|-------------|
|      24.216.208.251 : 32400  | plex | [slPlex](https://24.216.208.251:32400) | sl |
|      24.149.22.11   : 32400  | plex | [cfPlex](https://24.149.22.11:32400) | cf |
|      24.149.22.11   : 32500  | plex | [cfDVR](https://24.149.22.11:32500)  | cf |
| test.christrees.com :  2020  | ssh  | sg | cf |
| test.christrees.com :  2021  | ssh  | sg2 | cf |

- [tv.2cld.net](https://tv.2cld.net/)
- [cf.2cld.net](https://cf.2cld.net/)
- [sl.2cld.net](https://sl.2cld.net/)
- [netstack.org/docs](https://netstack.org/docs/)

| Service admin Link  | type    | description | location    | mac |
|---------------------|---------|-------------|-------------|-----|
| [http://192.168.0.1/](http://192.168.0.1/) | ng | tp-link ng on subnet | sl gb | 18-A6-F7-31-9C-06 |
| ~~[http://192.168.0.2/](http://192.168.2.2/)~~ | sg | reserved nas sg on subnet | vm on cg | na |
| ~~[https://192.168.0.3:8006/](https://192.168.2.3:8006/)~~ | cg | reserved proxmox cg subnet | cg hardware | na |
| ns2 | - | - | backup | na |
| [http://192.168.0.6:8080/](http://192.168.0.6:8080/) | sg2 | qnap sg2 on subnet | sl-sb-sw3p2 | 00-08-9B-E2-83-93 |
| Plex | - | - | - | na |
| [https://192.168.0.6:32400/](https://192.168.0.6:32400/) | slPlex | qnap  [slPlex](https://24.216.208.251:32400) on sg2 | vm on sg2 | 00-08-9B-E2-83-93 |
|---------------------|---------|-------------|-------------|-----|
| catTemp | - | - | - | na |
| [https://192.168.0.23:32400/](https://192.168.0.23:32400/) | removed plex | gusHPlex | app on gusHPLaptop | 00-23-8B-86-38-61 |

---

## Media Ethernet Devices

| Network Name     | MAC Address-          | IP         | port  | description     | rm | link |
|------------------|-----------------------|------------|-------|-----------------|--|------|
|	na	                 | na                | na           | sw1p0 | Spectrum Modem  | sr | |
|	Archer_C7 switch 1 sr | 18-A6-F7-31-9C-07 | 192.168.0.1  |sw1int | TP-LINK AC1720  | sr | [admin](http://192.168.0.1/) |
| switch 1 to 2        | living room switch lr | na      |sw1p4-sw2p5 | sw1-sw2        |sr-lr| |
| switch 2 to 3        | basement switch bm    | na      |sw2p4-sw3p0 | sw2-sw3        |sr-bm| |
|------------------|-----------------------|------------|-------|-----------------|----|------|
|	~~StevesRokuUltra~~	| 8C-49-62-0B-69-8C | 192.168.0.24 | ~~sw2p4~~ | StevesRokuUltra | sr | |
|	StevesRokuUltra	     | 8C-49-62-0B-69-8D | 192.168.0.14 | wifi  | StevesRokuUltra | sr | |
|	TIVO-8480001902B1749 | 00-11-D9-5F-47-83 | 192.168.0.15 | wifi  | Steves640       | sr | |
|	TIVO-8480001902B1749 | 00-11-D9-5F-47-82 | 192.168.0.11 | sw1p1 | Steves640       | sr | |
| TIVO-748000190569948 | 00-11-D9-35-02-A8 | 192.168.0.12 | sw1p2 | Steves320       | sr | |
|	HDHR-10802956	       | 00-18-DD-08-02-95 | 192.168.0.13 | sw2p4 | plexTuner       | sr | [admin](http://192.168.0.13/) |
|------------------|-----------------------|--------------|-------|-----------------|----|------|
|	~~KathysRokuUltra~~	 | 84-EA-ED-A8-64-9x | na           | wifi  | KathysRokuUltra | lr | |
|	KathysRokuUltra	     | 84-EA-ED-A8-64-91 | 192.168.0.21 | sw2p1 | KathysRokuUltra | lr | |
|	TIVO-74600019083B6E2 | 00-11-D9-38-0B-FC | 192.168.0.22 | sw2p2 | Kathys160       | lr | |
| gusHPLaptop          | 00-23-8B-86-38-61 | 192.168.0.23 | sw2p3 | gusHPLaptop win10 | lr | [gusHPlex](http://192.168.0.23:32400) |
| gusGram              | AC-74-B1-02-FB-CF | 192.168.0.28 | wifi  | gusGram win11 i7 | lr | rmdesk |
|	Portal-8B57B421F784  | A4-0E-2B-4C-EF-C7 | 192.168.0.29 | wifi  | portaltv        | lr | |
| pictureframe         | na                | na           | wifi  | picture frame   | lr | |
|------------------|-----------------------|------------|-------|-----------------|----|------|
|	cfPlex               | 10-C3-7B-46-0C-ED | 192.168.0.201 | sw1p1 | cfPlex chris's  | bm | rmdesk [plex](http://192.168.0.201:32400) |
|	cfsg2   	           | 00-15-5D-02-71-03 | 192.168.0.202 | vmbrg | trueNAS_vm-cfPlex | bm | [admin](http://192.168.0.202:8006/) |
|------------------|-----------------------|------------|-------|-----------------|----|------|
|	cats-Mac-mini        | 7C-C3-A1-73-CC-A3 | 192.168.0.211 | wifi  | macmini  chris  | bm | |
|	catSurface   	       | 28-18-78-C7-FC-23 | 192.168.0.212 | wifi  | suface   chris  | bm | |
|	Pixel-6a    	       | 86-50-46-38-28-96 | 192.168.0.213 | wifi  | Pixel-6a chris  | bm | |
| FireTV cube          | A4-08-01-60-57-35 | 192.168.0.214 | wifi  | FireTV   chris  | bm | |

## Coax

| Coax name  | source   | destination | locations |
| ---------- |----------|-------------|-----------|
| ant feed   | main ant | coax amp    | attic to basement |
| spl01 feed | coax amp | spl01       | basement |
| sr feed    | spl01    | spl02       | basement to sr |
| Steves320 feed | spl02p1 | Steves320 Tivo ant | sr |
| plexTuner feed | spl02p2 | plexTuner ant | sr |
| Kathys160 feed | spl02p3 | Kathys160 ant | lr |

| Coax name  | source   | destination | locations |
| ---------- |----------|-------------|-----------|
| cable feed   | main cable | spl03 input | sr |
| spl03 feed | spl03p1 | spectrum modem       | sr |
| spl04 feed | spl03p2   | spl04 input       | sr |
| Steves640 feed | spl04p1 | Steves320 Tivo cable | sr |
| Kathys160 feed | spl04p2 | Kathys160 cable | sr |
| ?? feed | spl04p3 | ?? cable | sr |
| ?? feed | spl04p4 | ?? cable  | sr |
| Kathys160 feed | spl04p5 | ?? cable  | sr |

# Reference Docs
- sl network based on [https://netstack.org/](https://netstack.org/) sl.lan model [https://netstack.org/docs/lan/](https://netstack.org/docs/lan/)
  - ng.sl.lan network gateway [https://netstack.org/docs/lan/network/tp-link/](https://netstack.org/docs/lan/network/tp-link/)
  - sg.sl.lan storage gateway [https://netstack.org/docs/lan/storage/freenas/](https://netstack.org/docs/lan/storage/freenas/)
  - cg.sl.lan compute gateway [https://netstack.org/docs/lan/compute/proxmox/nswin11vm](https://netstack.org/docs/lan/compute/proxmox/nswin11vm)
 
---

- DHCP 192.168.0.100-199
- DNS 8.8.8.8
- GW 192.168.0.1 255.255.255.0
- SSID: TP-LINK_24 (18-A6-F7-31-9C-06)
- SSID: TP-LINK_9C05_5G (18-A6-F7-31-9C-05)

- WAN
```
18-A6-F7-31-9C-07
IP Address:	24.216.208.251	Dynamic IP
Subnet Mask:	255.255.248.0	 
Default Gateway:	24.216.208.1	  
DNS Server:	71.10.216.1 , 71.10.216.2
```

## port forward

| External | Internal | IP | detail |
|-------|-------|---------------|---|
| 32400	| 32400	| 192.168.0.23  | gusHPlex on gusHPLaptop | 
| 32800	| 32400	| 192.168.0.201 | cfPlex on win11 | 
|  2020 |    22 | 192.168.0.202 | cf-sg2 cattemp truenas | 


- [Link to CD Pictures](https://photos.app.goo.gl/gJL3BKZerkMmL1Jn7)

