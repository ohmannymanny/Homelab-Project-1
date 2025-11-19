# Linux Command Reference

A personal reference of essential Linux and offensive security commands.

---

## 🔹 Networking / Recon
- `ip a` — show interfaces
- `ip route` — show routing table
- `ping <IP>` — test connectivity
- `ss -tulwn` — list open ports
- `netstat -tulnp` — service listener list

---

## 🔹 Enumeration Tools
- `nmap -sV <target>`
- `nmap -p- --stats-every 10s <target>`
- `nc -nv <target> <port>` — basic TCP connection
- `smbclient` — SMB enumeration

---

## 🔹 System Information
- `uname -a`
- `cat /etc/os-release`
- `df -h`
- `top` / `htop`

---

## 🔹 Permissions / Privilege Escalation
- `sudo -l` — list allowed sudo commands
- `find / -perm -4000 -type f 2>/dev/null` — SUID binaries
- `getcap -r /` — capabilities

---

## 🔹 File Operations
- `ls -la`
- `cp`, `mv`, `rm -rf`
- `scp <file> user@host:/path`

I will expand this list as I learn more.
