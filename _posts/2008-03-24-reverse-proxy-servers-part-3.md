---
title: Reverse Proxy Servers, Part 3
author: admin
layout: post
permalink: /reverse-proxy-servers-part-3/
dsq_thread_id:
  - 26016316
dsq_needs_sync:
  - 1
categories:
  - Uncategorized
---
a few weeks back, I talked about using [Squid as a reverse proxy for the site][1]. well, a guy named Robert, also from Ireland, posted a comment and mentioned that he had used a similar idea, and [gave details on his blog on how to do it][2]. He also has a [Wiki Page with more info about the setup][3]. Well, a few minutes ago, after some shouting at some of my servers, I decided to enable this on my network. All web traffic is now flowing though my Squid proxy server (only some is actually getting cached, like images, CSS and some java script). not only that, but it now knows about other servers in the house. so, some sites are being served off the Opteron, and another is being served from my main workstation.

This is now very cool. for testing, I can fire up a Virtual Server box, copy content to it, and a quick change of a squid instance, and we are all good. handy! 

By the way, congratulations [to Sylwia and Robert on their baby Boy, Lucas][4]. And while we are at it, to [Mo and Scott on the arrival of their baby boy Thabo][5].

<div class="wlWriterSmartContent" id="scid:0767317B-992E-4b12-91E0-4F059A8CECA8:e8958340-1f6e-4d6c-92bc-a7489afcf668" style="padding-right: 0px; display: inline; padding-left: 0px; float: none; padding-bottom: 0px; margin: 0px; padding-top: 0px">
  Technorati Tags: <a href="http://technorati.com/tags/servers" rel="tag">servers</a>, <a href="http://technorati.com/tags/proxy" rel="tag">proxy</a>, <a href="http://technorati.com/tags/squid" rel="tag">squid</a>, <a href="http://technorati.com/tags/Opteron" rel="tag">Opteron</a>, <a href="http://technorati.com/tags/PowerEdge" rel="tag">PowerEdge</a>, <a href="http://technorati.com/tags/Mac%20Pro" rel="tag">Mac Pro</a>, <a href="http://technorati.com/tags/Scott%20Hanselman" rel="tag">Scott Hanselman</a>, <a href="http://technorati.com/tags/Robert%20Sweetnam" rel="tag">Robert Sweetnam</a>, <a href="http://technorati.com/tags/Babys" rel="tag">Babys</a>, <a href="http://technorati.com/tags/Ireland" rel="tag">Ireland</a>
</div></p>

 [1]: http://blog.lotas-smartman.net/archive/2007/10/03/reverse-proxy-servers-part-2.aspx
 [2]: http://blog.sweetnam.eu/2007/10/30/is-everything-working-ok/
 [3]: http://www.sweetnam.eu/index.php/Reverse_Proxy_with_Squid
 [4]: http://blog.sweetnam.eu/2007/11/16/its-a-boy/
 [5]: http://www.hanselman.com/blog/BabyThaboArrives.aspx