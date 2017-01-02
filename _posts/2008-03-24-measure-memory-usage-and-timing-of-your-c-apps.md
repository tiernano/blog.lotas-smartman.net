---
title: 'Measure memory usage and timing of your C# app&#039;s'
author: admin
layout: post
permalink: /measure-memory-usage-and-timing-of-your-c-apps/
dsq_thread_id:
  - 26016346
dsq_needs_sync:
  - 1
categories:
  - Uncategorized
---
I need to look into working out how much memory certain tasks use, and how much time they take to complete. I also have to work out min and max memory usage, min and max processor load, as well as average processor load.

Well, I found the first part: Tobi + C# = T# has a post talking about [Memory and Timing tests][1]. Well, the main focus of that post is memory, and the timing post is [here][2]. 

The MSDN also has quite a large document on [measuring .NET app performance][3], part of the &#8220;*[Improving .NET Application Performance and Scalability][4]*&#8221; guide, and that has a lot of interesting stuff. only thing is that this should be as programmable as possible: I want to be able to log all the data somewhere so I can chart it in Excel, give info about what&#8217;s going, etc.

 [1]: http://saftsack.fs.uni-bayreuth.de/~dun3/archives/measure-memory-consumption-creating-object-functions/102.html
 [2]: http://saftsack.fs.uni-bayreuth.de/~dun3/archives/more-accurate-timing-stopwatch-performancetimer-queryperformancecounter/19.html
 [3]: http://msdn2.microsoft.com/en-us/library/ms998579.aspx
 [4]: http://msdn2.microsoft.com/en-us/library/ms998530.aspx