### This is basically the juice, the notes, documentation, etc.
    again this is more for personal use, mostly for sharing the journey



### COPY of README.md###

## Current Lab Status

[](https://github.com/ohmannymanny/Homelab-Project-1#current-lab-status)

**Phase 1A–1B completed:**

- VirtualBox hypervisor installed and configured
- Windows 11 VM fully set up
- Kali Linux VM fully set up
- Internal network configured (Host-Only, NAT)
- Confirmed host-to-host communication
- Remote Desktop (RDP) enabled and accessible from Kali
- Secure Obsidian → GitHub documentation pipeline built

---

## Purpose of This Homelab

[](https://github.com/ohmannymanny/Homelab-Project-1#purpose-of-this-homelab)

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

## Homelab Architecture (Current and Planned)

[](https://github.com/ohmannymanny/Homelab-Project-1#homelab-architecture-current-and-planned)

### ** Current Environment**

[](https://github.com/ohmannymanny/Homelab-Project-1#-current-environment)

|Component|Details|
|---|---|
|**Hypervisor**|Oracle VirtualBox|
|**Host System**|Lenovo Legion Pro 7|
|**VM #1**|Windows 11 (Evaluation)|
|**VM #2**|Kali Linux (Offensive Security)|
|**Networking**|Host-Only + NAT|
|**Remote Access**|RDP enabled, tested via xfreerdp|
|**Documentation System**|Obsidian + Git + GitHub|

### ** Short-Term Additions (Next Phases)**

[](https://github.com/ohmannymanny/Homelab-Project-1#-short-term-additions-next-phases)

- Active Directory domain controller (Windows Server)
- Additional Windows clients joined to AD
- Vulnerability scanning (Nessus Essentials)
- Wazuh SIEM server
- Basic honeypot (Cowrie or OpenCanary)
- Internal DNS and DHCP configuration
- Firewall and routing segmentation

### ** Long-Term Additions**

[](https://github.com/ohmannymanny/Homelab-Project-1#-long-term-additions)

- ELK stack logging
- Sysmon + Sigma + OpenHunting rules
- Purple team attack simulations
- SOC-style detection engineering
- Cloud security lab (AWS or Azure)
- Malware analysis VM (FlareVM or REMnux)
- Custom CTF challenges hosted in the lab

---

## Repository Structure

[](https://github.com/ohmannymanny/Homelab-Project-1#repository-structure)

This repo mirrors my Obsidian vault.
This can be found on the public github. 

https://github.com/ohmannymanny/Homelab-Project-1
