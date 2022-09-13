Reading Notes <br>
Class 11<br>
Re: Network Address Translation; Common Network Types and IPv4/IPv6 Addressing<br><br>

*This article supplemented our lecture in class today.  I've been wondering about the differences between network configurations, and I am finally learning all of them!*<br><br><br><br>

*This document is a summary of information in the article linked within, and includes paraphrasing and direct quotes of the original author.*<br><br>

**Network Address Translation** – CompTIA Network+ N10-007 – 1.3
*https://www.professormesser.com/network-plus/n10-007/network-address-translation-3/*<br><br><br>

## Network Address Translation (NAT)
- Private IP addresses: exist in private (local) network/home network/etc.
- ***NAT allows multiple devices (from a private network) to access the internet through a single public (global) ip address 
	- (the global ip address is supplied by the edge router)***
	- the edge router also masks the ports<br> (*to avoid the confusion that would be caused on the reply from the destination, as otherwise the ports would be the same and it would be unclear which reply belongs to which host*)<br><br>
- if NAT runs out of addresses in the pool of configured IP's, the packets are dropped
	- then an ICMP host unreachable packet to destination is sent 
	- (Internet Control Message Protocol)<br><br>
- NAT inside addresses = addresses that must be translated
	- inside local address: ip address assigned to a host on the inside/local/private network. 
	- inside global address: ip address that serves as the "avatar" ip address for one or more inside/local/private ip addresses to the outside world<br><br>
- NAT outside address = addresses that are not in control of an organization
	- outside local address: the actual IP address of the destination host in the local network after translation
	- outside global address: the IP address of the outside destination host before translation. 
### **NAT Configuration Types**
1.  Static NAT = one-to-one mapping btwn local/private and global/public ip  addresses
	- mostly for web hosting
	- for small private/home networks
2.  Dynamic NAT = a local/private IP is translated to a global/public IP from a pool of global/public addresses.  
	- there is a fixed number of private IP that can be translated to public IP's
	- for a fixed number of internet users needing access
3.  Port Address Translation (PAT) = many local/private IP's can be translated to single registered IP.  
	- port #'s distinguish traffic btwn IP addresses
	- most common, as thousands of users can be connected on one real global/public IP address<br><br><br><br><br>



Common Network Types – CompTIA Network+ N10-007 – 1.5
https://www.professormesser.com/network-plus/n10-007/common-network-types/ <br><br><br>

IPv4 and IPv6 Addressing – CompTIA Network+ N10-007 – 1.3
https://www.professormesser.com/network-plus/n10-007/ipv4-and-ipv6-addressing/ <br><br><br>


### Things I want to know more about: 