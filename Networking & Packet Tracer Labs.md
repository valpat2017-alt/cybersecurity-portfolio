# Cisco Packet Tracer – DHCP & Network Segmentation Lab

## Project Overview
This project demonstrates the configuration of **Dynamic Host Configuration Protocol (DHCP)** and **network segmentation** using Cisco Packet Tracer. The goal was to automate IP address assignment across multiple subnets and enable communication between devices in different broadcast domains.


## 🖥️ Lab Topology
- **Router0 (Cisco 1941)**
  - GigabitEthernet0/0 → Subnet 1 (`192.168.1.0/24`)
  - GigabitEthernet0/1 → Subnet 2 (`192.168.2.0/24`)
- **Switch0** → PCs in Subnet 1
- **Switch1** → PCs in Subnet 2
- **PCs (PC0–PC15)** connected across both subnets


##  Configuration Steps
### Static IP Setup
- Assigned `192.168.1.1/24` to Router Fa0/0
- Assigned `192.168.2.1/24` to Router Fa0/1
- Verified connectivity with `ping` from PCs to router interfaces

### DHCP Pools
```bash
ip dhcp excluded-address 192.168.1.1 192.168.1.10
ip dhcp pool LAN1
 network 192.168.1.0 255.255.255.0
 default-router 192.168.1.1
 dns-server 8.8.8.8

ip dhcp excluded-address 192.168.2.1 192.168.2.10
ip dhcp pool LAN2
 network 192.168.2.0 255.255.255.0
 default-router 192.168.2.1
 dns-server 8.8.8.8
