# INF249 – Attack Lab (MA2)

This project is a practical penetration testing assignment from  
**INF249 – Network Security (University of Bergen).**

## Scenario
The goal was to locate a hidden flag (`FLAG{...}`) on a target machine in a
simulated internal network, starting only from an entry point VM.

## What I did (high-level)
- **Network reconnaissance**
  - Used `arp-scan` to identify live hosts and determine the gateway vs. target.
  - Mapped services with `nmap -sV` (FTP, SSH, HTTP).

- **Initial access**
  - Exploited **anonymous FTP** misconfiguration to upload a PHP payload.
  - Triggered the payload via HTTP to obtain a **reverse shell** as `www-data`.

- **Post-exploitation**
  - Enumerated users via `/home`.
  - Leveraged a misconfigured **SUID binary (`/usr/bin/diff`)** to read `/etc/shadow`.
  - Cracked weak hashes offline using **John the Ripper**.

- **Privilege escalation**
  - Discovered credentials in a user script and switched to a sudo user.
  - Used recursive search to locate the hidden flag in another user’s home directory.

## Tools
- Linux CLI, nmap, netcat, FTP, HTTP
- John the Ripper (offline cracking)
- Standard enumeration and privilege escalation techniques

## Documentation
Full report: `report/INF249_MA2_attack_lab.pdf`

