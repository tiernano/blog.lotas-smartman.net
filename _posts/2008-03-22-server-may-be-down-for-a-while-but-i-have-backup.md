---
title: server may be down for a while, but i have backup!
author: admin
layout: post
permalink: /server-may-be-down-for-a-while-but-i-have-backup/
dsq_thread_id:
  - 26007996
categories:
  - Uncategorized
---
Right. I was playing with some site on the web, [PipeBoost][1], and it told me something interesting. if i use compession, i could save quite a lot of bandwidth and also make downloads faster. When checking the Blog Page, it reducied the size of the file by 74%! On standard archive pages it reducied the page size by 66%! this is great. only problem is its only for windows. so, there is [Mod_GZ][2] for apache. theres the little problem with it though. it currently only supports Apache 1.3 and im running 2.0 on the VDS Server. i have 2.0 on my local server too, but im thinking of copying all stuff over to the local machine, mirroring the site over there, then trying to get mod\_gz working on the server, bringing it back, testing, and then working with it. it may end up that i install mod\_gz on the local server first, and then try it on the server. makes more sence! anyway, i hope delays to be minimum. more info when i try it!

 [1]: http://www.pipeboost.com/
 [2]: http://sourceforge.net/projects/mod-gzip/