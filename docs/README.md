
- [sl lan](./lan)
  - [ng network gateway](./lan/ng)
  - [sg storage gateway](./lan/sg)
  - [cg compute gateway](./lan/cg)
 
---

| Service admin Link  | type    | description | location    |
|---------------------|---------|-------------|-------------|
| [http://192.168.0.1/](http://192.168.0.1/) | ng | tp-link ng on subnet | sl gb |
| [http://192.168.0.2/](http://192.168.2.2/) | sg | truenas sg on subnet | vm on cg |
| [https://192.168.0.2:443/](https://192.168.2.2:443/) | sg | truenas (https) sg on subnet | vm on cg |
| [https://192.168.0.3:8006/](https://192.168.2.3:8006/) | cg | proxmox cg subnet | cg hardware |
| - | - | - | - |
| [http://192.168.0.6:81/](http://192.168.0.6:81/) | sg2 | truenas2 sg2 on subnet | vm on cg2 |
| [https://192.168.0.6:444/](https://192.168.0.6:444/) | sg2 | truenas2 (https) sg2 on subnet | vm on cg2 |
| [https://192.168.0.7:8006/](https://192.168.0.7:8006/) | cg2 | proxmox cg2 subnet | vm on cg2 |
| - | - | - | - |
| [https://192.168.0.121:32400/](https://192.168.0.121:32400/) | plex | gusHPlex | app on gusHPLaptop |

---

## Media Ethernet Devices

| Network Name         | MAC Address       | IP            | port  | description     | location |
|----------------------|-------------------|---------------|-------|-----------------|----------|
|	KathysRokuUltra	     | 84-EA-ED-A8-64-91 | 192.168.0.105 | sw2p1 | KathysRokuUltra | lr |
|	TIVO-74600019083B6E2 | 00-11-D9-38-0B-FC | 192.168.0.104 | sw2p2 | Kathys160       | sr |
| gusHPlex             | na                | na            | ss2p3 | picture frame   | lr |
|	Portal-8B57B421F784  | A4-0E-2B-4C-EF-C7 | 192.168.0.111 | wifi  | portaltv        | lr |
| pictureframe         | na                | na            | wifi  | picture frame   | lr |
|----------------------|-------------------|---------------|-------|-----------------|----------|
|	StevesRokuUltra	     | 8C-49-62-0B-69-8D | 192.168.0.103 | wifi  | StevesRokuUltra | sr |
|	TIVO-8480001902B1749 | 00-11-D9-5F-47-83 | 192.168.0.120 | wifi  | Steves640       | sr |
|	TIVO-8480001902B1749 | 00-11-D9-5F-47-82 | 192.168.0.112 | sw1p1 | Steves640       | sr |
| TIVO-748000190569948 | 00-11-D9-35-02-A8 | 192.168.0.102 | sw1p2 | Steves320       | sr |
|	HDHR-10802956	       | 00-18-DD-08-02-95 | 192.168.0.118 | sw1p3 | plexTuner       | sr |
| switch 1 to 1        | na                | na            | sw1p4-sw2p0 | sw1-sw2 | sr-lr |`

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

- [Link to CD Pictures](https://photos.app.goo.gl/gJL3BKZerkMmL1Jn7)
- tbd
