
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
| cable feed   | main cable | spl03    | sr |
| spl03 feed | spl03p1 | spectrum modem       | sr |
| spl04 feed | spl03p1   | spl04 input       | sr |
| Steves640 feed | spl04p1 | Steves320 Tivo ant | sr |
| Kathys160 feed | spl04p3 | Kathys160 ant | lr |


---
2023.07.23
```
ID	Client Name	MAC Address	Assigned IP	Lease Time
1	catSurface	28-18-78-C7-FC-23	192.168.0.116	01:32:05
2	ghwin11	10-C3-7B-46-0C-ED	192.168.0.97	Permanent
3	Unknown	B6-79-9D-1C-41-FD	192.168.0.102	01:43:07
4	wlan0	CC-8C-BF-F6-79-29	192.168.0.103	01:28:37
5	wlan0	A0-92-08-61-0F-8A	192.168.0.104	01:29:05
6	TIVO-8480001902B1749	00-11-D9-5F-47-82	192.168.0.112	01:29:42
7	Unknown	FE-24-B4-B0-5E-35	192.168.0.115	01:53:16
8	TIVO-8480001902B1749	00-11-D9-5F-47-83	192.168.0.120	01:29:42
9	Unknown	A4-08-01-60-57-35	192.168.0.106	01:29:42
10	Unknown	1A-64-1A-7E-00-3D	192.168.0.110	01:32:43
11	BRW485AB64C63EF	48-5A-B6-4C-63-EF	192.168.0.122	01:29:53
12	Unknown	E4-E0-C5-00-52-8B	192.168.0.109	00:34:12
13	Pixel-6a	86-50-46-38-28-96	192.168.0.118	01:30:22
14	cats-Mac-mini	7C-C3-A1-73-CC-A3	192.168.0.107	01:30:18
15	A6386161	7C-B5-66-05-9D-C6	192.168.0.125	01:37:30
16	Portal-8B57B421F784	A4-0E-2B-4C-EF-C7	192.168.0.108	01:30:43
17	TIVO-74600019083B6E2	00-11-D9-38-0B-FC	192.168.0.113	01:50:21
18	KathysRokuUltra	84-EA-ED-A8-64-91	192.168.0.114	01:52:41
19	Unknown	16-2F-4E-27-3D-1F	192.168.0.111	01:58:26
20	android-4de9db6d80c2f04c	AC-D0-74-13-A8-78	192.168.0.105	01:45:27
21	StevesRokuUltra	8C-49-62-0B-69-8D	192.168.0.124	01:04:24
22	William-s-A02s	F2-E7-8B-A4-F1-B4	192.168.0.117	01:56:59
```

res
```
ID	MAC Address	Reserved IP Address	Status	Modify
1	D4-CA-6D-7C-E6-52	192.168.0.100	Enabled	Modify Delete
2	C8-2A-14-36-3D-9D	192.168.0.3	Enabled	Modify Delete
3	B2-57-A9-45-F1-72	192.168.0.99	Enabled	Modify Delete
4	B6-8B-7B-41-04-88	192.168.0.98	Enabled	Modify Delete
5	1A-59-CC-25-96-5D	192.168.0.2	Enabled	Modify Delete
6	00-23-8B-86-38-61	192.168.0.121	ghHPLaptop
7	02-A2-0B-C2-0B-F5	192.168.0.101	Enabled	Modify Delete
8	9E-2C-18-B7-59-8C	192.168.0.33	Enabled	Modify Delete
```

fw
```
ID	Service Port	Internal Port	IP Address	Protocol	Status	Modify
1	32400	32400	192.168.0.105	ALL	Enabled	Modify Delete
2	80	8010	192.168.0.98	TCP	Enabled	Modify Delete
3	32500	32400	192.168.0.99	ALL	Enabled	Modify Delete
4	32800	32400	192.168.0.107	ALL	Enabled	Modify Delete
```
D	Client Name	MAC Address	Assigned IP	Lease Time
1	KathysRokuUltra	84-EA-ED-A8-64-91	192.168.0.105	01:44:08
2	StevesRokuUltra	8C-49-62-0B-69-8D	192.168.0.103	01:47:44
3	TIVO-74600019083B6E2	00-11-D9-38-0B-FC	192.168.0.104	01:44:09
7	TIVO-8480001902B1749	00-11-D9-5F-47-82	192.168.0.112	01:44:20
9	TIVO-8480001902B1749	00-11-D9-5F-47-83	192.168.0.120	01:44:21
13	Portal-8B57B421F784	A4-0E-2B-4C-EF-C7	192.168.0.111	01:44:43
17	HDHR-10802956	00-18-DD-08-02-95	192.168.0.118	01:13:52
19	Pixel-6a	86-50-46-38-28-96	192.168.0.119	01:18:49
21	cats-Mac-mini	7C-C3-A1-73-CC-A3	192.168.0.123	01:43:46
