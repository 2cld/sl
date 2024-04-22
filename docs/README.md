[edit](https://github.com/2cld/sl/edit/main/docs/README.md)

| External Service             | type | description | location    |
|------------------------------|------|-------------|-------------|
|      24.216.208.251 : 32500  | 0.9 plex | [slDVR](https://24.216.208.251:32500) | sl |
|      24.149.22.11   : 32400  | 6.3 plex | [cfPlex](https://24.149.22.11:32400) | cf |
|      24.149.22.11   : 32500  | 6.6 plex | [cfDVR](https://24.149.22.11:32500)  | cf |
| test.christrees.com :  2020  | 6.2 ssh  | sg | cf |
| test.christrees.com :  2021  | 6.6 ssh  | sg2 | cf |

- [tv.2cld.net](https://tv.2cld.net/)
- [cf.2cld.net/docs](https://cf.2cld.net/docs)
- [sl.2cld.net/docs](https://sl.2cld.net/docs)
- [netstack.org/docs](https://netstack.org/docs/)

| Service admin Link  | type    | description | location    | mac |
|---------------------|---------|-------------|-------------|-----|
| - | ns | netstack [ns docs](https://netstack.org/docs/) | - | - |
| [http://192.168.0.1/](http://192.168.0.1/) | ng | tp-link [AC1750 Archer C7 doc](https://static.tp-link.com/res/down/doc/Archer_C7_V1_UG.pdf) ng | sl gb | 18-A6-F7-31-9C-06 |
| ~~[http://192.168.0.2/](http://192.168.2.2/)~~ | sg | nas sg | vm on cg | na |
| [https://192.168.0.3:8006/](https://192.168.0.3:8006/) | cg | [root](https://192.168.0.3:8006/) proxmox cg | cg on i3 macmini hw | na |
| - | ns2 | - | ns backup | na |
| ~~[http://192.168.0.5/](http://192.168.0.5/)~~ | ng2 | backup network gw | sl gb | na |
| [http://192.168.0.6:8080/](http://192.168.0.6:8080/) | sg2 | [buadmin](http://192.168.0.6:8080/) qnap sg2 5.3TB Raid 0.5TB Used | sl-sb-sw3p2 | 00-08-9B-E2-83-93 |
| ~~[http://192.168.0.7:8006/](http://192.168.0.5/7:8006)~~ | cg2 | backup compute gw | sl gb | na |
| Plex Services | - | - | - | na |
| [https://192.168.0.9:32400/](https://192.168.0.9:32400/) | slDVR | [slDVR](https://24.216.208.251:32500) on slwin11 -zt-10.147.17.198 .25TB-C 1.8TB-D 1.8TB-E | win app | 00-15-17-5B-F2-80 |
|---------------------|---------|-------------|-------------|-----|
| [Gus - Dashboard CasaOS](http://192.168.0.70/) | app |  vm slcg-100 | sl | 08-00-27-84-49-45 |
| [Gus - Remote - Guacamole](http://192.168.0.70:8090/guacamole/#/)  | [ghadmin](http://192.168.0.70:8090/guacamole/#/) | casoOS app | sl | 08-00-27-84-49-xx |
| [Gus - HomeAssistant](http://192.168.0.10:8123/) | ha | - | - | na |
| sl proxmox vms |---------|-------------|-------------|-----|
| [http://192.168.0.70](http://192.168.0.70/)  | CasaOS | vm slcg-100 | sl | 08-00-27-84-49-45 |
| [http://192.168.0.71:8090](http://192.168.0.70:8090/guacamole/#/)  | Guacamole | casoos app | sl | 08-00-27-84-49-xx |
| ~~[https://192.168.0.6:32400/](https://192.168.0.6:32400/)~~ | ~~slPlex~~ | ~~[slPlex](https://24.216.208.251:32400) on sg2~~ removed | vm sl-101 | 00-08-9B-E2-83-93 |
| ~~[192.168.0.10:8123](http://192.168.0.10:8123/)~~  | ha | vm slwin11 | sl | 08-00-27-84-49-45 |
| user machines | - | - | - | na |
| 192.168.0.9  slwin11  | win11 | Dell 1U win11 zt-10.147.17.198 | sl | 00-15-17-5B-F2-80 |
| 192.168.0.28 gusGram	| win11 | gus new laptop | sl | AC-74-B1-02-FB-CF |	
| 192.168.0.23 gusHPLaptop	| win10 | gus old laptop | sl | 00-23-8B-86-38-61 |	

---
## Maintainance
- Plex check [slDVR](https://24.216.208.251:32500)
- NAS Storage sg check [http://192.168.0.6:8080/](http://192.168.0.6:8080/)
- Proxmox slcg check [https://192.168.0.3:8006/](https://192.168.0.3:8006/)
- slwin11 check [Gus - Remote - Guacamole](http://192.168.0.70:8090/guacamole/#/) - slwin
- CasaOS check [Gus - Dashboard CasaOS](http://192.168.0.70/)
- Router check [http://192.168.0.1/](http://192.168.0.1/)

---
---
Below has Moved to [storage.md](./storage.md)
---

## slDVR Storage Mapping (10.147.17.198 - 192.168.0.9)

| slDVR 10.147.17.198 /192.168.0.9 | Plex | Plex Libraries | location | size TB |
|-----------------------------------|------|-------------|-------------|-----|
| C: local | none | system | sl | 0.25 |
| D: local | none  | local | sl | 1.81 |
| E: local | none  | local | sl | 1.81 |
| G: \\192.168.0.6\plex | slDVR | [gusHPlexG.md](./gusHPlexG) remoted storage | sl | 5.33 |
| T: \\10.147.19.228\catDVR | cfPlex  | TrueNAS catbox in catpool storage | cf | 1.00 |

## cfPlex Storage Mapping (10.147.17.228 - 192.168.6.2) from [https://cf.2cld.net/docs/](https://cf.2cld.net/docs/)

| cfPlex 10.147.17.228 /192.168.6.2 | Plex | Plex Libraries | location | size TB |
|-----------------------------------|------|-------------|-------------|-----|
| C: local                          | none | none | cf | 0.90 |
| D: \\10.147.19.198\slShareD       | none  | zt remote | sl | 1.81 |
| E: \\10.147.19.198\slShareE       | none  | zt remote | sl | 1.81 |
| ~~G: \\10.147.17.66\gusHPlexSFEPart~~ | gusHPlex | [gusHPlexG.md](./gusHPlexG) remoted storage | sl | 0.90 |
| ~~H: \\192.168.6.2\ghpool~~       | cfPlex  | TrueNAS ghpool storage | cf | 0.90 |
| ~~M: \\192.168.6.2\MediaShare~~   | cfPlex  | TrueNAS MediaShare storage | cf | 0.90 |
| ~~N: \\192.168.6.2\catbox~~       | cfPlex  | TrueNAS catbox in catpool storage | cf | 0.90 |
| O: \\192.168.6.10\plexnsds        | cfPlex  | [cfPlex0.md](./cfPlex0) StarTrek storage | cf | 1.78 |
| P: \\192.168.6.6\pshare           | cfDVR | Synology NAS storage | cf | 10.0 |

---
---
Below has Moved to [devices.md](./devices.md)
---

## Media Ethernet Devices

| Network Name     | MAC Address-          | IP         | port  | description     | rm | link |
|------------------|-----------------------|------------|-------|-----------------|--|------|
|	na	                 | na                | na           | sw1p0 | Spectrum Modem  | sr | |
|	Archer_C7 switch 1 sr | 18-A6-F7-31-9C-07 | 192.168.0.1  |sw1int | TP-LINK AC1720  | sr | [admin](http://192.168.0.1/) |
| switch 1 to 2        | living room switch lr | na      |sw1p4-sw2p5 | sw1-sw2        |sr-lr| |
| switch 2 to 3        | basement switch bm    | na      |sw2p4-sw3p1 | sw2-sw3        |lr-bm| |
| Steve Room |-----------------------|------------|-------|-----------------|----|------|
|	~~StevesRokuUltra~~	| 8C-49-62-0B-69-8C | 192.168.0.24 | ~~sw2p4~~ | StevesRokuUltra | sr | |
|	StevesRokuUltra	     | 8C-49-62-0B-69-8D | 192.168.0.14 | wifi  | StevesRokuUltra | sr | |
|	TIVO-8480001902B1749 | 00-11-D9-5F-47-83 | 192.168.0.15 | wifi  | Steves640       | sr | |
|	TIVO-8480001902B1749 | 00-11-D9-5F-47-82 | 192.168.0.11 | sw1p1 | Steves640       | sr | |
| TIVO-748000190569948 | 00-11-D9-35-02-A8 | 192.168.0.12 | sw1p2 | Steves320       | sr | |
|	HDHR-10802956	       | 00-18-DD-08-02-95 | 192.168.0.13 | sw2p4 | plexTuner       | sr | [admin](http://192.168.0.13/) |
| Living Room |-----------------------|--------------|-------|-----------------|----|------|
|	~~KathysRokuUltra~~	 | 84-EA-ED-A8-64-9x | na           | wifi  | KathysRokuUltra | lr | |
|	KathysRokuUltra	     | 84-EA-ED-A8-64-91 | 192.168.0.21 | sw2p1 | KathysRokuUltra | lr | |
|	TIVO-74600019083B6E2 | 00-11-D9-38-0B-FC | 192.168.0.22 | sw2p2 | Kathys160       | lr | |
| gusHPLaptop          | 00-23-8B-86-38-61 | 192.168.0.23 | sw2p3 | gusHPLaptop win10 | lr | [gusHPlex](http://192.168.0.23:32400) ghadmin |
| switch 2 to 3        | basement switch bm    | na      |sw2p4-sw3p1 | sw2-sw3        |lr-bm| |
| gusGram              | AC-74-B1-02-FB-CF | 192.168.0.28 | wifi  | gusGram win11 i7 | lr | rmdesk ghadmin |
|	Portal-8B57B421F784  | A4-0E-2B-4C-EF-C7 | 192.168.0.29 | wifi  | portaltv        | lr | |
| pictureframe         | na                | na           | wifi  | picture frame   | lr | |
| Basement         |-----------------------|------------|-------|-----------------|----|------|
| switch 2 to 3        | basement switch bm    | na      | sw2p4-sw3p1 | sw2-sw3        |lr-bm| |
|	sg2               | 00-08-9B-E2-83-93 | 192.168.0.6 | sw3p2 | [slPlex](https://192.168.0.6:32400)  | bm | [buadmin](http://192.168.0.6:8080/) |
|	slwin11 on hw | 00-15-17-5B-F2-80 | 192.168.0.9 | sw3p3 |  [slDVR](https://192.168.0.9:32400)  | bm | sladmin ghadmin |
|	ubunt22 vm on slwin11 | 08-00-27-00-5C-A0 | 192.168.0.10 | vswitch | not running  | vm | ubuntu22 ghadmin |
| Basement temp |-----------------------|------------|-------|-----------------|----|------|
|	cats-Mac-mini        | 7C-C3-A1-73-CC-A3 | 192.168.0.211 | sw3p4  | macmini  chris  | bm | cat ghadmin |
|	catSurface   	       | 28-18-78-C7-FC-23 | 192.168.0.212 | sw3p5  | suface   chris  | bm | cat ghadmin |
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
| 32400	| 32400	| 192.168.0.6  | slPlex on sg2 | 
| 32500	| 32400	| 192.168.0.9 | slDVR on slwin11 | 
| 32400	| 32400	| 192.168.0.23  | removed ~~gusHPlex~~ on gusHPLaptop | 
|  2020 |    22 | 192.168.0.202 | cf-sg2 cattemp truenas | 

MAC Res
```
ID	MAC Address	Reserved IP Address	Status	Modify
1	84-EA-ED-A8-64-91	192.168.0.21	Enabled	Modify Delete
2	00-11-D9-38-0B-FC	192.168.0.22	Enabled	Modify Delete
3	00-23-8B-86-38-61	192.168.0.23	Enabled	Modify Delete
4	8C-49-62-0B-69-8C	192.168.0.24	Enabled	Modify Delete
5	00-11-D9-5F-47-82	192.168.0.11	Enabled	Modify Delete
6	00-11-D9-35-02-A8	192.168.0.12	Enabled	Modify Delete
7	00-18-DD-08-02-95	192.168.0.13	Enabled	Modify Delete
8	8C-49-62-0B-69-8D	192.168.0.14	Enabled	Modify Delete
9	00-11-D9-5F-47-83	192.168.0.15	Enabled	Modify Delete
10	7C-C3-A1-73-CC-A3	192.168.0.211	Enabled	Modify Delete
11	28-18-78-C7-FC-23	192.168.0.212	Enabled	Modify Delete
12	86-50-46-38-28-96	192.168.0.213	Enabled	Modify Delete
13	A4-08-01-60-57-35	192.168.0.214	Enabled	Modify Delete
14	A4-0E-2B-4C-EF-C7	192.168.0.29	Enabled	Modify Delete
15	10-C3-7B-46-0C-ED	192.168.0.201	Enabled	Modify Delete
16	00-15-5D-02-71-03	192.168.0.202	Enabled	Modify Delete
17	AC-74-B1-02-FB-CF	192.168.0.28	Enabled	Modify Delete
18	00-08-9B-E2-83-93	192.168.0.6	Enabled	Modify Delete
19	00-15-17-5B-F2-80	192.168.0.9	Enabled	Modify Delete
20	08-00-27-84-49-45	192.168.0.10	Enabled	Modify Delete
```

DHCP 
```
ID	Client Name	MAC Address	Assigned IP	Lease Time
1	android-4de9db6d80c2f04c	AC-D0-74-13-A8-78	192.168.0.110	01:03:48
2	wlan0	CC-8C-BF-F6-79-29	192.168.0.100	01:19:17
3	StevesRokuUltra	8C-49-62-0B-69-8D	192.168.0.14	Permanent
4	TIVO-748000190569948	00-11-D9-35-02-A8	192.168.0.12	Permanent
5	500-64dba0f5f089	64-DB-A0-F5-F0-89	192.168.0.101	01:37:15
6	TIVO-8480001902B1749	00-11-D9-5F-47-82	192.168.0.11	Permanent
7	TIVO-8480001902B1749	00-11-D9-5F-47-83	192.168.0.15	Permanent
8	Unknown	A4-08-01-60-57-35	192.168.0.214	Permanent
9	BRW485AB64C63EF	48-5A-B6-4C-63-EF	192.168.0.122	01:19:37
10	Unknown	FE-24-B4-B0-5E-35	192.168.0.103	00:53:36
11	Unknown	C6-9A-1C-84-72-48	192.168.0.106	01:46:48
12	Unknown	1A-64-1A-7E-00-3D	192.168.0.109	01:01:32
13	catSurface	28-18-78-B7-BE-B7	192.168.0.107	01:57:15
14	gusGram	AC-74-B1-02-FB-CF	192.168.0.28	Permanent
15	Portal-744CF7122AD3	A4-0E-2B-3C-A7-62	192.168.0.105	01:52:18
16	sg2	00-08-9B-E2-83-93	192.168.0.6	Permanent
17	cats-Mac-mini	3C-07-54-72-49-E2	192.168.0.104	01:00:47
18	slwin11	00-15-17-5B-F2-80	192.168.0.9	01:21:47
19	amazon-4f24e65ad	A0-02-DC-F7-1B-62	192.168.0.102	01:09:23
20	Unknown	16-2F-4E-27-3D-1F	192.168.0.111	00:25:45
21	gusHPLaptop	00-23-8B-86-38-61	192.168.0.23	Permanent
22	Pixel-6a	4A-8C-7F-77-D9-02	192.168.0.112	01:11:06
23	Pixel-6a	86-50-46-38-28-96	192.168.0.213	Permanent
24	Portal-8B57B421F784	A4-0E-2B-4C-EF-C7	192.168.0.29	Permanent
25	wlan0	A0-92-08-68-FC-EE	192.168.0.113	00:31:25
26	LGwebOSTV	7C-1C-4E-5D-C5-F6	192.168.0.136	01:48:51
```



