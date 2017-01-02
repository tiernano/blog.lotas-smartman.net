---
title: Memcached with ASP.NET part 2
author: admin
layout: post
permalink: /memcached-with-aspnet-part-2/
dsq_thread_id:
  - 26016105
  - 26016105
categories:
  - Uncategorized
---
I have talked about [Memcached][1] [before][2], but now i actually got a chance to use it! This rocks! the Firewall on my main machine is causing some interesting problems (not letting me connect to the daemon) but i have gotten the daemon working on a different machine, and it works perfectly. I tried writing my own code to talk to Memcached, but things went haywire, so instead, I used the code from [this Code Project article][3], which works great. The [Win32 port is available here][4]. </p> 

<div class="wlWriterSmartContent" id="0767317B-992E-4b12-91E0-4F059A8CECA8:f5f747a2-5f70-4681-ab12-097b81183275" style="padding-right:0px;display:inline;padding-left:0px;padding-bottom:0px;margin:0px;padding-top:0px;">
  Technorati Tags: <a href="http://technorati.com/tags/Memcached" rel="tag">Memcached</a>, <a href="http://technorati.com/tags/ASP.NET" rel="tag">ASP.NET</a>, <a href="http://technorati.com/tags/Programming" rel="tag">Programming</a>, <a href="http://technorati.com/tags/Code%20Project" rel="tag">Code Project</a>
</div>

 [1]: http://www.danga.com/memcached/
 [2]: http://blog.lotas-smartman.net/archive/2007/07/22/using-memcached-with-asp-net.aspx
 [3]: http://www.codeproject.com/useritems/memcached_aspnet.asp
 [4]: http://jehiah.cz/projects/memcached-win32/