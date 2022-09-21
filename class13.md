Reading Notes <br>
Class 13<br>
Re: Port Scanning<br><br><br><br>

*The purpose of this document is to facilitate my learning of various networking security topics.  It is created for my personal use, and is a summary, including paraphrasing and direct quotes, of information found in the article(s) linked within.*<br><br>

## What is a Port Scanner and How Does it Work?
https://www.varonis.com/blog/port-scanning-techniques <br><br><br>

Attackers use port scanners to check port states but they do so to find out information about your access points, network, and devices on the network.  Examples include: 
- firewalls
- proxy servers
- VPN servers<br><br>
### Port Scanner operation: 
Sends a request packet of network data to connec to a specific TCP or UDP port on a computer to check its status; records the response. 
	- ex.:  check port 80 for web server status<br><br>  
### What is a Port?
- a virtual location point for network communication
- 131,082 network ports on each computer 
	- Two kinds of ports:  TCP, UDP
	- Port states: open, closed, or filtered.  
	- Port scanners checks port states and diagnoses network and connectivity issues. <br><br>
### Port Scanning Techniques
- ping scanner:  an ICMP echo request
	- administrators usually disable ICMP on the firewall or router for external traffice, while leaving it open in the internal network.  
- TCP half open (aka SYN scan)
	- doesn't complete the TCP 3-way-handshake, leaving the target hanging; doesn't alert network admins
	- a response indicates an active computer on the other end
	- are the NMAP default scan
- TCP Connect
	- same as TCP half-open scan but the port scanner completes the TCP connection.  
	- less privileges required to run than tcp half-open
- UDP
	- mostly used for DNS requests on port 53<br><br>
### Difference Between TCP and UDP 
- TCP:  orderly; includes error checking, verification, 3 way handshake for confirmation of successful connection<br><br>
- UDP:  faster; no error checking; connectionless protocol = programs just send the data, and if you miss a packet, it's gone for good.<br><br>
### Stealth Scanning
TCP flags: 
- FIN flag 
- X-MAS scan = sends packet with FIN, URG, and PUSH flags
	- all it does is make the packet look like a christmas tree
- no flag = NULL packet<br><br>
### Other Scanning Techniques
- TCP ACK scan:  to map firewall rulesets
- TCP Window scan:  differentiates open ports from closed ports, but works on few systems
- --scanflags:  advanced; sends custom TCP flags in a scan; can be done in NMAP<br><br>
### Port Scanning Tools
Nmap<br>
https://nmap.org/<br><br>
Solarwinds Port Scanner<br>
https://www.solarwinds.com/free-tools/port-scanner<br><br>
Netcat<br>
http://netcat.sourceforge.net/<br><br>
Advanced Port Scanner<br>
https://www.advanced-port-scanner.com/<br><br>
NetScan Tools<br>
https://www.netscantools.com/ <br><br>

### How to Detect a Port Scan?
- Port scan detector software 
	- http://sourceforge.net/projects/sentrytools/
	- http://www.openwall.com/scanlogd/
	- https://www.varonis.com/blog/netcat-commands/?hsLang=en
	- https://www.varonis.com/blog/ids-vs-ips/?hsLang=en <br><br>
### Why run port scans?
- to proactively detect and close all possible vulnerabilities
	- verify all open ports are being used correctly, and are secure
- Implications of running a port scan
	- can be considered an aggressive action; especially on a shared network
- https://www.varonis.com/products/data-security-platform/?hsLang=en <br><br><br><br>




