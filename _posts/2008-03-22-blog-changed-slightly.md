---
title: Blog changed slightly
author: admin
layout: post
permalink: /blog-changed-slightly/
categories:
  - Uncategorized
---
Ok. i changed the amount of days displayed on the front page from 7 to 4. The original page with 7 days was reaching 110k. thats not good. mind you its still reaching 77k now, but im working on getting [Mod_GZip][1] on the server so i can make it even smaller. [this page][2] from [PipeBoost][3] reckons if i was running pipeboost and win2k (which is needed, and IIS) i could compress the page to about 15k. I would not be suprised. i have used it before and it was quite good. Now im on apache, i need mod_gzip. have to install [Apache][4] 1.3.whatever, cause 2.0 doesent have moz_gzip available for it, i dont think.

 [1]: http://godonlyknows.lotas-smartman.net/?q=mod_gzip
 [2]: http://www.pipeboost.com/getreport.asp?URL=http%3A%2F%2Flotas-smartman.net%2Fblog
 [3]: http://www.pipeboost.com
 [4]: http://www.apache.org