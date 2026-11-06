
# Lab 02 — VLAN Segmentation

## Project
Small Manufacturing Network Resilience

**Status:** Completed — November 2026

**Video:** [Watch Lab 02 on YouTube](https://youtu.be/146XljrteNk)

## Objective
Demonstrate how VLANs can logically separate Office, Admin, and Production departments in a simulated manufacturing network.

## Lab Environment
- Simulator: Cisco Packet Tracer
- Switch: Cisco 2960
- Devices: 3 PCs
- Inter-VLAN routing: Not configured

## Network Configuration

| Department | VLAN | Switch Port | IP Address |
|---|---|---|---|
| Office | 10 | Fa0/1 | 192.168.10.10 |
| Admin | 20 | Fa0/3 | 192.168.20.20 |
| Production | 30 | Fa0/2 | 192.168.30.30 |

Subnet mask: 255.255.255.0

## Implementation
1. Created VLAN 10 (OFFICE).
2. Created VLAN 20 (ADMIN).
3. Created VLAN 30 (PRODUCTION).
4. Assigned each department to its corresponding switch port.
5. Verified assignments using `show vlan brief`.
6. Demonstrated connectivity testing in the simulated environment.

## Verified Switch Results
- VLAN 10: Fa0/1 — Active
- VLAN 20: Fa0/3 — Active
- VLAN 30: Fa0/2 — Active

## Evidence

### Published Video
[Lab 02 — VLAN Segmentation](https://youtu.be/146XljrteNk)

### Supporting Files
To be added:
- Cisco Packet Tracer project (.pkt)
- VLAN configuration screenshot
- Network topology screenshot
- Connectivity test screenshots

## Technical Limitations
This lab demonstrates VLAN membership and logical separation in a simulated environment.

No inter-VLAN router or Layer 3 routing configuration was used. Cross-subnet ping failures alone do not establish comprehensive network security.

The simulation does not demonstrate real-world industrial cybersecurity effectiveness.

## Next Experiment
Lab 03 — Controlled Inter-VLAN Access Using Access Control Lists (ACLs).
