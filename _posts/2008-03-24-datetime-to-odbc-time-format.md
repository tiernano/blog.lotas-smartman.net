---
title: DateTime to ODBC time format
author: admin
layout: post
permalink: /datetime-to-odbc-time-format/
dsq_thread_id:
  - 26012428
categories:
  - Uncategorized
---
I found this tip over at Brad [Abrams Blog here][1].

Want a datetime in this format?<?xml:namespace prefix = o /><o:p></o:p></defanged-SPAN><p class=MsoNormal><defanged-SPAN style="FONT-SIZE: 10pt; FONT-FAMILY: 'Courier New'">2004-06-21T11:29:01.9346744-08:00 <o:p></o:p></defanged-SPAN></p> <p class=MsoNormal><defanged-SPAN style="FONT-SIZE: 10pt; FONT-FAMILY: Arial">In .NET Framework 2.0: </defanged-SPAN><defanged-SPAN style="FONT-SIZE: 10pt; FONT-FAMILY: 'Courier New'">DateTime.ToString(&#8220;o&#8221;) ;</defanged-SPAN><defanged-SPAN style="FONT-SIZE: 10pt; FONT-FAMILY: Arial"><o:p></o:p></defanged-SPAN></p> <p class=MsoNormal><defanged-SPAN style="FONT-SIZE: 10pt; FONT-FAMILY: Arial">In .NET Framework 1.0\1.1: </defanged-SPAN><defanged-SPAN style="FONT-SIZE: 10pt; FONT-FAMILY: 'Courier New'">DateTime.ToString(&#8220;yyyy-MM-ddTHH:mm:ss.fffffffzzz&#8221;);</p> <p class=MsoNormal>Very handy tip that. </defanged-SPAN></p>

 [1]: http://blogs.msdn.com/brada/archive/2005/02/07/368848.aspx