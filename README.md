# Small Manufacturing Network Resilience

## About This Project
This is an independent research project focused on developing and evaluating cost-effective network segmentation and cybersecurity resilience approaches for small U.S. manufacturing businesses.

## Research Objective
To investigate how small manufacturing businesses can use practical network segmentation, risk assessment, and repeatable implementation methods to improve network security.

## What This Project Will Include
- Cisco Packet Tracer network simulations
- Baseline and segmented network designs
- VLAN and access-control experiments
- Cybersecurity risk assessment checklists
- NIST-aligned research and technical documentation
- Educational videos explaining the labs and findings
- A technical research report

## Research Methodology
1. Review relevant NIST and CISA guidance.
2. Build a simulated baseline manufacturing business network.
3. Design and test network segmentation approaches.
4. Record configuration details and experimental results.
5. Evaluate limitations, implementation considerations, and potential costs.
6. Seek independent technical feedback and improve the framework.

## Current Project Status
Phase 1: Research setup and initial Cisco Packet Tracer labs.

## Important Note
This is an independent educational and research project. Initial experiments use simulated networks and do not represent real-world industrial deployments or verified cybersecurity outcomes.

## Author
Farheen Arif Ahmed

## References
- NIST CSWP 28: Security Segmentation in a Small Manufacturing Environment — https://csrc.nist.gov/pubs/cswp/28/security-segmentation-in-a-small-manufacturing-env/final
- NIST Cybersecurity Framework — https://www.nist.gov/cyberframework
## Educational Video Tutorials

### Lab 01 — Basic Manufacturing Network

[Watch Lab 01 on YouTube](https://youtu.be/Bq2QFVUuMB4)

This introductory Cisco Packet Tracer lab demonstrates a flat network with three PCs connected to a Cisco 2960 switch, IPv4 configuration, and connectivity testing using ping commands.

All testing was performed in a simulated environment.

### Lab 02 — VLAN Segmentation in a Manufacturing Network

**Status:** Completed — November 2026

**Video Tutorial:** [Watch Lab 02 on YouTube](https://youtu.be/146XljrteNk)

**Objective:**
Demonstrate logical network segmentation using VLANs in a simulated small manufacturing environment.

**Simulation Environment:**
- Tool: Cisco Packet Tracer
- Switch: Cisco 2960
- End devices: Three PCs
- Routing: No inter-VLAN router configured

**Network Configuration:**

| Department | VLAN | Switch Port | IP Address |
|---|---|---|---|
| Office | 10 | Fa0/1 | 192.168.10.10 |
| Admin | 20 | Fa0/3 | 192.168.20.20 |
| Production | 30 | Fa0/2 | 192.168.30.30 |

**Configuration Commands:**
```text
enable
configure terminal

vlan 10
name OFFICE
exit

vlan 20
name ADMIN
exit

vlan 30
name PRODUCTION
exit

interface fastEthernet 0/1
switchport mode access
switchport access vlan 10
exit

interface fastEthernet 0/3
switchport mode access
switchport access vlan 20
exit

interface fastEthernet 0/2
switchport mode access
switchport access vlan 30
exit

end
show vlan brief
```

**Verified Results:**
- VLAN 10 (OFFICE) assigned to Fa0/1.
- VLAN 20 (ADMIN) assigned to Fa0/3.
- VLAN 30 (PRODUCTION) assigned to Fa0/2.
- All three VLANs displayed as active in `show vlan brief`.

**Limitations:**
This lab uses a simulated network without inter-VLAN routing. VLAN membership was verified using switch configuration output. Cross-network ping failures alone do not establish comprehensive network security.

**Next Lab:**
Lab 03 — Controlled Inter-VLAN Access Using ACLs.
