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
