## **Phase 1B — Internal Network Discovery, Enumeration, and Remote Access**

**Objective:**  
Simulate an attacker inside an internal corporate network (example: hospital, LAN) and learn how hosts are discovered, enumerated, and accessed using Kali Linux.

This phase covers the offensive side of internal network security — the same techniques used by penetration testers and real-world attackers, but safely isolated inside my homelab.

## **Summary of Phase 1B Learning Objectives Achieved**

###  Internal host discovery

###  ARP-based local scanning

###  Service enumeration with Nmap

###  RDP version and cipher enumeration

###  NTLM/NetBIOS data gathering

###  Successful remote access into Windows 11 via RDP

###  Mapping offensive techniques to real-world enterprise behavior

## **Verify Internal Network Connectivity**

**Goal:**  
Confirm that Kali and Windows 11 are on the same VirtualBox Host-Only network.

ip a              # Find Kali’s IP (eth1 →1192.168.X.X)
ipconfig          # Find Windows IP (→1192.168.X.Y)
ping 192.168.X.Y
Result:**  
Kali and Win11 VM can communicate — LAN is working.
## **Internal Host Discovery (arp-scan)**

**Goal:**  
Detect active hosts inside the VirtualBox LAN.

sudo arp-scan --interface=eth1 192.168.56.0/24

**What it shows:**

- List of active devices
    
- Their IPs
    
- Their MAC addresses
    
- Identifies unknown or unmanaged devices (red-team behavior)

## **Enumerating Open Ports with Nmap**

**Goal:**  
Identify exposed services and services running on Windows 11.

sudo nmap -sV 192.168.X.Y

**Findings:**

- Port **3389/tcp (RDP)** open
    
- Windows version info leaked
    
- NetBIOS / NTLM computer name
    
- Remote Desktop protocols & ciphers
    

**Real-World Mapping:**  
This mirrors internal enumeration during an Active Directory breach or lateral movement attempt.

## **RDP-Specific Enumeration**

### Check RDP Encryption:
sudo nmap -p3389 --script rdp-enum-encryption 192.168.X.Y

Findings:

- CredSSP supported
    
- Standard RDP encryption supported
    
- Host security layer identified

### Check NTLM & NetBIOS:

`sudo nmap -p3389 --script rdp-ntlm-info 192.168.X.Y`

Findings:

- NTLM domain name
    
- Computer name
    
- OS version
    
- Product build


## **Establish Remote GUI Access via RDP (xfreerdp3)**

Installed:

`sudo apt install freerdp3-x11`

Connected:

`xfreerdp3 /v:192.168.X.Y`

Results:

- Certificate warning (normal in a lab)
    
- Successfully authenticated
    
- **Full GUI Windows 11 session inside Kali**
    

**This completes the attacker foothold simulation.**

**Real-World Meaning:**  
This simulates gaining remote
![[Pasted image 20251119195523.png]]