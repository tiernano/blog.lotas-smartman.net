---
title: using Memcached with ASP.NET
author: admin
layout: post
permalink: /using-memcached-with-aspnet/
dsq_thread_id:
  - 26016064
  - 26016064
categories:
  - Uncategorized
---
InfoQ has a post talking about using [Memcached with ASP.NET][1]. Interesting idea. your front end servers just server webpages, and maybe the odd webservice for Ajax. then your middle tier is just web services or WCF services serving data to the front end. Finally, your DBs are in the back. Your front end servers would have [Memcached][2] installed on them, and every request would hit Memcached first. very cool stuff&#8230;. [Win32 port of Memcached is here.][3]&nbsp;[Memcached API for C# here][4].</p> 

<div class="wlWriterSmartContent" id="0767317B-992E-4b12-91E0-4F059A8CECA8:fc06e44b-76fa-495c-ad32-246d5ae482f7" style="padding-right:0px;display:inline;padding-left:0px;padding-bottom:0px;margin:0px;padding-top:0px;">
  Technorati Tags: <a href="http://technorati.com/tags/Memcached" rel="tag">Memcached</a>, <a href="http://technorati.com/tags/Caching" rel="tag">Caching</a>, <a href="http://technorati.com/tags/ASP.NET" rel="tag">ASP.NET</a>, <a href="http://technorati.com/tags/programming" rel="tag">programming</a>
</div>

 [1]: http://www.infoq.com/news/2007/07/memcached
 [2]: http://www.danga.com/memcached/
 [3]: http://jehiah.cz/projects/memcached-win32/
 [4]: http://sourceforge.net/projects/memcacheddotnet/