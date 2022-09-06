Reading Notes <br>
Class _____<br>
Re _____________<br><br><br><br>

*This document is a summary of information in the article linked within.*<br><br>

The OSI model was developed by the International Organization for Standardization (ISO). It describes the layers that computer systems use to communicate over a network and was the first standard model for network communications adopted by all major computer and telecommunication companies in the early 1980s.<br><br>

## Understanding the OSI Model – N10-008 CompTIA Network+ : 1.1 (video)
https://www.professormesser.com/network-plus/n10-008/n10-008-video/understanding-the-osi-model-3/ <br><br>

### OSI:  Systems Interconnection Reference Model
- a guide
- not same as OSI protocol suite<br><br>

**- 7 Layers:  unique protocols at every layer**<br><br>

- helpful mnemonic:<br>(7 down to 1) =  All People Seem To Need Data Processing
(Application, Presentation, Session, Transport, Network, Data Link, Physical.)<br><br>

### - Layer 1:  Physical Layer
- signaling, cabling, connectors (this layer not about protocols)
	- example of error msg or troubleshooting outcome of Layer 1: 
		- "You have a physical layer problem." 
		- how to solve: 
			- fix your cabling, punch-downs (?), etc. 
			- run loopback tests, test/replace calbes, swap adapter cards<br><br>

### - Layer 2:  Data Link
	- foundation of comm at data link layer, basic network language
	- DLC (data link control) protocols = MAC address (media access control)<br><br>

### - Layer 3:  Network Layer (or Routing Layer)
	- IP (internet protocol)
	- fragments frames to traverse different networks (ex.: switching back and forth between wifi and wired conneciton will fragment data)<br><br>

### - Layer 4:  Transport Layer ("post office" layer)
	- parcels and letters (?)
	- TCP (transmission ctrl protocol)
	- UDP (user datagram protocol)
	- when data must be sent in seperate frames and pieced back together<br><br>

### - Layer 5:  Session Layer
	- comm mgmt btwn devices (start, stop, restart)
	- control and tunneling protocols
	- set up session and begin transfering information<br><br>

### - Layer 6: Presentation Layer
	- character encoding, app encryption happen here
	- combine w/app layer often<br><br>

### - Layer 7:  Application Layer
	- the one we get to see
	- on screen is layer 7 app data
	- http, ftp, dns, pop3<br><br>


## Data Communication – N10-008 CompTIA Network+ : 1.1 (video)
https://www.professormesser.com/network-plus/n10-008/n10-008-video/data-communication/ <br><br>

### PDU (Protocol Data Unit)
- Transmission units:
	- a different grp of data @ different OSI layers

Ethernet operates on a frame of data

IP operates on a packet of data

TCP or UDP


Encapsulation and decapsulation
	Application data exists at Layers 5, 6, 7
	
- Each layer has a header and a payload<br>
- the header describes or identifies the payload<br>
- the tcp header contains important control information
	includes set of bits called TCP flags
	flags ctrl the payload: 
	- -SYN: sync sequence numbers
	- -PSH: push the data to the app w/o buffering
	- -RST: reset the connection
	- -FIN: last packet from the sender

**MTU = max transmission unit**<br>
max IP packet to transmit (but not fragment)<br>
difficult to know the MTU all the way through the path
automated =<br> 
inaccurate, esp when ICMP is filtered 

 In the linked video, there is a demo of 
- building an Ethernet frame.
- IP fragmentation (in mult's of 8)
- troubleshooting MTU = concern for tunneled traffice
- troubleshoot w/ ping: ping w/ "don't fragment", force a max size of 1472:
	- Windows: ping -f -l 1472 8.8.8.8
	- Linux, maxOS: ping -D -s 1372 8.8.8.8

### The following article and notes are very important to understand:<br><br><br><br>

## Understanding Network Data Delivery: Layers 2 and 3 of the OSI Model
https://www.comptia.org/blog/layers-2-and-3-osi-model <br><br>

### LAYER 3: NETWORK LAYER - OSI MODEL
- responsible for packet forwarding, incl routing thru intermdte routers

### UNDERSTANDING NETWORK DELIVERY
**How do Layers 2, 3 work together?**<br><br>

- Layer 2: the DATA LINK layer = 
	-"transfers data btwn nodes on a network segment across the physical layer" (commonly known as a host's physical address)
	- divided into 2 parts: MAC sublayer, data link sublayer
		- MAC sublayer: device address, is permanent to the device; devices can comm directly through switch 2.		
- data link sublayer: a second layer of addressing implemented for comm btwn devices when MAC no longer sufficient re network congestion, there are more devices
		- together these sublayers make up the pc's phsysical address
- Layer 3:  incl's host's logical address
	- outside envelope over the Layer 2 frame, that incl's layer 3 address of sender of packet & layer 3 address of recipient
	- addresses divided to identify specific network address, specific host/group of hosts
		- if recip ntwork addy = diff than sender ntwork addy, packets directed to ntwork's router for delivery handling
	- TCP/IP protocols used for comm crossing ntworks
- How an IP is structured:<br><br>
172.16.	...|  1. 		..........|  12<br>
...................|................|<br>
Network	| Subnet	| Host<br><br>

IP addresses = both network, host identification<br>
- allowing devices on same network able to comm at layer 2
- allowing devices on diff networks to comm: direct their output data to routers responsible for delivery<br><br><br><br>
		

## What Is Wireshark and How to Use It
https://www.comptia.org/content/articles/what-is-wireshark-and-how-to-use-it <br><br>

**Analysis in real-time and offline; discover root cause of problems**<br><br>


### A network protocol analyzer
**most used in the world**<br><br>


Three Things Wireshark does: 
1.  Packet Capture:  listens to ntwork connec'n, grabs streams of traffic (thousands of packets at a time)
2.  Filtering:  to obtain needed information only
3.  Visualization:  GUI provides visual of network streams, conversations<br><br>


**Article compares Wireshark to exploring a cave w/ a flashlight to see what "cool things" you can find**<br><br>


### Used for: 
- troubleshooting networks
- trace connections
- view contents of suspect ntwork transactions
- identify bursts of network traffic<br><br>


**Must-have in IT pro toolkit**
*Note to self: get good at Wireshark*<br><br>


### Things to know about Wireshark: 
1.  To use, understanding is a must with regard to the following: 
    - three-way TCP handshake
    - protocols: TCP, UDP, DHCP, ICMP<br><br>

2.  "Can only sniff traffic btwn local comp and the remote system it is talking to."

3.  Not an (IDS) Intrusion Detection System.

4.  Cannot decrypt encryped traffic

5.  Cannot determine if IPv4 packet real IP or spoofed IP.<br><br>

### Common Uses
- drill down to find connection issues
- can identify version of TLS browser and website w/connection issues
- identify specific retransission issues using packet flow statistics, allows router or switch reconfig to speed it back up<br><br>


### Install on Linux
1.  sudo apt-get install wireshark; or<br> (sudo dpkg-reconfigure wireshark-common; sudo usermod -a -G wireshark USER; newgrp wireshark)

2.  Once you have completed the above steps, you then log out and log back in, and then start Wireshark:

3.  $ wireshark &<br><br>


### Capturing Packets:
*Note: Must have admin or root access to pc*<br><br>


1.  Capture, Options (frm main window)
	- brings up Capture Interfaces dialog, lists all avail. interfaces
2.  Select an interface, perhaps the most active one
	- visualizes with moving line = packets on network
3.  click Start button to begin captuer
4.  Let it capture all packets you want
	- then click red square button at the top
5.  Static packet is captured for you to investigate<br><br>


### Color Coding in Wireshark
Light purple: 	TCP
Light blue: 		UDP
Black: 		Packets w/errors
Light green: 		HTTP traffice
Light yellow: 	windows-specific traffic - incl SMB, NetBIOS
Dark yellow: 	Routing
Dark gray: 		TCP SYN, FIN, ACK traffic<br><br>


### How to filter and inspect packets<br>
1.  Display Filter window at top of screen
2.  highlight packet (or portion), right click on packet<br><br>


filter key phrases:<br> 
	- ip. addr - specifies IPv4 address<br>
	- ipv6.addr - specifies IPv6 address<br>
	- src - source (where packet came from)<br>
	- dst - destination (where packet is going)<br>

	- && = "and"<br>
	- == = "equals"<br>
	- ! = "not"<br><br>

valid rules = green<br>
bad filter rule = hot pink

