# Enterprise Network Design & Security

A multi-router, multi-subnet enterprise network designed and secured end-to-end in **Cisco Packet Tracer**. Built as the capstone for the **NTI Network Security** program (120 hours, scored 92%).

The goal was to take a full network from an addressing plan all the way to a hardened, defended configuration.

## Addressing

A single `192.168.1.0` block is carved into the departments using **VLSM**, with dedicated `/30` links between routers (R1, R3, R5, R7, R8).

## Security controls implemented

| Area | What was done |
|---|---|
| **Device hardening** | `enable secret`, encrypted passwords, **SSH instead of Telnet** |
| **AAA — local** | Local username/password authentication on access devices |
| **AAA — server-based** | **TACACS+** (Router-Blue) and **RADIUS** (Router-Green) |
| **Access control** | Named ACL (`TEST_Rules`) restricting SSH, plus a numbered ACL (130) |
| **Routing security** | **OSPF MD5** authentication between routers |
| **Layer 2** | **Port security** on access switches |
| **Remote access** | Site VPN router configuration |

## Files

- `*.pkz` — the full topology, open in Cisco Packet Tracer
- `security report.pdf` — the security configuration report (control-by-control)

NTI Network Security capstone · Group project.
