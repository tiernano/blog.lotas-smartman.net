---
title: more multithreading in ASP.NET
author: admin
layout: post
permalink: /more-multithreading-in-aspnet/
dsq_thread_id:
  - 26015578
categories:
  - Uncategorized
---
As a follow up post to <a class href="http://blog.lotas-smartman.net/archive/2007/02/19/multithreading-in-asp-net.aspx">last nights post on Multi threading ASP.NET</a> stuff, i found this <a class href="http://msdn.microsoft.com/msdnmag/issues/05/10/WickedCode/">post on MSDN</a>. The problem with last nights post is there is no call back to the client. So, if you have a process that goes off and does something, the client does not now when it is completed. the MSDN page goes into a bit more detail on how to do it. one task i now have is building it so the call back is done over <a class href="http://ajax.asp.net/">AJAX</a>. this would be very cool.