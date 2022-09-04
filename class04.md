Reading Notes <br>
Class 04<br>
Re Group Policy (GPO)<br>
Wireless Standards, Technology, Encryption<br><br><br><br>




*Information below is summarized from the associated linked articles found within this document.*<br><br>

## What is Group Policy (GPO) and What Role Does It Play in Data Security
https://www.lepide.com/blog/what-is-group-policy-gpo-and-what-role-does-it-play-in-data-security/

GPO settings are created in the Group Policy Editor within the MMC (Microsoft Management Console) 
- managed by sys admin
- gp's control working environments of users in Active Directory (AD)<br><br>


### What is a Group Policy Object (GPO)?
- found within MMC GP Editor
- can be associate with single or multiple AD containers
	- sites, domains, OU's (org'l units)
		- registry-based policies, security options, software installation, etc.<br><br>


### Examples:
- GPO used to determine the home page that a user sees when launching browser after logging in to domain
- to define which network printers appear to a user in a specific AD
- to tweak security  protocols and practices, like restricting internet connection options, programs, screen time, site availability, etc.<br><br>


### Order of GPO procession: 
- **LSDOU**
	1. Local (local computer)
	2. Site (site level)
	3. Domain (domain AD policies)
	4. Organizational Unit
- *conflicting policies = last applied policy "wins"<br><br>


### Some Security Uses: 
- Policy of Least Privilege
	- users only have permissions required to perform duties 
		- sys admin must disable Local Administrator rights globally, then grand admin access to those whose role requires it
- disabling outdated protocols
- prevent users from making changes to system
- Data Security
	- password policy: establish Length, Complexity, Frequency of required password change
	- systems mgmt: configure new users with pre-set rules defined by role of user in organization
	- health checking: deploy updates, system patches against lates security threats<br><br>


### Limitations
- not user friendly
	- understanding Powershell helps with GPO updates
		- these can be configured to automatically apply in intervals between 0 minutes (7 seconds to the machine) and 45 days
		- setting updates too frequently will clog network traffice
- not immune to cyberattack 
	- difficult to detect without a GP auditing and monitoring solution in place
		- Lepide Data Security Platform (gp auditing and monitoring
			-https://www.lepide.com/lepideauditor/group-policy-auditing.html
			- when a critical change is made, Lepide sends admin real time alert w/option to roll back unwanted changes and revert to the previous state. 
			- assists with policy of least privilege<br><br>




## Wireless Standards – N10-008 CompTIA Network+ : 2.4
https://www.professormesser.com/network-plus/n10-008/n10-008-video/wireless-standards-n10-008/

### - Six popular 802.11 standards, speeds, frequencies, etc. 
	1. 802.11a = 
		- 5 GHz:    max 54 mb/sec
	2. 802.11b = 
		- 2.4 GHz: max 11 mb/sec
		- no MIMO
	3. 802.11g = 2.4 
		- 2.4 GHz: 54 mb/sec
		- no MIMO
	4. 802.11n =
		- 5 GHz either/or 2 GHz: max 150 mb/sec each
			- total throughput 600 mb/sec
		- MIMO w/four seperate streams
	5. 802.11ac = 
		- 5 GHz: 867 mb/sec each 
			- total 6.9 gb/sec
		- MIMO
	6.  802.11ax = 
		- 5 GHz either/or 2 GHz: max 1200 mb/sec each
			- total throughput 9.6 gb/sec
		- bi-directional MIMO w/eight streams<br><br>


## Wireless Technologies – N10-008 CompTIA Network+ : 2.4
https://www.professormesser.com/network-plus/n10-008/n10-008-video/wireless-technologies-n10-008/

### Frequencies
- 802.11 = either/or: 2.4, 5 GHz
	- can be used on same access point
	- can support comm. over add'l frequencies (not common, but interesting)
		- these add'l frequency groups = "channels"
		- #'d and assigned by IEEE<br><br>

### Channel Bandwidth
- range of frequencies / amt of frequency in use/would be in use
	- ex.: 2.4 GHz used on 802.11 network
		- in North America: three non-overlapping channels: 
		- 1, 6, and 11; in **20-megahertz** blocks
		- btwn 2,412 and 2,482 megahertz
		- **40-megahertz** is wider bandwidth, uses more of the available frequencies when total bandwidth increased<br><br>

### Service Sets
- (IBSS) Independent Basic Service Set = 
	- ad hoc or direct comm. btwn two devices
- ad hoc = created for particular purpose, no implementation of access point to comm
	- can be permanent if on particular network
	- temporary to configure device to connect to wireless network that has no access point, once rebooted<br><br>
- (SSID) Service Set Identifier = wireless network name
	- larger organization networks have multiple access points
		- same SSID, different BSSID<br> 
- (BSSID) Basic Service Set Identifier
	- physical address/media access control address of wireless access point
	- MAC address of access point behind the scenes, while user just uses SSID<br><br>
	
- (ESSID) Extended Service Set Identifier
	- allows use of same wireless name to be used across all locations of organization<br>
	- ex.: network switch connects to multiple access points
	- access points have different BSSID's, MAC addresses 
		- access points share same SSID
	- when walking through organization building with mobile device, it will automatically connect to access point most local bc it has same config as ESSID originally connected to
	- this setup can be configured at home, too (i am going to do it this way instead of giving my access point a different name)<br><br>
	
To send/receive info simultaneously: 
	- need appropriate # of antennas, support proper # of streams
	- ex.'s: 2 by 2:2 or 4 by 4:4 = 
		- first # = # of antennas on access point
		- then "x"
		- # of antennas on client
		- (after colon) total # of streams supported for that device<br><br>

### MIMO
- *(MIMO) = multiple input multiple output*
	- (means it supports multiple devices to send/receive info at same time)
	- OFDMA = Orthogonal Frequency Division Multiple Acces
		- streams broken into smaller pieces
		- only required data sent to/from individual devices<br><br>

### Miscellaneous
- parabolic antenna - focus signal to single point<br><br>



## Wireless Encryption – N10-008 CompTIA Network+ : 2.4
https://www.professormesser.com/network-plus/n10-008/n10-008-video/wireless-encryption-n10-008/

### WPA2
- Wifi Protected Access (version 2, 2006)
- (CCMP) or (Counter/CBC-MAC Protocol) Counter Mode with Cipher Block Chaining Message Authentication Protocol 
	- CCMP uses AES encryption, CBC-MAC for Message Integrity Check (MIC)
- secure, but vulnerable to brute force attacks on hashed password<br><br>


### WPA3
- (version 3, 2018)
- (GCMP) Galois/Counter Mode Protocol = stronger encryp. than vers. 2
- includes same encryp, checks as vers. 2, but adds (GMAC) Galois Message Auth'n Code<br><br>


### Pre-shared keys
- shared password used for entire wireless network
	- if using this, the hash sent across the network can be derived by attackers
		- this alone does not provide network access, but using hash, pre-shared key can be determined<br><br>


### SAE
- (SAE) Simultaneous Authenication of Equals
	- handshake protocol, enables secure exchange of keys of password-based auth'n methods
- used by WPA3<br><br>


### Miscellaneous
- (MIC) Message Integrity Check = ensures data sent is what is being properly received on other side of connection<br><br>


### Things I want to know more about:<br><br>
<br><br>







