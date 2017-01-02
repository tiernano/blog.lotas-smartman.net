---
title: Auto detecting proxy servers using Windows Server
author: admin
layout: post
permalink: /auto-detecting-proxy-servers-using-windows-server/
dsq_thread_id:
  - 26016232
categories:
  - Uncategorized
---
So, over the last few days I setup&nbsp; a proxy server in the house on one of my older machines. I used [Squid][1], but i needed to work out how to get all machines to use it, automatically. [This article][2], over at Grape-Info.com has the information you need. there are 3 ways to do this: Web Proxy Auto Discovery, using DNS and WPAD files, DHCPINFORM, which uses DHCP to tell the machines what to do, and finally, Active Directory group policy. I am currently using a mixture of all 3. most machines will use the WPAD, and all getting IP addresses from DHCP will use that, but anything that has its own static IP, and is on the domain will use group policy. Handy!

<div class="wlWriterSmartContent" id="0767317B-992E-4b12-91E0-4F059A8CECA8:57348cdf-b542-40bd-bb97-89cade409243" contenteditable="false" style="padding-right: 0px; display: inline; padding-left: 0px; padding-bottom: 0px; margin: 0px; padding-top: 0px">
  Technorati Tags: <a href="http://technorati.com/tags/Squid" rel="tag">Squid</a>, <a href="http://technorati.com/tags/Proxy" rel="tag">Proxy</a>, <a href="http://technorati.com/tags/Windows" rel="tag">Windows</a>, <a href="http://technorati.com/tags/Active%20Directory" rel="tag">Active Directory</a>, <a href="http://technorati.com/tags/DHCP" rel="tag">DHCP</a>, <a href="http://technorati.com/tags/DNS" rel="tag">DNS</a>, <a href="http://technorati.com/tags/WPAD" rel="tag">WPAD</a>
</div></p>

 [1]: http://www.squid-cache.org
 [2]: http://www.grape-info.com/doc/win2000srv/internet-gw/wpad/index.html