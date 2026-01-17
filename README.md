# OIBSIP
Basic network scanning using Nmap
This document details  network reconnaissance performed on the local network segment 192.168.0.0/24 using Nmap 7.98.
# Tool used:
Nmap 7.98
# Target:
192.168.0.0/24
# Hosts Discovered
1.  192.168.0.1
   MAC Address - D8:47:32:92:4B:08 (TP-Link Technologies)
   Latency - 0.0081s
   OS - Linux (kernel 3.10.14)
   Device Type - Broadband Router, WAP, CPE
Open Ports:
- 23/TCP - Telnet (BusyBox telnetd 1.14.0 or later)
- 53/TCP - DNS (tcpwrapped)
- 80/TCP - HTTP (TP-LINK WAP http config)
- 1900/TCP - UPnP (Portable SDK for UPnP devices 1.6.19)
  
Telnet is an unencrypted remote management service, and exposing multiple management interfaces increases the attack surface, leading to higher security risk.

2.  192.168.0.101
   MAC Address - 9C:28:F7:3A:76:EE (Xiaomi Communications)
   Latency - 0.0085s
Open Ports:
- 5060/TCP - 
