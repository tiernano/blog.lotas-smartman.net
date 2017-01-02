---
title: Restoring Exchange to other hardware
author: admin
layout: post
permalink: /restoring-exchange-to-other-hardware/
categories:
  - Uncategorized
---
A while back i was thinking of moving my exchange box to new hardware. well, i still am. i found this article over at [MSExchange.org telling you how to do it][1], the proper way. but because my exchange server is quite small (3 user accounts) i was given a tip by Alex [here on the irishdev forums][2] which makes more sense. tell outlook to copy the mail to the local machine (local PST) and then, take the old server off line, put the new server online, copy all the email from outlook to exchange, and tell outlook to delever mail to the server. interesting idea, which i will probably try. first, i need new hardware though (a nice Athlon 64 system with at least a gig of ram, and 2 80Gb hdds to start with&#8230;).

 [1]: http://www.msexchange.org/tutorials/Restoring-Exchange-Server2003-Alternate-Hardware.html
 [2]: http://www.irishdev.com/forums/817/ShowPost.aspx