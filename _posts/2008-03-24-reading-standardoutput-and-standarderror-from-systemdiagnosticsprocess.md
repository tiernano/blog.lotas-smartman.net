---
title: reading StandardOutput and StandardError from System.Diagnostics.Process
author: admin
layout: post
permalink: /reading-standardoutput-and-standarderror-from-systemdiagnosticsprocess/
dsq_thread_id:
  - 26016380
  - 26016380
dsq_needs_sync:
  - 1
categories:
  - Uncategorized
---
Do, I have been working on some code that calls some external commands and works out some Timing around them. I mentioned this before, and the first part I worked on was [memory and CPU usage][1].

Well, my next task was to make sure the commands where running correctly, and trying to grab the output. Luckily enough, there is an option when creating your process, under [StartInfo][2] called [RedirectStandardOutput][3]. There is also [RedirectStandardError][4]. Both of these tell the process your starting to redirect the output to the [StandardOutput][5] and [StandardError][6] streams of the process, which can then be read from by your application.

Check out this post on [Joel.Net which has demo code][7], and more info.

 [1]: http://blog.lotas-smartman.net/archive/2007/12/14/measure-memory-usage-and-timing-of-your-c-app-s.aspx
 [2]: http://msdn2.microsoft.com/en-us/library/system.diagnostics.processstartinfo.aspx
 [3]: http://msdn2.microsoft.com/en-us/library/system.diagnostics.processstartinfo.redirectstandardoutput.aspx
 [4]: http://msdn2.microsoft.com/en-us/library/system.diagnostics.processstartinfo.redirectstandarderror.aspx
 [5]: http://msdn2.microsoft.com/en-us/library/system.diagnostics.process.standardoutput.aspx
 [6]: http://msdn2.microsoft.com/en-us/library/system.diagnostics.process.standarderror.aspx
 [7]: http://joel.net/me/weblog.aspx?weblogs_show=06fa16b4-cbdd-415d-8996-529763ab0534