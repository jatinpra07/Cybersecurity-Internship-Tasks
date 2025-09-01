# Task-1 Notes – Cybersecurity & Ethical Hacking Internship

## Lab Setup  
- VirtualBox installed  
- Kali Linux (Attacker) → IP: 192.168.56.5  
- Metasploitable 2 (Target) → IP: 192.168.56.4  
- Both connected using Host-Only Adapter  
- Verified connection with `ping` command  

## Wireshark  
- Captured ICMP packets (ping)  
- Command: `ping -c 4 192.168.56.4`  
- Applied filter: `icmp`  
- Saw Echo Request and Echo Reply  

## Nmap  
- Scanned Metasploitable from Kali  
- Command: `nmap -sS -sV -O 192.168.56.4`  
- `-sS` = SYN scan  
- `-sV` = service version detection  
- `-O` = OS detection  
- Found open ports, running services, OS fingerprint  

## Burp Suite  
- Proxy set to 127.0.0.1:8080 in Firefox  
- Burp intercept ON  
- Opened DVWA page  
- Intercepted login request successfully  

## Netcat  
- Listener on Metasploitable: `nc -lvp 4444`  
- Client on Kali: `nc 192.168.56.4 4444`  
- Simple chat between machines worked  

## Linux Cheat-Sheet (Basic Commands)  
- `ifconfig` → show network config  
- `ping <IP>` → test connectivity  
- `netstat -tulnp` → show listening ports  
- `ls` → list files  
- `cd` → change directory  
- `pwd` → print current directory  
- `cp` → copy files  
- `mv` → move/rename files  
- `rm` → remove files  
- `cat` → show file contents  
- `nano` → edit file  
- `chmod` → change permissions  
- `sudo` → run as root  
- `apt-get update && apt-get upgrade` → update system  
