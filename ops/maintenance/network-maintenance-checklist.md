# SL Network Maintenance Checklist

## ⚠️ ACTION REQUIRED - DHCP Reservation for slwin11ops
- [ ] **slwin11ops LAN IP is drifting** - observed as both 192.168.0.143 and 192.168.0.141
- [ ] **Add DHCP reservation** on router (192.168.0.1) for MAC `B0-83-FE-65-80-80`
- [ ] **Confirm DNS change** - newer output shows Cloudflare DNS (1.1.1.1, 1.0.0.1) instead of router DNS
- [ ] **Confirm WSL2 status** - WSL adapter missing from latest ipconfig /all output
- [ ] Once reservation is set, update docs with the final static IP

## ✅ COMPLETED - Merged slwin11ops-notes.md
- [x] Merged root-level slwin11ops-notes.md (fresh ipconfig /all) into ops/install/slwin11ops-notes.md
- [x] Replaced old abbreviated ipconfig with full /all output
- [x] Added ZeroTier CLI status (v1.14.2 ONLINE)
- [x] Documented all differences between old and new runs
- [x] Removed duplicate root-level file

## ✅ COMPLETED - Mothballed Machines Cleanup
- [x] **Removed slwin11 (192.168.0.9)** - All references cleaned from documentation
- [x] **Removed sg2 QNAP (192.168.0.6)** - All storage references cleaned
- [x] **Updated storage.md** - Removed slDVR storage mappings and deprecated shares
- [x] **Updated DHCP table** - Removed mothballed machines, fixed gusHPLaptop IP
- [x] **Updated External Services** - Removed slDVR Plex reference
- [x] **Updated Maintenance section** - Now references only active cf Plex services

## ✅ COMPLETED - Critical IP Address Fix
- [x] **RESOLVED: slwin11ops IP Address** - Fixed from incorrect 192.168.0.3 to actual 192.168.0.143
- [x] **Confirmed ZeroTier IP** - 10.147.17.94 is correct ✅
- [x] **Updated slwin11ops-notes.md** - All service references now use correct IP
- [x] **Verified from ipconfig output** - ExternalHVether adapter shows 192.168.0.143

## ✅ COMPLETED - Deprecated Services Cleanup
- [x] **Removed old bradnordyke.com Cloudflare tunnels** from README.md
- [x] **Cleaned up services.md** - Removed deprecated CasaOS, Guacamole, old Proxmox entries
- [x] **Updated devices.md** - Removed placeholder entries, fixed gusHPLaptop IP
- [x] **Fixed MAC addresses** - Added correct MAC for slwin11ops (B0-83-FE-65-80-80)
- [x] **Removed Pre-2025 section** - Cleaned up outdated topology information
- [x] **Standardized documentation** - Improved structure and removed broken links

## 🔍 REMAINING VERIFICATION NEEDED

### 1. Cloudflare Tunnel Status ✅ (Partially confirmed)
- [x] **traefik.2cld.com** - ✅ Active (Cloudflare Access protected)
- [x] **portainer.2cld.com** - ✅ Active (Cloudflare Access protected)  
- [ ] **gitea.2cld.com** - ❌ HTTP 530 error (service may be down)
- [ ] **slcp.2cld.com** - ❌ HTTP 530 error (service may be down)

### 2. Local Service Verification (slwin11ops - 192.168.0.143)
- [ ] Test local Plex: http://192.168.0.143:32400/
- [ ] Test local Portainer: http://192.168.0.143:9000/
- [ ] Test local Traefik: http://192.168.0.143:80/

### 3. ZeroTier Network Status ✅ (Confirmed)
- [x] slwin11ops ZT IP: 10.147.17.94 ✅ 
- [x] mg2 ZT IP: 10.147.17.135 ✅ 
- [ ] Complete gusHPLaptop ZT IP: 10.147.17.??
- [ ] Verify gusGram ZT IP: 10.147.17.190

## 🔧 COMMANDS TO RUN FOR VERIFICATION

### On slwin11ops (192.168.0.143):
```cmd
ipconfig /all
zerotier-cli status
zerotier-cli listnetworks
```

### On mg2 VM (192.168.0.140):
```bash
ip a
zerotier-cli status
docker ps
docker-compose ps
```

### Network Tests:
```cmd
ping 192.168.0.6    # sg2 QNAP (if running)
ping 192.168.0.9    # slwin11 (if running)
ping 10.147.17.135  # mg2 ZT
ping 10.147.17.94   # slwin11ops ZT
```

## 📋 REMAINING DOCUMENTATION UPDATES

### After Verification, Update These Files:
- [ ] **docs/storage.md** - Remove references to down services
- [ ] **docs/README.md** - Update DHCP table with current devices
- [ ] **ops/install/slwin11ops-notes.md** - Fix IP reference (192.168.0.3 → 192.168.0.143)
- [ ] **Complete missing ZeroTier IPs** in services.md

## 🎯 NEXT STEPS
1. **Run verification commands** to determine actual service status
2. **Test service URLs** to confirm what's actually running
3. **Update documentation** to match reality
4. **Remove storage mappings** for services that are actually down