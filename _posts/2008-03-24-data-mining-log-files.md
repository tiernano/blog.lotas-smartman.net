---
title: Data mining Log files
author: admin
layout: post
permalink: /data-mining-log-files/
dsq_thread_id:
  - 26012724
categories:
  - Uncategorized
---
I found [this article over on OnLAMP about Data mining log files][1]. Well it got me thinking. i have a lot of log files on my server (about 4 months of them!) and i want to see some interesting info about it, like total bandwidth usage, ask it questions about where visitors came from, etc. i could very easly use a log analyzer, but thats no fun! i want to write something like this my self. so far i have managed to read the log files into a listbox and also work out if they are proper lines or fake lines (The ones IIS puts in at the start. these usually start with a #). Next on the list is working out unique visitors, and also working out stuff like DB and the like. code soon, hopefully&#8230;

 [1]: http://www.onlamp.com/pub/a/onlamp/2005/03/03/pg_datamining.html