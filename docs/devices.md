## Media Ethernet Devices

### Physical Routers and Switches

| Hardware         | location purpose      | IP         | con port  | description     | rm | link |
|------------------|-----------------------|------------|-------|-----------------|--|------|
|	na	             | na                    | na           | sw1p0 | Spectrum Modem  | sr | |
|	na	             | na                    | 192.168.1.1  | sw1p0 | Spectrum WiFi  | sr | [admin portal](http://192.168.1.1) |
| switch 1 to 2    | living room switch lr | na           |sw1p4-sw2p5 | sw1-sw2        |sr-lr| |
| switch 2 to 3    | basement switch office of | na       |sw2p4-sw3p1 | sw2-sw3        |of-bm| |
| switch 3 to 4    | basement switch livingroom lm | na   |sw3p4-sw4p1 | sw3-sw4        |lr-bm| |

### Network IP netStack

| Name     | MAC       | IP         | port  | description     | rm | link |
|------------------|-----------------------|------------|-------|-----------------|--|------|
|	ng sl Archer_C7 switch 1 sr | 18-A6-F7-31-9C-07 | 192.168.0.1  |sw1int | TP-LINK AC1720  | sr | [admin](http://192.168.0.1/) |
| slwin11ops | B0-83-FE-65-80-80 | 192.168.0.143 | sw3p? |  slwin11ops Dell i5 win11  | bm | ghadmin |
| mg2 (Hyper-V VM) | 00-15-5D-09-BF-02 | 192.168.0.140 | vswitch |  Ubuntu 24.04 VM on slwin11ops  | vm | ghadmin |
| Steve Room |-----------------------|------------|-------|-----------------|----|------|
|	TIVO-8480001902B1749 | 00-11-D9-5F-47-82 | 192.168.0.11 | sw1p1 | Steves640       | sr | |
| TIVO-748000190569948 | 00-11-D9-35-02-A8 | 192.168.0.12 | sw1p2 | Steves320       | sr | |
|	HDHR-10802956	       | 00-18-DD-08-02-95 | 192.168.0.13 | sw2p4 | plexTuner       | sr | [admin](http://192.168.0.13/) |
|	StevesRokuUltra	     | 8C-49-62-0B-69-8D | 192.168.0.14 | sw1p?  | StevesRokuUltra | sr | |
|	TIVO-8480001902B1749 | 00-11-D9-5F-47-83 | 192.168.0.15 | sw1p?  | Steves640       | sr | |
|------------------|-----------------------|------------|-------|-----------------|--|------|
|	TIVO-xxx | 00-11-D9-xx-xx-xx | 192.168.0.16 | wf-zt  | gusTV6       | sr | |
|	TIVO-xxx | 00-11-D9-xx-xx-xx | 192.168.0.17 | wf-zt  | gusTV7       | sr | |
|------------------|-----------------------|------------|-------|-----------------|--|------|
|	TIVO-xxx | 00-11-D9-3B-34-CB | 192.168.0.18 | cf-zt  | gusTV8       | sr | |
|	TIVO-xxx | 00-11-D9-xx-xx-xx | 192.168.0.19 | cf-zt  | gusTV9       | sr | |
| Living Room |-----------------------|--------------|-------|-----------------|----|------|
|	~~KathysRokuUltra~~	 | 84-EA-ED-A8-64-9x | na           | wifi  | KathysRokuUltra | lr | |
|	KathysRokuUltra	     | 84-EA-ED-A8-64-91 | 192.168.0.21 | sw2p1 | KathysRokuUltra | lr | |
|	TIVO-74600019083B6E2 | 00-11-D9-38-0B-FC | 192.168.0.22 | sw2p2 | Kathys160       | lr | |

### Other devices temp

| Name | MAC          | IP         | port  | description     | rm | link |
|--------------|--------------|------------|-------|-----------------|----|------|
| gusHPLaptop          | 00-23-8B-86-38-61 | 192.168.0.23 | sw2p3 | gusHPLaptop win10 | lr | ghadmin |
| gusGram              | AC-74-B1-02-FB-CF | 192.168.0.28 | wifi  | gusGram win11 i7 | lr | ghadmin |
|	cats-Mac-mini        | 7C-C3-A1-73-CC-A3 | 192.168.0.211 | sw3p4  | macmini  chris  | bm | cat ghadmin |
|	catSurface   	       | 28-18-78-C7-FC-23 | 192.168.0.212 | sw3p5  | suface   chris  | bm | cat ghadmin |
|	Pixel-6a    	       | 86-50-46-38-28-96 | 192.168.0.213 | wifi  | Pixel-6a chris  | bm | |
| FireTV cube          | A4-08-01-60-57-35 | 192.168.0.214 | wifi  | FireTV   chris  | bm | |



