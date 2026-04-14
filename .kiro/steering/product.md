# SL Home Lab Infrastructure

This repository documents the "SL" home lab network infrastructure, a comprehensive home networking setup that includes multiple sites (sl, cf, wf) connected via ZeroTier VPN.

## Core Purpose
- Document network topology, services, and device configurations
- Maintain operational procedures for home lab infrastructure
- Track Plex media servers, storage systems, and compute resources
- Provide reference documentation for network administration

## Key Components
- **Network Infrastructure**: TP-Link routers, managed switches, ZeroTier VPN
- **Media Services**: Multiple Plex servers (slDVR, cfPlex, cfDVR) with distributed storage
- **Compute Resources**: Windows 11 workstations, Hyper-V VMs, Docker containers
- **Storage Systems**: QNAP NAS, TrueNAS systems, local storage arrays
- **Remote Access**: RDP, Google Remote Desktop, SSH tunnels

## Sites
- **sl**: Primary site (192.168.0.0/24) - Main home lab
- **cf**: Secondary site (192.168.6.0/24) - Remote location
- **wf**: Tertiary site (192.168.9.0/24) - Additional services

The documentation follows the netstack.org architecture patterns and serves as both operational reference and disaster recovery documentation.