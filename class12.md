Reading Notes <br>
Class 12<br>
Re: Radius Authentication, Methods, TACACS, Kerberos, and more<br><br><br><br>

*The purpose of this document is to facilitate my learning of various networking security topics.  It is created for my personal use, and is a summary, including paraphrasing and direct quotes, of information found in the article(s) linked within.*<br><br>

**Remote Authentication Dial-In User Service**<br><br>

RADIUS is a network management protocol that facilitates AAA management for network users. 
- a client/server protocol that runs in the application layer and can use either TCP or UDP
uses port 1812 (Authentication / Port 1813 Authorization<br><br><br><br>


## Radius Concepts
*https://wiki.freeradius.org/guide/Concepts*<br><br>


The article's author describes "how things work in RADIUS" as such:<br><br>
***"The client sends the server a RADIUS authentication request. You don't decide what's in the request, the client does. The server doesn't decide what's in the request, the client does. The client is 100% responsible for everything in the request."***<br><br>

### Picking an "Auth-Type" - authorize {}

### Authenticating a user - authenticate {}

### Insufficient information<br><br>

- server receives a RADIUS request from the client.
- the server reviews the request, comparig them to what modules the server has been configured  to allow through (authorization).
	- it checks the request for key attributes, like MS-CHAP-Challenge, CHAP-Challenge, or EAP-Message. 
- Authenticating a user:  after authorizing, server checks for an Auth-Type. If none, request is rejected.  
- otherwise it reviews the request's authentication type, like user/password.<br><br>

*I am certain I will get good information from this article in the near future, but for right now, I don't even know how to make notes from it.  It's an odd format that I'm sure I'll appreciate later.*<br><br><br><br>


### Things I want to know more about: <br><br><br><br>






Authentication Methods<br>
*https://www.professormesser.com/network-plus/n10-008/n10-008-video/authentication-methods-n10-008/*

Defense in depth<br>
*https://www.professormesser.com/network-plus/n10-008/n10-008-video/defense-in-depth-n10-008/*

RADIUS and TACACS<br>
*https://www.professormesser.com/security-plus/sy0-401/radius-and-tacacs-2/*

Kerberos<br>
*https://www.professormesser.com/security-plus/sy0-401/kerberos-2/*

