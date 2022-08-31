Class 02
Reading Notes
Re Domain Controller



## What is a Windows Domain and How Does It Affect My PC?
https://www.howtogeek.com/194069/what-is-a-windows-domain-and-how-does-it-affect-my-pc/

### What is a Domain?

Windows domains are used on large networks, usually corporate. 
- settings and user accounts are controlled by the domain controller. 
	- domain controllers are made up of one or more servers
		- provide network admins ability to manage large number of pc's on the same network, or remotely via VPN from one place.  
		- group policy settings, implementation.

- local user accounts are not used on the pc's.
- domain login usable on any machine on domain. 

- How to check if computer part of a domain:
	- control panel, system, security, system
		computer name, domain, workgroup settings
		if word "domain" is followed by a domain name, yes. 
		if "workgroup" followed by name, pc is part of workgroup, not domain. 

### Workgroups 
- if pc not part of a domain = part of workgroup
- refers to computers on same local network
- no computer has control over any other in group.

### Joining or Leaving a Domain
- need permission from administrator, or be the local admin. 
- Settings, sys info, sys properties
	- can do so here if part of domain and have access to change this
- Can reinstall windows if part of old domain no longer applicable. 


## Top 10 Dangerous DNS Attacks Types and The Prevention Measures
https://cybersecuritynews.com/dns-attacks/

- Domain Name System, always under attack
	- uses UDP, sometimes TCP

Famous DNS Attack Types:
- DNS Cache Poisoning Attack
- Distributed Reflection Denial of Service (DRDoS)
- DNS Hijacking
- Phantom Domain Attack
- TCP SYN Floods
- Random Subdomain Attack
- DNS Tunneling
- DNS Flood Attack
- Domain Hijacking
- Botnet-based Attacks


## Overview of DNS – N10-008 CompTIA Network+ : 1.6
https://www.professormesser.com/network-plus/n10-008/n10-008-video/an-overview-of-dns-n10-008/



## DNS Record Types
https://www.professormesser.com/network-plus/n10-008/n10-008-video/dns-record-types-n10-008/
