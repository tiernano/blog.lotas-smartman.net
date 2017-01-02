---
title: Email2HTTP in ASP.NET
author: admin
layout: post
permalink: /email2http-in-aspnet/
dsq_thread_id:
  - 26016422
dsq_needs_sync:
  - 1
categories:
  - Uncategorized
---
Right, so here is some sample code and tutorial to get [Email2HTTP][1] to work with ASP.NET. Its extremely simple:

First, sign up for an account at [Email2HTTP.com][1]. Once you have your account, set up a domain or use the sample on they give you when you sign up:

<img src="http://images.lotas-smartman.net/image.ashx?id=916b9f29-1794-4949-b755-b9fa62d8ffb9" mce_src="http://images.lotas-smartman.net/image.ashx?id=916b9f29-1794-4949-b755-b9fa62d8ffb9"> 

Once your domain is setup (I used the sample, so everything, including MX records and DNS was already setup. if you are using a different one, you will need to follow the instructions) you need to add a Target URL. this is where email gets redirected to. 

<img src="http://images.lotas-smartman.net/image.ashx?id=9fe0e5a0-9c1f-4a2c-a9af-6f4e67b92d9a" mce_src="http://images.lotas-smartman.net/image.ashx?id=9fe0e5a0-9c1f-4a2c-a9af-6f4e67b92d9a"> <p mce_keep="true">&nbsp;</p> 

Name your target and add the URL you want to receive the email. next, we you are going to want to write the code.

Here is a VERY SIMPLE example I have built. I built it in a ASP.NET handler page (ASHX). this just made my life a little easer.

public void ProcessRequest (HttpContext context) {  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; string subject = &#8220;&#8221;;  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; string body = &#8220;&#8221;;  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; context.Response.Write(context.Request.Form.Keys.Count);  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; context.Response.Write(&#8220;<br>&#8221;);  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; subject = context.Request.Form.Get(&#8220;subject&#8221;);  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; body = context.Request.Form.Get(&#8220;body&#8221;);  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; context.Response.Write(s);  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; context.Response.Write(&#8220;<br>&#8221;);  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; context.Response.Write(&#8220;Body: &#8221; + body);  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; context.Response.Write(&#8220;<br>&#8221;);  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; context.Response.Write(&#8220;Subject: &#8221; + subject);  
&nbsp;&nbsp; }<p mce_keep="true">&nbsp;</p> 

Anything that is written back gets emailed back to the user. So, if you emailed, say a stock symbol, you could call a web service, get some information and send it back to the user via email. 

This is very cool! Couple of things that would be nice: instead of calling the webserver directly with all the posted data, which is done now and could be &#8220;spoofed&#8221;, call the webserver and post a key, which could be used then by the server to call the service and get the information. this could also be handy for servers which are inside a network: they could poll the service every, say, 5 minutes and pull information down. It would not be real time, but it would allow &#8220;hidden&#8221; servers to use the service.

[<img alt="kick it on DotNetKicks.com" src="http://www.dotnetkicks.com/Services/Images/KickItImageGenerator.ashx?url=http%3a%2f%2fblog.lotas-smartman.net%2farchive%2f2008%2f02%2f11%2femail2http-in-asp-net.aspx" border=0>][2]

 [1]: http://www.email2http.com/
 [2]: http://www.dotnetkicks.com/kick/?url=http%3a%2f%2fblog.lotas-smartman.net%2farchive%2f2008%2f02%2f11%2femail2http-in-asp-net.aspx