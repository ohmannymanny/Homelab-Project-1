# Homelab  

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

## Current Lab Status

**Phase 1A–1B completed:**

- VirtualBox hypervisor installed and configured on a Lenovo Legion Pro 7
- Windows 11 VM fully set up (evaluation image)
- Kali Linux VM fully set up (latest Kali rolling image)
- Internal VirtualBox network configured (Host-Only, plus NAT for Kali)
- Confirmed host-to-host communication between Kali and Windows over the Host-Only network
- Windows firewall inbound rule added to allow ICMPv4 (ping) from Kali
- Remote Desktop (RDP) enabled on the Windows 11 VM and successfully accessed from Kali using `xfreerdp3`
- Secure Obsidian → Git → GitHub documentation pipeline set up and tested

**Phase 1C status:**

- Phase 1C (baseline hardening and tooling) has been defined and partially started, but is not yet complete.
- Planned/early work in Phase 1C:
  - Windows 11 baseline configuration and tooling
  - Kali Linux tooling and shell customization
  - Clean “baseline” snapshots after configuration


---

## Purpose of This Homelab

This environment simulates a small enterprise-style internal network so I can:

- Learn and practice blue team and red team concepts
- Build and safely break Windows and Linux environments
- Perform secure remote administration and monitoring
- Run basic vulnerability scans and harden systems
- Eventually build SIEM pipelines (Wazuh, Splunk, ELK) inside the lab
- Deploy honeypots and detect attacks in a controlled environment
- Practice malware analysis inside isolated VMs
- Document all work using Git-driven version control (Obsidian + GitHub)

Anything listed as SIEM, honeypot, malware analysis, or cloud is **planned work**, not yet built, unless explicitly marked as completed.


---

## Homelab Architecture (Current and Planned)


### Current Environment

| Component           | Details                                   |
|--------------------|-------------------------------------------|
| **Hypervisor**     | Oracle VirtualBox                         |
| **Host System**    | Lenovo Legion Pro 7 (Windows 11)          |
| **VM #1**          | Windows 11 (Evaluation)                   |
| **VM #2**          | Kali Linux (Offensive Security)           |
| **Networking**     | VirtualBox Host-Only network + NAT (for Kali) |
| **Host-Only LAN**  | 192.168.56.0/24 (Kali and Windows are peers) |
| **Remote Access**  | RDP enabled on Windows, tested from Kali using `xfreerdp3` |
| **Documentation**  | Obsidian vault synced to GitHub via Git   |

Current known addressing in the lab:

- Kali Linux VM: `192.168.X.X/24` (Host-Only interface)
- Windows 11 VM: `192.168.X.Y/24` (Host-Only interface)

Kali has internet connectivity via a NAT adapter. The Windows VM currently uses Host-Only networking for lab purposes; internet access on that VM has not been configured yet.


### Short-Term Additions (Next Phases)

These items are **planned** and have not yet been implemented:

- Active Directory domain controller (Windows Server)
- One or more Windows clients joined to the domain
- Vulnerability scanning (e.g., Nessus Essentials)
- Wazuh or similar SIEM server
- Basic honeypot (Cowrie, OpenCanary, or similar)
- Internal DNS and DHCP configuration for the lab network
- Firewall and basic network segmentation


### Long-Term Additions

These are longer-range goals and are not yet implemented:

- Centralized logging with an ELK stack
- Sysmon + Sigma + hunting rules for Windows telemetry
- Purple team attack simulations and detection tuning
- SOC-style detection engineering workflows
- Cloud security lab (AWS or Azure) integrated with/on top of this environment
- Dedicated malware analysis VM (FlareVM or REMnux)
- Custom CTF-style challenges hosted inside the lab


---

## Kali Linux Configuration (Current)

Kali is used as the primary offensive and admin workstation in this homelab.

Current state:

- Kali is updated to the latest rolling release.
- Core tools installed and verified:
  - `nmap`
  - `net-tools`
  - `curl`
  - `wget`
  - `git`
  - `htop`
  - `seclists` (for wordlists and discovery)
  - `xfreerdp3` (for RDP into the Windows 11 VM)
- Shell customization:
  - `zsh` and `oh-my-zsh` installed
  - Syntax highlighting and autosuggestion plugins configured
  - Prompt updated to improve readability when running commands and reading output
- Connectivity:
  - Kali can successfully:
    - Ping the Windows VM
    - Discover the Windows VM over the Host-Only network
    - RDP into Windows using `xfreerdp3 /v:192.168.X.Y`


---

## Windows 11 Configuration (Current)

Windows 11 is currently acting as a standalone workstation in the lab.

Current state:

- Installed as a VirtualBox VM using a Windows 11 evaluation ISO.
- VirtualBox Guest Additions installed for better integration.
- Connected to the Host-Only network:
  - IP: `192.168.X.Y/24`
- Windows Defender Firewall enabled.
- Inbound ICMPv4 allowed (to permit ping from Kali) via a specific inbound rule.
- Remote Desktop enabled and tested:
  - RDP connections from Kali using `xfreerdp3` have been confirmed working.
- Internet access for this VM is not configured yet; traffic is currently scoped to the VirtualBox lab network.

Phase 1C will add more baseline tooling and hardening (Sysinternals, useful utilities, and any other tools documented as they are actually installed).


---

## Documentation and Version Control Workflow

The homelab documentation is maintained as an Obsidian vault on the host system and is version-controlled using Git and GitHub.

Current documentation pipeline:

- Obsidian vault path (local, on the host):  
  `C:\Obsidian Vaults\Cybersecurity_Master_Vault`
- Git is initialized inside the vault folder.
- Obsidian Git community plugin is installed and configured to:
  - Detect changes to notes
  - Stage, commit, and push changes to GitHub
- GitHub repository:
  - `https://github.com/ohmannymanny/Homelab-Project-1`
- The repository uses separate branches to distinguish:
  - A high-level overview branch for clean, recruiter-friendly documentation
  - A detailed vault branch containing the full Obsidian structure and notes

Only notes and files that exist in the Obsidian vault and have been committed are pushed to GitHub. VM-specific changes (inside Windows or Kali) are separate from the Git history unless explicitly documented.


---

## Repository Structure

This repository mirrors the structure of the Obsidian vault that backs this homelab.

Top-level folders (subject to expansion as the lab grows):

- `00 - Roadmap (Baseline)`  
  High-level learning and lab roadmap, phases, and long-term plans.

- `01 - Homelab Setup`  
  Notes for VirtualBox installation, VM creation, networking choices, and base snapshots.

- `02 - Phase Documentation`  
  Detailed write-ups of each phase:
  - Phase 1A: VirtualBox + VM install
  - Phase 1B: Networking, ping, basic nmap, and RDP from Kali to Windows
  - Phase 1C: Baseline hardening and tooling (in progress)
  Future phases (AD, SIEM, honeypots, etc.) will be documented here once they are actually built.

- `03 - Templates`  
  Reusable templates for investigations, scans, lab write-ups, and repeatable workflows.

- `04 - Offensive Security`  
  Commands, methodologies, and notes related to offensive testing performed inside the lab.

- `05 - Defensive Security`  
  Hardening checklists, log analysis workflows, and blue team notes as they are implemented.

- `06 - SOC & SIEM`  
  Will contain SIEM and SOC-style documentation once those components are deployed.

- `07 - Advanced Blue Team`  
  Advanced detection, threat hunting, and analysis notes (future use as capabilities grow).

- `08 - Cloud Security`  
  Planned area for AWS/Azure security labs that integrate with or extend this homelab.

- `09 - Daily Logs`  
  Day-by-day notes of work done in the lab, troubleshooting steps, and learning reflections.

- `10 - Reference Library`  
  Cheat sheets, protocol references, external links, and curated study resources.

- `11 - Tools & Cheat Sheets`  
  Quick reference for tools like `nmap`, `nc`, `gobuster`, `xfreerdp3`, and OS commands.

- `12 - Networking Notes`  
  Subnetting examples, routing concepts, DNS/DHCP notes, and network diagrams tied to the lab.

- `13 - Windows Internals`  
  Research and experiments related to Windows internals and artifacts, as they are performed.

- `14 - DFIR Notes`  
  Forensics and incident response notes (to be populated when those labs are built).

- `15 - Red Techniques`  
  Red-team and adversary emulation techniques tested within this environment.

- `16 - Scripts Library`  
  Automation and helper scripts (Bash, PowerShell, Python) used in or for this lab.

- `17 - Project Labs`  
  Self-contained lab projects (e.g., AD deployment, SIEM build, honeypot lab, CTF scenarios).


---

## Link to Public Repository

This homelab and its documentation are tracked here:

https://github.com/ohmannymanny/Homelab-Project-1

This README reflects only what has actually been implemented so far. Planned items are explicitly marked as future work and will be updated as the environment evolves.
