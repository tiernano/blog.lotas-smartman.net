---
title: 'Windows Server &quot;Longhorn&quot; Virtualization'
author: admin
layout: post
permalink: /windows-server-longhorn-virtualization/
dsq_thread_id:
  - 26015640
categories:
  - Uncategorized
---
Check out this Soap Box video showing you how [Windows Server code named &#8220;Longhorn&#8221; does virtualization][1]. Some very cool bits a pieces in there. Its again one of those things that i dont actually need (like [grid computing][2] or a [SAN][3]/[iSCSI][4] system) but its something that could be handy. At the moment i have 2 main servers running on my network: a 64bit dual proc opteron with 2Gb ram running as a SQL server, Virtual Server, application server and Domain controller/DNS server. Then there is the poweredge server, which acts as front end web server, Exchange email server, Domain Controller/DNS server and does a bit of file serving. Now, the theory behind virtualization would be to get 2 large machines (say dual proc, dual/quad core) with lots of ram, and a shared storage pool (SAN or iSCSI). each machine would have their own workload (say the exchange box living on one machine, using 2gb ram and 1 processor, a web server VM running on each box (for load balancing) and a SQL cluster. so, in reality, say 5 seperate work loads, maybe 8 different VMs. if one VM needs more memory, but the parent machine does not have it, it could move to the next box, without too much hassle. if a phyicial machine needs a memory upgrade, it would move its VMs to the other box, load them up their, shut them down on its self, and power down for extra RAM. then, when it wakes back up, take them back and work with them again.

It also makes backup a bit easier in that you can backup an entire machine. Very cool stuff.&nbsp;

 [1]: http://soapbox.msn.com/video.aspx?vid=5119240c-6579-4827-8338-7f5539930402
 [2]: http://blog.lotas-smartman.net/archive/2007/03/04/alchemi-net-based-enterprise-grid.aspx
 [3]: http://blog.lotas-smartman.net/archive/tags/SAN/default.aspx
 [4]: http://blog.lotas-smartman.net/archive/tags/iscsi/default.aspx