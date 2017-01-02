---
title: Zero based Arrays
author: admin
layout: post
permalink: /zero-based-arrays/
dsq_thread_id:
  - 26007678
categories:
  - Uncategorized
---
just watching a Video on how to upgrade from VB6 to VB.NET. It was on the MSDN January 2004 DVD, so i cant give a direct link. But he was talking about [Zero Based Arrays][1]. Basicly, you cant start counting at anything other then zero in an array. so if you have code like:

for i =&nbsp;1 to 10

you would have:

for i = 0 to 9

in VB.net. this is because of being based on .NET and being compatible with C# and the rest of them. so, thats the first thing i have learned. also, that upgrade wizard is pretty handy, but it broke a few of my VB6 Apps.

 [1]: http://msdn.microsoft.com/library/default.asp?url=/library/en-us/vbcon/html/vbconupgraderecommendationusezero-boundarrays.asp