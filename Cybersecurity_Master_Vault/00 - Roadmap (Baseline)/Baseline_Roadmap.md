# Baseline Cybersecurity Roadmap

This roadmap represents my long-term progression:

**Help Desk → Systems Admin / Network Admin → Cybersecurity Analyst → Security Engineer → Cloud Security (Blue + Red hybrid)**

##  CURRENT PHASE: Phase 1 – Homelab Foundations
- Set up virtualization environment (VirtualBox)
- Create Windows 11 Victim VM
- Create Kali Linux Attacker VM
- Configure networking (Host-Only + NAT)
- Verify connectivity between VMs
- Begin documenting everything inside Obsidian

##  UPCOMING PHASES
### **Phase 2 – Basic Offensive Skills**
- Nmap fundamentals & port scanning
- Service enumeration (SMB, RDP, SSH)
- Begin attacking your Windows VM (credential guessing, misconfig testing)

### **Phase 3 – Defensive Engineering (Blue Team)**
- Build a full SIEM (Wazuh or Elastic)
- Send Windows logs → SIEM
- Detect threats you create from Kali

### **Phase 4 – Active Directory (Enterprise Simulation)**
- Build a multi-machine AD domain
- Users, Groups, GPOs, DNS, DHCP
- Attack your own AD environment

### **Phase 5 – Detection Engineering**
- Write alert rules, Sigma rules
- Track your own attacks in the SIEM

### **Phase 6 – Red Team Development**
- Payload development
- Privilege escalation
- Lateral movement
- Pivoting into other VM networks

### **Phase 7 – Cloud Security & Automation**
- Azure AD + Defender
- AWS detection techniques
- Terraform automation
