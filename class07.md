Reading Notes <br>
Class 07<br>
Re:  NGINX<br><br><br><br>



*This document is a summary of information in the article(s) linked within.*<br><br>

## What is NGINX?
https://www.nginx.com/resources/glossary/nginx/ <br><br>


**"NGINX is an open source software for web serving, reverse proxying, caching, load balancing, media streaming, and more."**<br><br>

- originally created as a performance and stability oriented HTTP web server. <br><br>
- other functions include: 
	- proxy server for email (IMAP, POP3, SMTP)
	- reverse proxy
	- load balancer for (HTTP, TCP, UDP servers)<br><br>

**Fun Fact:  NGINX was created by Igor Sysoev to solve the C10K problem in 1999.***<br><br>
- the existing web servers couldn't handle large numbers of simultaneous connections.  
	- (I remember Y2K, but had never heard of C10K. Neat.) 
- it revolutionezed high-volume server operation 
- was, and is still, the fastest web server available
	- can handle hundreds of thousands of connections at once 
- now NGINX Plus = offered as a commercial product for enterprise customers
- scalable<br><br>

### NGINX as a Web Server
- speed is the central goal
- now has grown to support the modern web: (WebSocket, HTTP/2, gRPC, streaming-- HDS, HLS, RTMP, etc.)<br><br>

### NGINX Beyond Web Serving
- use as a reverse proxy and load balancer: 
	- manages and distributes incoming traffic, distributes to slower upstream servers
- use as an SSL/TLS terminator / web accelerator:
	- compresses/caches content incoming, improves performance
	- reduces load application servers, allowing underlying app-related hardware to reach its potential in effectiveness<br><br>
 
### What can NGINX (or Plus) Do for You?
- Already used by many well-known, high volume sites: 
	- Netflix, Dropbox, Zynga, and 350 million others
- cloud-native architectures: 
	- software-only load balancer, web server, API gateway, content cache, reverse proxy
	- minimizes configuration tasks 
- documentation found here: https://docs.nginx.com/nginx/
	- ebooks and other learning materials: https://www.nginx.com/resources <br><br>

***NGINX is an always-growing product that is continually developed to keep up with the modern web, and maintains its place at the top among its peers for performace and stability.*** 
<br><br>
<br><br>
<br><br>
<br><br>