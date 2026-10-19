# Mini NOC Network Monitoring Lab

A personal lab project combining Cisco network simulation and Linux server monitoring to practice fundamental Network Operations Center (NOC) tasks.

## 1. Project Overview

This project simulates a small enterprise network using Cisco Packet Tracer and deploys a Zabbix monitoring environment on Ubuntu Server.

The main objectives are to practice network configuration, server monitoring, alert notification, and basic troubleshooting.

## 2. Technologies

- **Networking:** Cisco Packet Tracer, Cisco IOS, VLAN, Inter-VLAN Routing, Static Routing
- **Operating System:** Ubuntu Server
- **Virtualization:** VMware
- **Monitoring:** Zabbix Server, Zabbix Agent 2
- **Database & Web:** MySQL, Apache
- **Alerting:** Gmail SMTP
- **Troubleshooting:** Linux CLI, Ping, Traceroute, Systemctl

## 3. Lab Architecture

### Cisco Network Simulation

The simulated network consists of Cisco routers, switches, and end devices.

Implemented configurations:
- VLAN segmentation
- Inter-VLAN routing
- Static routing between subnets
- IP addressing and default gateway configuration
- Connectivity verification between network devices

### IP Addressing Plan

| Device | Interface | IP Address | Subnet Mask | Gateway |
|---|---|---|---|---|
| PC1 | NIC | 192.168.10.10 | 255.255.255.0 | 192.168.10.1 |
| PC2 | NIC | 192.168.10.11 | 255.255.255.0 | 192.168.10.1 |
| R1 | G0/0.10 | 192.168.10.1 | 255.255.255.0 | N/A |
| R1 | G0/0.20 | 192.168.20.1 | 255.255.255.0 | N/A |
| R1 | G0/1 | 10.0.0.1 | 255.255.255.252 | N/A |
| R2 | G0/0 | 10.0.0.2 | 255.255.255.252 | N/A |
| R2 | G0/1 | 192.168.30.1 | 255.255.255.0 | N/A |
| PC3 | NIC | 192.168.30.10 | 255.255.255.0 | 192.168.30.1 |

**Note:** VLAN 10 uses the 192.168.10.0/24 subnet, VLAN 20 uses 192.168.20.0/24, and the R1–R2 point-to-point link uses 10.0.0.0/30.

### Linux Monitoring Environment

Zabbix Server and Agent 2 are deployed on Ubuntu Server running in VMware.

Monitoring activities:
- Linux host availability
- CPU, memory, and disk metrics
- Problem detection and status verification
- Email alert configuration and testing

**Scope:** Zabbix monitors the Ubuntu Server. Direct SNMP monitoring of Cisco Packet Tracer devices has not been established.

## 4. Implementation

1. Designed and configured the Cisco network topology in Packet Tracer.
2. Implemented VLANs, inter-VLAN routing, and static routes.
3. Installed Ubuntu Server in VMware.
4. Deployed Zabbix Server, Zabbix Agent 2, MySQL, and Apache.
5. Verified host monitoring data in the Zabbix web interface.
6. Configured Gmail SMTP and tested email alert delivery.
7. Practiced network troubleshooting and documented lab configurations.

## 5. Evidence and Documentation

| File / Folder | Description |
|---|---|
| `topology/` | Packet Tracer network topology file |
| `configs/` | Cisco device configurations |
| `screenshots/` | Network, monitoring, and alerting screenshots |

## 6. Skills Demonstrated

- Network configuration and connectivity troubleshooting
- VLAN and routing fundamentals
- Linux server administration
- Zabbix monitoring and alert configuration
- Email notification testing
- Basic incident documentation

## 7. Limitations

This is a personal learning project in a simulated and virtualized environment.

- Cisco network devices are simulated in Packet Tracer.
- Zabbix monitoring is configured for Ubuntu Server.
- Direct SNMP integration with Packet Tracer routers has not been verified.
- The lab is not a production monitoring environment.
