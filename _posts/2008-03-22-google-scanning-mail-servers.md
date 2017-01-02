---
title: Google scanning Mail servers?
author: admin
layout: post
permalink: /google-scanning-mail-servers/
dsq_thread_id:
  - 26009668
dsq_needs_sync:
  - 1
categories:
  - Uncategorized
---
Just checking my logwatch email that i get daily from my linux box and this was in it:

> Did not issue MAIL/EXPN/VRFY/ETRN during connection to MTA:  
> 64.233.170.199 : 3 Time(s)  
> 64.233.170.195 : 2 Time(s)  
> 64.233.170.200 : 2 Time(s)  
> 64.233.170.193 : 1 Time(s)  
> 64.233.170.202 : 1 Time(s)  
> 64.233.170.205 : 1 Time(s)  
> 64.233.170.203 : 1 Time(s)

when i did a whois on the first IP, it responds that it is owned by Google, and is named rproxy.gmail.com. So, i did a bit more snooping of my log files and found this:

> May 4 15:15:54 robbin sendmail[19490]: i44EFssX019490: rproxy.gmail.com [64.233.170.199] did not issue MAIL/EXPN/VRFY/ETRN during connection to MTA  
> May 5 00:46:46 robbin sendmail[28788]: i44NkksX028788: rproxy.gmail.com [64.233.170.199] did not issue MAIL/EXPN/VRFY/ETRN during connection to MTA  
> May 5 10:48:08 robbin sendmail[3407]: i459m7sX003407: from=<newsalerts -noreply@google.com>, size=1744, class=0, nrcpts=1, msgid=<1083750486.14962.8922c0c5ee1138d0.23d3bdd0@persist.google.com>, proto=SMTP, daemon=MTA, relay=rproxy.gmail.com [64.233.170.199]  
> May 6 02:12:36 robbin sendmail[17559]: i461CZsX017559: from=<newsalerts -noreply@google.com>, size=1411, class=0, nrcpts=1, msgid=<1083805952.49870.2f40090edfed40e4.7bd06f31@persist.google.com>, proto=SMTP, daemon=MTA, relay=rproxy.gmail.com [64.233.170.199]  
> May 6 08:33:12 robbin sendmail[23910]: i467XCsX023910: rproxy.gmail.com [64.233.170.199] did not issue MAIL/EXPN/VRFY/ETRN during connection to MTA  
> May 6 10:55:33 robbin sendmail[26470]: i469tXsX026470: rproxy.gmail.com [64.233.170.199] did not issue MAIL/EXPN/VRFY/ETRN during connection to MTA  
> May 6 23:15:04 robbin sendmail[7657]: i46MF4sX007657: rproxy.gmail.com [64.233.170.199] did not issue MAIL/EXPN/VRFY/ETRN during connection to MTA</newsalerts></newsalerts>

I know google are sending me a news alert every time linux, longhorn or microsoft is found in the google news, but why is it asking me other questions? Strange&#8230;