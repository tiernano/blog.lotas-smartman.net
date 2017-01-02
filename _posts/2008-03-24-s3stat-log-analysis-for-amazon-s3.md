---
title: 'S3Stat: log analysis for Amazon S3'
author: admin
layout: post
permalink: /s3stat-log-analysis-for-amazon-s3/
dsq_thread_id:
  - 
  - 
dsq_needs_sync:
  - 1
categories:
  - Uncategorized
---
[<img src="http://images.lotas-smartman.net/image.ashx?id=b11f94ce-50b2-480d-a936-8f2da64d502b" align="right" border="0" />][1] So, about a month ago, I signed up for [S3Stat][1]. Its a log analysis system that reads your S3 log files and give you some very nice graphs and info about your S3 usage. 

To give you an idea of how cool and automated the system is, I actually haven&#8217;t logged into the site in the month I had it, and only though of it today. When I talked about [the image site on Friday Stats][2], I ran my own stats. the problem, I noticed, was that every hit was not being counted. if the ISA server on the front of my site cached the request, it was not written back to the SQL Server, so my stats may have been skewed. Also, anyone else with a proxy server could be getting cached results. The images, on the other hand, should be going direct to S3. Or at least I think they are. Anyway, in the last month of running stats (12th Feb to be exact) I have had 7000 hits and 83mb of files served. I have just signed up for my full account (only $2 a month, billed to your Amazon account, which is handy) and I am very happy, so far.

 [1]: http://www.s3stat.com/
 [2]: http://blog.lotas-smartman.net/archive/2008/02/29/image-site-stats.aspx