---
title: Seriously rethinking my network rebuild, for a while
author: admin
layout: post
permalink: /seriously-rethinking-my-network-rebuild-for-a-while/
dsq_thread_id:
  - 26013215
categories:
  - Uncategorized
---
Ok. I have been talking about a network upgrade for the last few days ([here][1] and [here][2]) and i have gotten some things started, like installed SBS 2003 on a Virtual Server, for testing, and backed up exchange, etc. Well, it got me thinking. Its a rebuild, but its not that &#8220;Future Proof&#8221;. The current backbone of the network is an aging AMD Athlon 1.33Gz with 512mb RAM and 30Gb of HDD. Its acting as an Exchange Server, ISA 2004 server, Active Directory Domain controler, DNS server for the network, and some other things. So, i decided to see what i can get as a new server. So i checked out my [&#8220;not so local&#8221; computer store][3] (their warehouse is in Norway, if i remember correctly and im in Dublin) and found that for a little over EUR500 including shipping, i can get a 2.4Gz Athlon 64 processor (the 512kb cache one) with a mother board with GigE lan, 2 80Gb hdds (Samsungs, 7200RPM, 8Mb cache and NCQ) and 2 512MB DDR PC3200 DIMMs. Also, im looking at a standard AGP graphics card (its a GeForce MX4000, so hopefully there will be 64bit drivers for it) which gets me nicely to my next point: 64BITS. I think that this server will be the next big thing in the network (just before my Dual Opteron with Dual Cores comes in, sometime before the end of the year&#8230;). If i get a nice new 64 bit server, i can run Exchange 2003 on it, MSSQL, AND probably still have some power for IIS web serving. That will mean my current web server (Duron 700Mhz with 384Mb ram) can do other things (development server or something, maybe a dedicated WSUS server&#8230;) and my current Exchange box (1.33Gz athlon talked about above) will become dedicated ISA 2004 router/proxy/etc. At the moment, that looks very likly. other things to concider before i get out the credit card and buy this: 1: upgraded internet connection. Currently looking at getting a dedicated 2mb connection from Irish Broad Band (2mb wireless internet connection, business broadband. very cool). I may also get a dual headded router (so both connections work together, which is 5mb/s down, and 2.3mb/s up!) and finally, network infrastructure (GigE LAN switch, proper KVM switch, more switchs&#8230; etc). So, down time for this weekend is off. Currently thinking for somewhere in the region on the last week in July. Lets see how that goes!

 [1]: http://blog.lotas-smartman.net/archive/2005/07/02/11827.aspx
 [2]: http://blog.lotas-smartman.net/archive/2005/07/01/11824.aspx
 [3]: http://www.komplett.ie