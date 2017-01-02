---
title: Tunnelling over SSH
author: admin
layout: post
permalink: /tunnelling-over-ssh/
dsq_thread_id:
  - 26008051
categories:
  - Uncategorized
---
Right. i was just messing with the mac for a while, and i connected to the internet though a dial up modem at 56k (compaied to my 1mb) just to see how fast my websites loaded. anyway, while i was testing that, i remembered about reading something ages ago about tunnelling http traffic over an SSH connection, using compression. So, after searching the web, i found [this article][1] on how to do it for email and FTP, and modified the command to do it with Squid. So basicly, since i was trying it on a MacOSX box, i used the Linux client Config. i typed the following command:

<font face="Courier New">ssh <SSH Server IP> -L 3128:192.168.1.2:3128</font>

and it worked. SSH Server IP is the ip of my server over the internet. 192.168.1.2 is my local ip address of the squid box (non accessable over the web) and the 3128 ports are the port of the local machine to want to tunnel from and the other is the port on the other server. not sure which one is which, thats why i left them both a 3128. then, to get it compressed, i just added -C. i also have to login as a user, so, i added -l and my username. thats about it. once SSH logged into the server, i then just told OSX to use localhost as the proxy with port 3128, and it works!! pages seem to load quicker too! SWEET!

 [1]: http://www.ccs.neu.edu/groups/systems/howto/howto-sshtunnel.html