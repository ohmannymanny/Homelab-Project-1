## Kali Linux – Attacker VM Setup

This Kali Linux VM functions as the attacker workstation. I will use it to learn and practice offensive security techniques, including network discovery, port scanning, exploitation testing, and penetration testing workflows.

### Installation Summary

- Source: Official Kali Linux VirtualBox image
    
- Successfully imported into VirtualBox
    
- Manually installed VirtualBox Guest Additions
    
- Verified correct display behavior and mouse integration
    

### Networking Configuration

The Kali VM is configured to communicate only with other machines in the lab, not the internet (except when required for updates).

- Kali IP Address: **192.168.56.104**
    
- Subnet: 255.255.255.0 (/24)
    
- Internet access: Enabled (for updates and tool installation)
    
- Connectivity with Windows: Fully functional
    

### Tools and Features Verified

- Terminal and package manager (apt)
    
- Ping tests between Kali and Windows
    
- Nmap installation and usage
    
- Guest Additions installation confirmation
    

### Snapshots Created

- Base Kali Install
    
- Post-Network Verification
    

This VM will be used for:

- Nmap scanning
    
- Reconnaissance
    
- Password attacks (RDP, SMB)
    
- Web and network exploitation
    
- Active Directory attack simulations