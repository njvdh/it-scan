# it-scan

A minimalist infrastructure scanner for Linux hosts (Proxmox, Incus) and Ruckus Wireless networks.

## Features
- **Linux Inventory:** Remote status check via SSH for Uptime, Storage, and ZFS pools.
- **Virtualization Support:** Automatically detects and lists running Proxmox VMs and Incus containers.
- **Ruckus WiFi:** Scans Ruckus APs via SNMP. Supports both legacy OIDs and modern OIDs (e.g., R350/R550) for client counting.

## Requirements
- `snmp` tools installed on the scanning host.
- SSH key-based access to target Linux hosts.
- SNMP enabled on Ruckus Access Points.

## Usage
```bash
./it-scan wifi   # Scan only WiFi APs
./it-scan linux  # Scan only Linux hosts
./it-scan all    # Run full inventory
