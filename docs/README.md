

| Service admin Link  | type    | description | location    | mac |
|---------------------|---------|-------------|-------------|-----|
| [http://192.168.0.1/](http://192.168.0.1/) | ng | tp-link ng on subnet | sl gb | 18-A6-F7-31-9C-06 |
| [http://192.168.0.2/](http://192.168.2.2/) | sg | truenas sg on subnet | vm on cg | na |
| [https://192.168.0.2:443/](https://192.168.2.2:443/) | sg | truenas (https) sg on subnet | vm on cg | na |
| [https://192.168.0.3:8006/](https://192.168.2.3:8006/) | cg | proxmox cg subnet | cg hardware | na |
| - | - | - | - | na |
| ~~[http://192.168.0.6:81/](http://192.168.0.6:81/)~~ | ~~sg2~~ | truenas2 sg2 on subnet | vm on cg2 | na |
| ~~[https://192.168.0.6:444/](https://192.168.0.6:444/)~~ | ~~sg2~~ | truenas2 (https) sg2 on subnet | vm on cg2 | na |
| ~~[https://192.168.0.7:8006/](https://192.168.0.7:8006/)~~ | ~~cg2~~ | proxmox cg2 subnet | vm on cg2 | na |
| - | - | - | - | na |
| [https://192.168.0.23:32400/](https://192.168.0.23:32400/) | plex | gusHPlex | app on gusHPLaptop | 00-23-8B-86-38-61 |

---

## Media Ethernet Devices

| Network Name         | MAC Address       | IP            | port  | description     | location |
|----------------------|-------------------|---------------|-------|-----------------|----|
|	na	                 | na                | na            | sw1p0 | Spectrum Modem  | sr |
|	Archer_C7	           | 18-A6-F7-31-9C-07 | 192.168.0.1   |sw1int | TP-LINK AC1720  | sr |
|----------------------|-------------------|---------------|-------|-----------------|----|
|	~~KathysRokuUltra~~	 | 84-EA-ED-A8-64-9x | na            | wifi  | KathysRokuUltra | lr |
|	KathysRokuUltra	     | 84-EA-ED-A8-64-91 | 192.168.0.21  | sw2p1 | KathysRokuUltra | lr |
|	TIVO-74600019083B6E2 | 00-11-D9-38-0B-FC | 192.168.0.22  | sw2p2 | Kathys160       | lr |
| gusHPLaptop          | 00-23-8B-86-38-61 | 192.168.0.23  | sw2p3 | gusHPLaptop     | lr |
|	Portal-8B57B421F784  | A4-0E-2B-4C-EF-C7 | 192.168.0.29  | wifi  | portaltv        | lr |
| pictureframe         | na                | na            | wifi  | picture frame   | lr |
|----------------------|-------------------|---------------|-------|-----------------|----|
|	~~StevesRokuUltra~~	     | 8C-49-62-0B-69-8C | 192.168.0.24  | ~~sw2p4~~ | StevesRokuUltra | sr |
|	StevesRokuUltra	     | 8C-49-62-0B-69-8D | 192.168.0.14  | wifi  | StevesRokuUltra | sr |
|	TIVO-8480001902B1749 | 00-11-D9-5F-47-83 | 192.168.0.15  | wifi  | Steves640       | sr |
|	TIVO-8480001902B1749 | 00-11-D9-5F-47-82 | 192.168.0.11  | sw1p1 | Steves640       | sr |
| TIVO-748000190569948 | 00-11-D9-35-02-A8 | 192.168.0.12  | sw1p2 | Steves320       | sr |
|	HDHR-10802956	       | 00-18-DD-08-02-95 | 192.168.0.13  | sw1p3 | plexTuner       | sr |
| switch 1 to 1        | na                | na       |sw1p4-sw2p0 | sw1-sw2        |sr-lr|`
|----------------------|-------------------|---------------|-------|-----------------|----|
|	cfPlex               | 10-C3-7B-46-0C-ED | 192.168.0.201 | sw1p1 | cfPlex chris's  | bm |
|	cfsg2   	           | xx-xx-F7-31-9C-xx | 192.168.0.202 | vmbrg | trueNAS_vm-cfPlex | bm |
|----------------------|-------------------|---------------|-------|-----------------|----|
|	cats-Mac-mini        | 7C-C3-A1-73-CC-A3 | 192.168.0.211  | wifi  | macmini  chris  | bm |
|	catSurface   	       | 28-18-78-C7-FC-23 | 192.168.0.212  | wifi  | suface   chris  | bm |
|	Pixel-6a    	       | 86-50-46-38-28-96 | 192.168.0.213  | wifi  | Pixel-6a chris  | bm |
| FireTV cube          | A4-08-01-60-57-35 | 192.168.0.214  | wifi  | FireTV   chris  | bm |

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

---
- [sl lan](./lan)
  - [ng network gateway](./lan/ng)
  - [sg storage gateway](./lan/sg)
  - [cg compute gateway](./lan/cg)
 
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
| 32800	| 32400	| 192.168.0.201 | slPlex on slPlex win11 | 


- [Link to CD Pictures](https://photos.app.goo.gl/gJL3BKZerkMmL1Jn7)

