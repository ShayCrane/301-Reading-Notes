Reading Notes <br>
Class 03<br>
Re Active Directory and DHCP<br><br><br>



## What is: Active Directory
https://www.cyberark.com/what-is/active-directory/<br><br>

### **AD is MS's directory and identity management service for Windows domain networks.**<br><br>  

**AD is made up of different directory services:** 
- AD DS: Active Directory Domain Services: core service used to manage users and resources. 
- AD LDS:   AD Lightweight Dir. Services: low over head version for directory-enabled applications
- AD cERTIFICATE Services
- AD Rights Mgmt Services

**Fundamental Features**
- schema
- global catalog
- query and index mechanism
- replication service

**AD Data Structures**
- domain
- tree
- forest

**AD Benefits**
- Security
- Extensibility 
- Simplicity
- Resiliency<br><br>

**Azure Active Directory: cloud-based identity management solution**<br><br>

**DHCP Overview - N10-008 CompTIA Network+: 1.6**
https://www.professormesser.com/network-plus/n10-008/n10-008-video/dhcp-overview-n10-008/

**IPv4 address config. used to be manual**
- subnet mask, a default gateway, or any other IP parameters)
- not practical
- Solution: bootstrap protocol, but not perfect-- did not define everything or when an IP would be avialable again
- Real solution: DHCP

**DHCP**
- DHCP server
- port 67
Example from video/article: 
- we have Sam on one side, Jack is on the other. Sam is connected to a switch... a DHCP server. 
- router connecting sites together 
- Jack is at this other site, connected to that router with a switch. 
- Config of Sam connecting to network: 
	-  needing an IP address. 
- Sam sendsDHCP Discover message from 0.0.0.0– because Sam does not have an IP address
	-  this is sent using UDP port 68 to 255.255.255.255. 
		- the broadcast address for a network. 
			- every device that is on this local network will see this message that Sam is sending, including the DHCP server 
- Sam's broadcast goes to UDP port 67.
- that broadcast is sent to all devices on the network. 
- A DHCP Discover message sent to a router that doesn’t have any DHCP services running would ignore the broadcast, 
	- but the broadcast does make it to the DHCP server on that local network. 
- DHCP server now wants to send a message back to Sam with potential IP addresses that Sam can use... 
	- called a DHCP Offer message, from its local IP address, which is 10.10.10.99, using UDP port 67, to a destination address of 255.255.255.255.


## Configuring DHCP - N10-008 CompTIA Network+: 1.6
https://www.professormesser.com/network-plus/n10-008/n10-008-video/configuring-dhcp-n10-008/

**DHCP pools:**


**Scope properties:**


**DHCP lease times**<br><br>


**Things I want to know more about**
- 
- 
- 