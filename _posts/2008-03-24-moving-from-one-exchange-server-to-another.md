---
title: 'Moving from one exchange server to another&#8230;'
author: admin
layout: post
permalink: /moving-from-one-exchange-server-to-another/
dsq_thread_id:
  - 26013203
  - 26013203
categories:
  - Uncategorized
---
Ok. as some of you may know, i run my own [Exchange 2003][1] box at home. the server is a [Windows 2003 Server][2] box with [ISA2004][3] and [Exchange 2003][4] on it (actually it has [WSUS][5] on there too). The problem is that when i set this up, i dident realise how important it was to have more then one network card in the system, and more then one network. the networks are ment to be seperate. so, now my problem is ActiveSync over the air works half of the time, ISA2004 server has a problem with publishing internal servers, but exchange works grand.

So, why am i saying all this. Well, i want to install [SBS2003][6] on my main server (currently the exchange box) and move all the existing logs and messages with it. i also wouldent mind getting my old data which i still have in log files, back into the exchange box. so, does anyone know of any ways of doing this? i know i should &#8220;Ask Google&#8221; but i dont have time now, i will research it over the next few hours, but if anyone has any tips or tricks or how tos (i know this is resyndicated on [Developers.ie][7] and i know there are lots of smart people there <img src="http://blog.lotas-smartman.net/wp-includes/images/smilies/icon_razz.gif" alt=":P" class="wp-smiley" /> will flattery get me my answer?) can you post a comment, or email me at <a href="mailto:tierno@lotas-smartman.net" hre="mailto:tierno@lotas-smartman.net">tierno@lotas-smartman.net</a>. 

I will post an article explaining what has happened over the next few days. one thing that has to be done is cleaning of the systems. there is a LOT of dust inside the 2 servers. I hope to have down time to a minimum. I plan to use [Virtual Server][8] on my workstation, which is already acting as the [SQL server][9], and using Win2k3 server on the [Virtual Server][8], that that running the web site. Email will be backed up thanks to [ZoneEdit][10], so thats handy. Wish me luck! <img src="http://blog.lotas-smartman.net/wp-includes/images/smilies/icon_smile.gif" alt=":)" class="wp-smiley" />

 [1]: http://www.microsoft.com/exchange
 [2]: http://www.microsoft.com/windowsserver2003/default.mspx
 [3]: http://www.microsoft.com/isaserver/default.mspx
 [4]: http://www.microsoft.com/exchange/default.mspx
 [5]: http://www.microsoft.com/windowsserversystem/updateservices/default.mspx
 [6]: http://www.microsoft.com/windowsserver2003/sbs/default.mspx
 [7]: http://www.developers.ie
 [8]: http://www.microsoft.com/virtualserver
 [9]: http://www.microsoft.com/sql
 [10]: http://www.zoneedit.com