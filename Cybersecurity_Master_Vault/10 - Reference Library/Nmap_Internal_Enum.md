# Nmap Internal Network Enumeration Cheat Sheet

## Host Discovery
sudo arp-scan --interface=eth1 192.168.56.0/24

## Basic Port Scan
sudo nmap <IP>

## Service Detection
sudo nmap -sV <IP>

## Script Scanning
sudo nmap -sC -sV <IP>

## RDP Enumeration
sudo nmap -p3389 --script rdp-enum-encryption <IP>
sudo nmap -p3389 --script rdp-ntlm-info <IP>

## OS Detection
sudo nmap -O <IP>

## Save Scan Output
sudo nmap -sV -oN scan_results.txt <IP>
