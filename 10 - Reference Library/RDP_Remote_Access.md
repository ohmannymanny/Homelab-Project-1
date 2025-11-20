# RDP Remote Access (xfreerdp3)

## Install FreeRDP 3
sudo apt update
sudo apt install freerdp3-x11 -y

## Connect to a Remote Windows Machine
xfreerdp3 /v:<IP>

## Optional Flags
/u:<username>
/p:<password>
/cert:ignore        # ignore certificate warnings in lab
/size:1920x1080     # window size


## RDP Enumeration
sudo nmap -p3389 --script rdp-enum-encryption <IP>
sudo nmap -p3389 --script rdp-ntlm-info <IP>
(Also seen in [[#Nmap_Internal_Enum]])

