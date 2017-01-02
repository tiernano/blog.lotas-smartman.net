---
title: Update on the fixing of my exchange box
author: admin
layout: post
permalink: /update-on-the-fixing-of-my-exchange-box/
categories:
  - Uncategorized
---
Yesterday, i said [i was going to fix my Exhcnage server][1] which died a few weeks back. i also said last night that [i got it back up and running][2] and that ISA server was being annoying and not wanting to work properly. well, its still like that. There is a problem with MSDE, for some reason, and i tried reinstalling it this morning (MSDE that is) and now i think MSDE works, but ISA doesent know where it is (new instance, or old instance with new password. something weird there). Anyway, i ran out of hacking time before i had to leave for work this morning, so tonight i will be trying to reinstall ISA and get the MSDE instance working. one thing i can say though. When i loged into the win2k3 server, i got an error saying that a file ending in RLL (resource link library?) was missing or not loaded. this was in a directory like 63?? but there was no directory like that. there was a 1033 directory, which is English, so i guess it was a resource file. lots of weirdness going on there. when i reinstalled MSDE, that error stoped, so i hope i am on my way to it working properly. i also found out that there is a massive 200,000 emails sitting in my exchange user account and an other 35,000 in the current pop3 server, which will have to be ported to the exchange box over the next few days. that should be fun!

 [1]: http://blog.lotas-smartman.net/archive/2005/03/07/11131.aspx
 [2]: http://blog.lotas-smartman.net/archive/2005/03/07/11135.aspx