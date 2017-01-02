---
title: FreeCache
author: admin
layout: post
permalink: /freecache/
dsq_thread_id:
  - 26009721
categories:
  - Uncategorized
---
[FreeCache][1] is a pretty cool looking idea. Basicly, this sits on machines around the world, and users modify links on their site. The link on the site looks something like <http://freecache.org/http://www.lotas-smartman.net/wordpress/wp-images/smilies/icon_razz.gif> and that connects to the freecache server, downloads the page to the freecache server, and then sends it to the user. the next time someone downloads that page, its served by the freecache server without the use of the main web server. Only one little problem with this. It has been slashdotted! So, the requests are taking a long time to run, and most are timing out. If this ever gets back up and running, it will be something i might try for this site. Its like a poor mans [Akamai][2], or so [slashdot reckon][3].

 [1]: http://www.archive.org/web/freecache.php
 [2]: http://www.akamai.com
 [3]: http://slashdot.org/articles/04/05/12/1635205.shtml?tid=126&tid=95