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
- 5060/TCP - SIP (filtered)
Likely to be smart home device or mobile application with SIP capabilities.


3.  192.168.0.102
   MAC Address - B0:68:E6:EB:1F:64 (Chongqing Fugui Electronics)
   Latency - 0.018s
Open Ports:
- 9080/TCP - tcpwrapped
Unknown device, likely to be IoT device.

4.  192.168.0.109
   MAC Address - Not shown **(Scanned from this host)**
   Latency - 0.00084s
   OS - Microsoft Windows
   CPE - cpe:/o:microsoft:windows
Open Ports:
- 135/TCP - MSRPC (Microsoft Windows RPC)
- 139/TCP - NetBIOS-SSN (Microsoft Windows netbios-ssn)
- 445/TCP - Microsoft-DS (SMB file sharing)
This is the scanning host running windows.

5.  192.168.0.107 (unknown device)
   MAC Address - 6A:3B:77:32:B2:BC (unknown)
   Latency - 0.012s
All 1000 scanned ports are in ignored states.
Device is up but is not responding to standard port probes, possibly has firewall enabled.

# Summary
Total ports scanned - 256
Active hosts found - 5
Closed ports - 996-1000 per host

# Key Findings
- Router Security: The TP-Link router (192.168.0.1) has Telnet enabled, which poses a security risk as it transmits credentials in plaintext
- Windows Host: Standard Windows networking services are exposed on 192.168.0.109
- IoT Devices: Multiple consumer IoT devices detected (Xiaomi, Chongqing Fugui Electronics)
- Network Segmentation: All devices are on a single /24 subnet
