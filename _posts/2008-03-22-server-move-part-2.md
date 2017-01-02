---
title: server move part 2
author: admin
layout: post
permalink: /server-move-part-2/
dsq_thread_id:
  - 26006527
categories:
  - Uncategorized
---
this could be quite cheap to do with [NFS][1]. i reckon that i use about 112mb a week for my blog and [the hairy one.com][2]. the other sites are quite small and probably use a max of 20mb a week. there is a gcache script, which is a pain in the arse and i cant get rid of it, which askes the server for it, and its not there (404 error). im guessing it takes up about 40 &#8211; 50mb a week (just putting a php file up which will send a 404 message). by my calculations it totals about 2gb a month. then, the sites get crawled by google bot and the rest, so an other 2 &#8211; 4 gb in there (big site!) and thats 6gb total. im guessing a max of a tenner a month total. if times are slow and traffic is down, its cheaper. if traffic goes up, its limited by how much is in my account. i like this. ill try it soon.

 [1]: http://www.nearlyfreespeech.net
 [2]: http://www.the-hairy-one.com