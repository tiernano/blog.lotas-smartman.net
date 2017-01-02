---
title: Rails Conf, Scribd, Scaling rails and custom traffic analysis
author: admin
layout: post
permalink: /rails-conf-scribd-scaling-rails-and-custom-traffic-analysis/
dsq_thread_id:
  - 26015845
dsq_needs_sync:
  - 1
categories:
  - Uncategorized
---
A while back i found this article over at O&#8217;Reilly Radar about the <a class href="http://radar.oreilly.com/archives/2007/05/first_day_at_ra.html">first day of Rails Conf</a>. Since i am a geek and im interested in Scaling web applications (cause you never know&#8230;) I started reading the <a class href="http://www.scribd.com/doc/49575/Scaling-Rails-Presentation">Scribd Scalling Rails Presentation</a>. Its a good presentation, and its not just handy for Rails users. the idea of Fragment Caching is very cool. But, back to the original idea of the post: custom traffic analysis. This is quite a cool idea. In the presentation, they show some code on what the DB should look like. So, i wrote some code, in C# of course, to use this DB and build my own traffic analysis section to a site i am building. here is some of that code:

&nbsp;

<pre class="code"><span>public</span> Counter(<span>HttpRequest</span> req)
        {
            bl = <span>new</span> <span>BLL</span>();
            <span>string</span> referer = <span>""</span>;
            <span>if</span> (req.UrlReferrer != <span>null</span>)
            {
                referer = req.UrlReferrer.AbsoluteUri;
            }
            bl.PageView(req.Url.AbsoluteUri, req.AnonymousID, req.UserHostAddress, referer, req.UserAgent, <span>DateTime</span>.Now);
        }</pre>

[][1]

&nbsp;

The idea is that on each page you want to count, you would use the following code:

<font color="#2b91af" size="2"></p> 

<p>
  Counter</font><font size="2"> c = </font><font color="#0000ff" size="2">new</font><font size="2"> </font><font color="#2b91af" size="2">Counter</font><font size="2">(context.Request);</p> 
  
  <p>
    </font>
  </p>
  
  <p>
    well, not exactly that code. this was used in an ASHX file. normally it would be&nbsp;<font color="#2b91af" size="2"></p> 
    
    <p>
      Counter</font><font size="2"> c = </font><font color="#0000ff" size="2">new</font><font size="2"> </font><font color="#2b91af" size="2">Counter</font><font size="2">(Request);</font>
    </p>
    
    <p>
      <font size="2">the bl.pageview method only checks what is being entered. it makes sure anything that is being sent in is not null. then it just chucks it in the DB. the req.AnonymousID is the session ID, or at least i think it is. If I am wrong, which it has been known, please leave a comment. I will update the code accordingly&#8230; <img src="http://blog.lotas-smartman.net/wp-includes/images/smilies/icon_smile.gif" alt=":)" class="wp-smiley" /></font>
    </p>
    
    <p>
      <font size="2">[updated: using proper coloring for the code!]</font>
    </p>
    
    <div class="wlWriterSmartContent" id="0767317B-992E-4b12-91E0-4F059A8CECA8:21961437-d980-4925-94d4-b3d6cdab02af" style="padding-right:0px;display:inline;padding-left:0px;float:none;padding-bottom:0px;margin:0px;padding-top:0px;">
      Technorati Tags: <a href="http://technorati.com/tags/counter" rel="tag">counter</a>, <a href="http://technorati.com/tags/rails" rel="tag">rails</a>, <a href="http://technorati.com/tags/scribd" rel="tag">scribd</a>, <a href="http://technorati.com/tags/rails%20conf" rel="tag">rails conf</a>, <a href="http://technorati.com/tags/traffiic%20analysis" rel="tag">traffiic analysis</a>, <a href="http://technorati.com/tags/scaling" rel="tag">scaling</a>
    </div>

 [1]: http://11011.net/software/vspaste