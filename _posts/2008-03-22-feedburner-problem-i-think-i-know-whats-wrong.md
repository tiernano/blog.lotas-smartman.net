---
title: 'feedburner problem: i think i know whats wrong'
author: admin
layout: post
permalink: /feedburner-problem-i-think-i-know-whats-wrong/
dsq_thread_id:
  - 26008739
categories:
  - Uncategorized
---
i posted [here about feedburner not updaing my feeds][1]. well i think i know why. My IP address changed a while back, before yesterday, but not sure exactly when. this is the problem with running a webserver from home. anyway, i think they may just have the old ip address. im just checking the TTL of the dns server info now. right i just fixed the DNS info (i hope). it was set to 10 days for the expire info, so i now set it to 1day. refresh is 2 hours, retry is 1 hour and what ever else. i hope this works grand! hopefully i wont break anything&#8230;.

 [1]: http://blog.lotas-smartman.net/%22http://blog.lotas-smartman.net/archives/2004/03/26/1633/just-testing-feedburners-ping-updates//%22