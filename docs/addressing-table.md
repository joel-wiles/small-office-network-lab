# Addressing Table

| Device | Interface | IP Address | Subnet Mask | Default Gateway | How it gets its IP |
|---|---|---|---|---|---|
| R1 | G0/0 | 192.168.10.1 | 255.255.255.0 | N/A | Static |
| SW1 | VLAN 1 | 192.168.10.2 | 255.255.255.0 | 192.168.10.1 | Static |
| PC1 | NIC | 192.168.10.11+ | 255.255.255.0 | 192.168.10.1 | DHCP from R1 |
| PC2 | NIC | 192.168.10.11+ | 255.255.255.0 | 192.168.10.1 | DHCP from R1 |
| PC3 | NIC | 192.168.10.11+ | 255.255.255.0 | 192.168.10.1 | DHCP from R1 |

- Network: **192.168.10.0/24**
- Reserved for network gear and printers: **192.168.10.1 – 192.168.10.10** (excluded from DHCP)
- DHCP pool: **192.168.10.11 – 192.168.10.254**
- DNS server handed out: **8.8.8.8**

## Cabling

| From | Port | To | Port | Cable |
|---|---|---|---|---|
| R1 | G0/0 | SW1 | G0/1 | Copper straight-through |
| SW1 | Fa0/1 | PC1 | FastEthernet0 | Copper straight-through |
| SW1 | Fa0/2 | PC2 | FastEthernet0 | Copper straight-through |
| SW1 | Fa0/3 | PC3 | FastEthernet0 | Copper straight-through |
