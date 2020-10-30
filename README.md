# jumpbox-docker-alpine
This is still a WIP:  
This is a jumpbox with an SSHd listening for connections.  It allows someone to ssh into the network to this box, and then "jump" to another host by opening ports to another host. For example forwarding RDP to a Windows host, or ssh'ing to another linux box, or forwarding X11 to another host.  

The sshd_config file has limitations placed on it for security (Beal, 2019):  

1. disable insteractive mode (no logins to the jump host are authorized, this is just a gatekeeper, no hanging out in the fatal funnel)  
2. force SSH version 2  
3. disable password auth (can't brute force a password if we aren't even checking for them)  
4. no root logins (see point 1.)  

Reference: Beal, Rob (2019, March 01). *Building an SSH Jumpbox with Docker*. Retrieved from https://engineering.land.tech/ssh-jumpbox/  
Check branch `landtech` for a PDF of the site if it becomes unavailable.  
