---
title: Blog speed issues (hopefully) gone away
author: admin
layout: post
permalink: /blog-speed-issues-hopefully-gone-away/
dsq_thread_id:
  - 26016597
categories:
  - Uncategorized
---
So, last night, after moving the blog to France, i realized that the site was still acting a bit slow&#8230;. so much for the server in house being under powered and over crowded&#8230; so, i asked on the Graffiti CMS forums would moving the Data backend to [MS SQL Server][1] instead of [VistaDB][2] make the site faster. And i was told yes, definitely. So, after a bit of playing around, and a lot of help from [David Penton][3] (who is a very elusive guy since i cant find his blog&#8230;.) and [Jayme Davis][4] (who helped me before with [setting up this site with Graffiti][5]), the blog backend is now SQL 2005 Express! I have noticed a large speed up on some pages, queries loading faster and fewer processor spikes! also, memory usage seems to be a lot more stable.

 [1]: http://www.microsoft.com/sql
 [2]: http://www.vistadb.net/
 [3]: http://dev.communityserver.com/user/Profile.aspx?UserID=45677
 [4]: http://telligenti.com/jaymedavis/default.aspx
 [5]: http://blog.lotas-smartman.net/graffiti-blog-now-live/