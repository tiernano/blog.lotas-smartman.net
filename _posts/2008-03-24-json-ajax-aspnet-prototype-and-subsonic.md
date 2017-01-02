---
title: JSON, AJax, ASP.NET, Prototype and SubSonic
author: admin
layout: post
permalink: /json-ajax-aspnet-prototype-and-subsonic/
dsq_thread_id:
  - 26016060
  - 26016060
categories:
  - Uncategorized
---
Over the last few days, I have been working on something with a mixture of [ASP.NET][1], [JSON][2], [SubSonic][3], [Ajax][4] and [Prototype][5]. the way everything is done is fairly simple, but also a bit all over the shop. mind you, I&#8217;m learning, and I&#8217;m happy with the results.

I have an ASHX file written in C#, which uses SubSonic to query a SQL DB.

Subsonic returns a list of objects, which I then convert to a JSON string using [Json.NET][6]. this is then returned to the user.

the front end is a very simple HTML file, which includes Prototype. it calls the ASHX pages, getting back the JSON objects, parses them, and then displays them to the user. Very cool stuff!

Only doing this as a test, and demo, but lets hope I can get it working on something else! <img src="http://blog.lotas-smartman.net/wp-includes/images/smilies/icon_smile.gif" alt=":)" class="wp-smiley" />

<div class="wlWriterSmartContent" id="scid:0767317B-992E-4b12-91E0-4F059A8CECA8:aae2e690-0d5b-41b3-8687-3c329b184d2a" style="padding-right:0px;display:inline;padding-left:0px;padding-bottom:0px;margin:0px;padding-top:0px;">
  Technorati Tags: <a href="http://technorati.com/tags/JSON" rel="tag">JSON</a>, <a href="http://technorati.com/tags/AJax" rel="tag">AJax</a>, <a href="http://technorati.com/tags/ASP.NET" rel="tag">ASP.NET</a>, <a href="http://technorati.com/tags/ProtoType" rel="tag">ProtoType</a>, <a href="http://technorati.com/tags/Subsonic" rel="tag">Subsonic</a>, <a href="http://technorati.com/tags/ASHX" rel="tag">ASHX</a>, <a href="http://technorati.com/tags/Programming" rel="tag">Programming</a>
</div>

 [1]: http://www.asp.net/
 [2]: http://www.json.org/
 [3]: http://www.codeplex.com/actionpack
 [4]: http://en.wikipedia.org/wiki/AJAX
 [5]: http://www.prototypejs.org/
 [6]: http://www.newtonsoft.com/products/json/