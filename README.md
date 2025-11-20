# Cybersecurity Master Homelab  

Documenting my hands-on journey from **Help Desk → SysAdmin → Cybersecurity Analyst → Security Engineer → Cloud Security**.

This repository contains my structured notes, research, walkthroughs, configurations, and documentation for building a full **enterprise-style cybersecurity homelab**. Everything here is designed to build real, practical skill.
This is my journey/path and making it public... who knows but here to learn, explore, build, and collaborate.
First love is music, so if you are interested in checking out what I have made:
https://soundcloud.com/evencemusic
Second love is computers, always been around them, always spent way too much time on them but this time its more serious so here I am... going to be spending even more time on them cause I love it. In this repo it combines a small amount of personal relevance but mostly focused achieving milestones and goals through out the journey and building a homelab with the plan of potentially scaling up over time. 
Using Profressor Messer as a resource and learning source material,Friends, IT Discord servers, Google, AI, Books, Work Expierence. 
Recently been playing Tower Networking Inc. game on Steam. been loving it so far, would recommend.
Hackthebox: ohmannymanny (Currenly Private, however have HTB Academy, Lab Monthly subs)



---

##  Current Lab Status
**Phase 1A–1B completed:**
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

