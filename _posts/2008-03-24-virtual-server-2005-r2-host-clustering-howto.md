---
title: Virtual Server 2005 R2 Host clustering howto
author: admin
layout: post
permalink: /virtual-server-2005-r2-host-clustering-howto/
dsq_thread_id:
  - 26015441
  - 26015441
categories:
  - Uncategorized
---
Check out these 5 Blog Casts from [John Howard, PM for Windows Virtulization][1], showing you how to build a [Virtual Server R2][2] Host cluster. The idea of&nbsp;this is cool. You have 2 large boxes, both running Virtual Server 2005 R2 and you have a couple of important VM&#8217;s you want to have High Availability on. With this walk though, you can have it. Very cool stuff!

[Part 1][3]  
[Part 2][4]  
[Part 3][5]  
[Part 4][6]  
[Part 5][7]

So, some ideas about this. You could have, lets say for arguments sake, a [SQL Box][8], [Exchange Server][9], [IIS Web Server][10], [ISA server][11] and [Team Foundation Server][12], all on 5 separate Virtual Machines. Then you would have 3 large enough boxes, each running some of the VM&#8217;s (we say the the ISA and Web server are on one box, TFA and SQL on another, and SQL on a third). and have them fail over as needed. so a machine goes down for extra memory, everything moves over to one of the other machines, and all is still up. then you can move things back when it comes up again. Very cool!

 [1]: http://blogs.technet.com/jhoward/
 [2]: http://www.microsoft.com/windowsserversystem/virtualserver/default.mspx
 [3]: http://blogs.technet.com/jhoward/archive/2005/11/29/415242.aspx
 [4]: http://blogs.technet.com/jhoward/archive/2005/11/29/415243.aspx
 [5]: http://blogs.technet.com/jhoward/archive/2005/11/30/415322.aspx
 [6]: http://blogs.technet.com/jhoward/archive/2005/12/01/415388.aspx
 [7]: http://blogs.technet.com/jhoward/archive/2005/12/02/415459.aspx
 [8]: http://www.microsoft.com/sql/
 [9]: http://www.microsoft.com/exchange
 [10]: http://www.microsoft.com/WindowsServer2003/iis/default.mspx
 [11]: http://www.microsoft.com/isaserver
 [12]: http://msdn2.microsoft.com/en-us/teamsystem/aa718825.aspx