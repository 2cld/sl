# SL Network Services

- Subnet 192.168.0.0/24
- Gateway 192.168.0.1
- DNS 192.168.0.1
- ssh ghadmin@10.147.17.135 -> mg2 nsUb2404 on SLWIN11OPS Hyper-V vm
```
ssh ghadmin@10.147.17.135
```
- ssh -p 2222 ghadmin@10.147.17.94 -> wsl SLWIN11OPS
```
ssh -p 2222 ghadmin@10.147.17.94
```

| Service admin Link  | type    | description | location    | mac |
|---------------------|---------|-------------|-------------|-----|
| ops machines | - | - | - | na |
| 192.168.0.143  [slwin11ops-notes](../ops/install/slwin11ops-notes)  | win11 | Dell i5 win11 [zt-10.147.17.94](https://my.zerotier.com/network/d5e5fb65371eb4a4) | sl | B0-83-FE-65-80-80 |
| 192.168.0.140  [slwin11ops-hv-mg2-notes](../ops/install/slwin11ops-hv-mg2-notes)  | Ub2404 | hv-vm Dell i5 win11 [zt-10.147.17.135](https://my.zerotier.com/network/d5e5fb65371eb4a4) | sl | 00:15:5d:09:bf:02 |
| 192.168.0.28 gusGram	| win11 | gus new laptop [zt-10.147.17.190](https://my.zerotier.com/network/d5e5fb65371eb4a4) | sl | AC-74-B1-02-FB-CF |	
| 192.168.0.23 gusHPLaptop	| win10 | gus old laptop [zt-10.147.17.??](https://my.zerotier.com/network/d5e5fb65371eb4a4) | sl | 00-23-8B-86-38-61 |	
| - | ns | netstack [ns docs](https://netstack.org/docs/) | - | - |
| [http://192.168.0.1/](http://192.168.0.1/) | ng | tp-link [AC1750 Archer C7 doc](https://static.tp-link.com/res/down/doc/Archer_C7_V1_UG.pdf) ng | sl gb | 18-A6-F7-31-9C-06 |

---
