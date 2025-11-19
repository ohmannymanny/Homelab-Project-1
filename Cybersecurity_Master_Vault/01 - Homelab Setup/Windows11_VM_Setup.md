## Windows 11 Enterprise Evaluation – VM Build Notes

This virtual machine serves as the victim workstation in my cybersecurity homelab. It represents a standard Windows 11 enterprise endpoint. I will use it to practice system enumeration, privilege escalation, service exploitation, lateral movement, detection engineering, and hardening techniques.

### Installation Summary

- Operating System: Windows 11 Enterprise Evaluation
    
- Hypervisor: VirtualBox
    
- Installation completed using the official Windows 11 ISO
    
- UEFI, Secure Boot, and TPM 2.0 enabled
    
- Local user created: **labuser**
    

### Post-Install Setup

- Installed VirtualBox Guest Additions
    
- Resolved display and scaling issues
    
- Confirmed keyboard and mouse integration
    
- Optional updates completed as needed
    

### Networking Configuration

The Windows VM is intentionally isolated using a VirtualBox Host-Only Network. This limits communication to lab machines only and prevents any external exposure.

- Windows IP Address: **192.168.56.105**
    
- Subnet: 255.255.255.0 (/24)
    
- Internet access: Disabled (intentional)
    
- Local connectivity between Windows and Kali: Fully functional
    

### Firewall Configuration

To support initial reconnaissance and scanning, ICMP Echo Request (ping) was enabled for the **Private Profile** within Windows Defender Firewall.

This configuration allows:

- Kali → Windows ping
    
- Windows → Kali ping
    

No other inbound rules were altered.

### Snapshots Created

- Base Install – clean installation of Windows 11
    
- Post-Networking Fix – after verifying ICMP and host-only network communication
    

This VM will later be used for:

- RDP exposure testing
    
- SMB enumeration
    
- Vulnerability testing
    
- Installation of Sysmon and Windows logging configurations
    
- Integration into an Active Directory environment