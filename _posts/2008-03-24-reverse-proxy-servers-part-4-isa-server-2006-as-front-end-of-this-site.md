---
title: 'Reverse Proxy Servers, part 4: ISA Server 2006 as front end of this site'
author: admin
layout: post
permalink: /reverse-proxy-servers-part-4-isa-server-2006-as-front-end-of-this-site/
dsq_thread_id:
  - 26016443
  - 26016443
categories:
  - Uncategorized
---
this is now the 4th part of the Reverse Proxy Saga going on with this network ([Part 1][1], [Part 2][2] and [Part 3][3]). today I have implemented an [ISA 2006][4] server sitting in front of the web servers. it actually seems to be working quite well, plus I have the advantage of everything being compressed outbound, if the client supports it. 

The problem with [Squid][5], which was originally running the site, was that outbound compression was not supported. Also, I got the impression that Squid though of Windows as a second class citizen. not everything was supported on Squid on Win32, which was a pity. 

I am currently using it as a Virtual machine on my main workstation, but I hope to move to a full, non Virtualized build soon. If your interested, [ISA info is here][4], and the [VHD image (30 day trial) is here][6].

 [1]: http://blog.lotas-smartman.net/archive/2007/10/03/reverse-proxy-servers.aspx
 [2]: http://blog.lotas-smartman.net/archive/2007/10/03/reverse-proxy-servers-part-2.aspx
 [3]: http://blog.lotas-smartman.net/archive/2007/11/20/reverse-proxy-servers-part-3.aspx
 [4]: http://www.microsoft.com/isaserver/default.mspx
 [5]: http://www.squid-cache.org/
 [6]: http://www.microsoft.com/downloads/details.aspx?FamilyID=234c9dda-5452-4946-9e2f-d4b64082814e&DisplayLang=en