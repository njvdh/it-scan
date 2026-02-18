# it-scan

A minimalist infrastructure scanner designed for system administrators managing mixed environments of Linux hosts (Proxmox, Incus) and Ruckus Wireless networks.

## Features
- **Linux Inventory:** Rapid remote status checks via SSH, including:
  - Uptime and Load averages.
  - Disk storage utilization.
  - **ZFS Health:** Real-time status of ZFS pools.
- **Virtualization Intelligence:** Automatically detects and lists running Proxmox VMs and Incus containers on target hosts.
- **Ruckus WiFi Monitoring:** Scans Ruckus Access Points via SNMP. 
  - Dual-mode support: Compatible with both legacy OIDs and modern OIDs (tested on R350/R550).
  - Client count tracking per AP.

## Requirements
- `snmp` client tools installed on the scanning host.
- SSH key-based access to target Linux hosts (for non-interactive scanning).
- SNMP enabled on Ruckus Access Points.

## Setup
1. Copy `it-scan.conf.example` to `it-scan.conf`.
2. Edit `it-scan.conf` to include your host IPs and SNMP community strings.

## Usage
```bash
./it-scan wifi   # Scan WiFi Access Points only
./it-scan linux  # Scan Linux/Proxmox/Incus hosts only
./it-scan all    # Run full infrastructure inventory
