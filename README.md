# Cybersecurity Master Homelab  
Documenting my hands-on journey from **Help Desk → SysAdmin → Cybersecurity Analyst → Security Engineer → Cloud Security**.

This repository contains my structured notes, research, walkthroughs, configurations, and documentation for building a full **enterprise-style cybersecurity homelab**. Everything here is designed to build real, practical skill—not just theory.

---

##  Current Lab Status
**Phase 1A–1C completed:**
- VirtualBox hypervisor installed and configured
- Windows 11 VM fully set up
- Kali Linux VM fully set up
- Internal network configured (Host-Only, NAT)
- Confirmed host-to-host communication
- Remote Desktop (RDP) enabled and accessible from Kali
- Secure Obsidian → GitHub documentation pipeline built

---

##  Purpose of This Homelab
This environment simulates an enterprise-level internal network so I can:
- Learn and practice blue team & red team concepts
- Build and break Windows environments safely
- Perform secure remote administration and monitoring
- Run vulnerability scans and harden systems
- Build SIEM pipelines (Wazuh, Splunk, ELK)
- Deploy honeypots and detect attacks
- Practice malware analysis in isolated VMs
- Document all work using Git-driven version control

This is the same workflow that cybersecurity analysts, sysadmins, and penetration testers use in real organizations.

---

##  Homelab Architecture (Current and Planned)

### ** Current Environment**
| Component | Details |
|----------|---------|
| **Hypervisor** | Oracle VirtualBox |
| **Host System** | Lenovo Legion Pro 7 |
| **VM #1** | Windows 11 (Evaluation) |
| **VM #2** | Kali Linux (Offensive Security) |
| **Networking** | Host-Only + NAT |
| **Remote Access** | RDP enabled, tested via xfreerdp |
| **Documentation System** | Obsidian + Git + GitHub |

### ** Short-Term Additions (Next Phases)**
- Active Directory domain controller (Windows Server)
- Additional Windows clients joined to AD
- Vulnerability scanning (Nessus Essentials)
- Wazuh SIEM server
- Basic honeypot (Cowrie or OpenCanary)
- Internal DNS and DHCP configuration
- Firewall and routing segmentation

### ** Long-Term Additions**
- ELK stack logging
- Sysmon + Sigma + OpenHunting rules
- Purple team attack simulations
- SOC-style detection engineering
- Cloud security lab (AWS or Azure)
- Malware analysis VM (FlareVM or REMnux)
- Custom CTF challenges hosted in the lab

---

##  Repository Structure
This repo mirrors my Obsidian vault.

