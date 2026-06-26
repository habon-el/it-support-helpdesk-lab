# it-support-helpdesk-lab
# 🖥️ IT Support & Helpdesk Skills Lab

![Status](https://img.shields.io/badge/Status-In%20Progress-orange)
![ITSM](https://img.shields.io/badge/ITSM-osTicket-blue)
![OS](https://img.shields.io/badge/OS-Linux%20%7C%20macOS%20%7C%20Windows-lightgrey)
![Network](https://img.shields.io/badge/Network-TCP%2FIP%20%7C%20VPN%20%7C%20DNS-green)
![Framework](https://img.shields.io/badge/Framework-ITIL%20v4-purple)

## Overview

A hands-on IT Support and Helpdesk lab simulating a real Level 2 IT Support environment. Built to develop and demonstrate practical skills for enterprise IT support roles, including ticket management, multi-OS support, network troubleshooting, VPN administration, and ITIL incident management.

**Target Role:** Level 2 IT Support Analyst  
**Environment:** Kali Linux + Docker + Azure  
**Author:** Axcel Habon

---

## Lab Architecture

```
┌─────────────────────────────────────────────────────┐
│                   IT Support Lab                     │
│                                                     │
│  ┌─────────────┐    ┌─────────────┐                │
│  │   osTicket   │    │    MySQL    │                │
│  │  (Port 8080) │◄──►│  Database  │                │
│  │   ITSM Tool  │    │  (Docker)  │                │
│  └─────────────┘    └─────────────┘                │
│                                                     │
│  ┌─────────────┐    ┌─────────────┐                │
│  │  OpenVPN    │    │  Wireshark  │                │
│  │  (Azure VM) │    │  TCP/IP Lab │                │
│  └─────────────┘    └─────────────┘                │
│                                                     │
│  ┌─────────────┐    ┌─────────────┐                │
│  │  macOS VM   │    │    ITIL     │                │
│  │  Support Lab│    │  Procedures │                │
│  └─────────────┘    └─────────────┘                │
└─────────────────────────────────────────────────────┘
```

---

## Skills Demonstrated

| Skill | Tool | Status |
|-------|------|--------|
| ITSM Ticket Management | osTicket | ✅ Complete |
| SLA Policy Configuration | osTicket Admin Panel | ✅ Complete |
| Department & Agent Setup | osTicket | ✅ Complete |
| Ticket Lifecycle Management | osTicket | ✅ Complete |
| macOS User Management | macOS System Settings | ✅ Complete |
| macOS FileVault Encryption | macOS Security | ✅ Complete |
| TCP/IP Troubleshooting | Wireshark + CLI | ✅ Complete |
| DNS Diagnostics | nslookup, dig | ✅ Complete |
| VPN Deployment | OpenVPN on Azure | ✅ Complete |
| VPN Client Troubleshooting | OpenVPN Client | ✅ Complete |
| ITIL Incident Management | Documentation | ✅ Complete |

---

## Project Modules

### Module 1 — ITSM: osTicket Helpdesk System ✅

Deployed a full ITSM ticketing system using Docker simulating a university IT support environment.

**What I built:**
- Deployed osTicket + MySQL using Docker containers on a private network
- Configured 5 departments: Help Desk, Hardware Support, Network & Infrastructure, Software & Applications, VIP Support
- Set up SLA policies with response/resolution targets by priority (Critical → Low)
- Created and resolved 10 realistic Level 2 support tickets

**SLA Configuration:**

| Priority | Response Time | Resolution Time |
|----------|--------------|-----------------|
| Critical | 15 minutes | 2 hours |
| High | 1 hour | 4 hours |
| Medium | 4 hours | 1 business day |
| Low | 8 hours | 3 business days |

**Sample Tickets Resolved:**

| Ticket # | Issue | Priority | Resolution |
|----------|-------|----------|------------|
| TKT-001 | Professor cannot connect to VPN | High | Reset credentials, updated VPN client |
| TKT-002 | MacBook not connecting to campus WiFi | Medium | Cleared network profile, re-enrolled |
| TKT-003 | Outlook not syncing emails | Medium | Cleared cache, re-added Exchange account |
| TKT-004 | Dean laptop screen flickering | High | VIP escalation — loan device provided |
| TKT-005 | New staff member laptop setup | Low | Imaged machine, installed COE software |
| TKT-006 | Student cannot access shared drive | Medium | Fixed AD group membership |
| TKT-007 | Printer offline in faculty lounge | Low | Restarted spooler, reinstalled driver |
| TKT-008 | Zoom not working during lecture | Critical | On-site support — switched to backup AV |
| TKT-009 | iPhone not syncing university calendar | Low | Configured Exchange ActiveSync on iOS |
| TKT-010 | Suspicious phishing email received | High | Isolated, reported to security team |

---

### Module 2 — macOS Support Lab 🔄

Hands-on macOS support tasks simulating common Level 2 issues in a university environment.

**Tasks Practiced:**
- User account creation and management
- FileVault full-disk encryption setup
- Exchange email account configuration
- Remote Management enabling for IT support
- Disk Utility First Aid for disk errors
- macOS Terminal diagnostic commands

---

### Module 3 — TCP/IP Troubleshooting Lab 🔄

Network diagnostic lab using Wireshark and CLI tools to diagnose and resolve connectivity issues.

**Tools Used:** Wireshark, ping, traceroute, nslookup, netstat, ipconfig/ifconfig

**Scenarios Diagnosed:**
1. User reports "internet is down" → traced with ping + traceroute
2. Websites load but email does not → DNS/MX record investigation
3. Connected to WiFi but no internet → DHCP failure (169.x.x.x address)
4. Specific website unreachable → bypass DNS, check proxy
5. Slow network performance → Wireshark retransmission analysis

---

### Module 4 — VPN Setup & Troubleshooting 🔄

Deployed and tested a real OpenVPN server on Azure to simulate enterprise VPN support.

**What I built:**
- Deployed OpenVPN server on Azure JumpBox VM
- Configured client .ovpn profile and connected from Kali Linux
- Tested and documented 5 common VPN failure scenarios

**VPN Troubleshooting Scenarios:**

| Problem | Cause | Fix |
|---------|-------|-----|
| Cannot connect at all | Firewall blocking UDP 1194 | Opened NSG inbound rule |
| Connects but no internet | Routing misconfiguration | Fixed redirect-gateway setting |
| Frequent disconnections | Keepalive timeout | Adjusted keepalive parameters |
| DNS not working over VPN | Missing DNS push config | Added dhcp-option DNS to config |
| Wrong credentials error | Expired password | Reset auth credentials |

---

### Module 5 — ITIL Incident Management 🔄

Documented a complete ITIL v4 incident management procedure for a university IT department.

**ITIL Lifecycle Stages Documented:**
1. Identification → 2. Logging → 3. Categorization → 4. Prioritization → 5. Initial Diagnosis → 6. Escalation → 7. Investigation → 8. Resolution → 9. Closure → 10. Post-Incident Review

---

## Technologies Used

| Category | Technology |
|----------|------------|
| ITSM Platform | osTicket (open-source) |
| Database | MySQL 5.7 (Docker) |
| Containerization | Docker |
| Network Analysis | Wireshark |
| VPN | OpenVPN |
| Cloud | Microsoft Azure |
| OS Environments | Kali Linux, macOS, Windows |
| Framework | ITIL v4 |

---

## Key Takeaways

- Deployed and configured a production-grade ITSM ticketing system from scratch
- Practiced real Level 2 support scenarios across hardware, software, and network categories
- Applied ITIL incident management methodology to ticket handling
- Gained hands-on experience with multi-OS support (Linux, macOS, Windows)
- Built and troubleshot a real VPN infrastructure on Azure

---

## Related Projects

- [Azure Cloud Cybersecurity Lab](https://github.com/habon-el/azure-cloud-cybersecurity-lab) — ELK Stack SIEM, Microsoft Sentinel, attack simulation, and SOC incident response

---

## Author

**Axcel Habon**  
SOC Analyst | Cloud Security | IT Support  
📍 Canada  
🎯 Preparing for CySA+ (July 29, 2026)  
🔗 [GitHub](https://github.com/habon-el)
