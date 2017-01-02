---
title: 'RE: ASP.NET in 80386 assembly language'
author: admin
layout: post
permalink: /re-aspnet-in-80386-assembly-language/
categories:
  - Uncategorized
---
using assembly to make ASP.NET pages! found this a few days ago and forgot to ost it, but talk about muts. just proves pretty much anything can be done with the .NET Framework though. lots of extra languages you can use.

> Something new ( new?!&nbsp;<img alt hspace=0 src="http://www.msnhk2.com/messengerclub/limages/20031007170111.gif" align=baseline border=0> )&nbsp;for me today&#8230; 
> 
> *For the curious, here&#8217;s an .aspx page in assembly langauge:* 
> 
> <pre><em>&lt;%@ page language="Asm80386" %&gt;<br />&lt;%<br />Str:  DB "Testing...", 0<br /><br />  mov eax, -2<br />  cmp eax, 2<br />  jle Label1<br />  xor eax, eax<br />Label1:<br />  lea esi, Str<br />  push esi<br />  call "Response.Write(string)"<br />  pop esi<br />%&gt;<br />&lt;br&gt;EAX: &lt;%= eax %&gt;</em></pre>
> 
> via [[Mike][1]]
> 
> This is the first time for me to see this kind of **codes** in ASP.NET Programming. <img src="http://blog.lotas-smartman.net/wp-includes/images/smilies/icon_smile.gif" alt=":)" class="wp-smiley" /> 
> 
> <img src ="http://weblogs.asp.net/coltk/aggbug/106141.aspx" width = "1" height = "1" /></blockquote> 
> 
> *[Via [Feedster RSS Search Results for assembly asp.net][2]]*

 [1]: http://mikepope.com/blog/DisplayBlog.aspx?permalink=597
 [2]: http://weblogs.asp.net/coltk/archive/2004/04/02/106141.aspx