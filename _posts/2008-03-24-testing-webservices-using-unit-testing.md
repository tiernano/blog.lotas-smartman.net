---
title: Testing webservices using Unit Testing
author: admin
layout: post
permalink: /testing-webservices-using-unit-testing/
dsq_thread_id:
  - 26016099
  - 26016099
dsq_needs_sync:
  - 1
categories:
  - Uncategorized
---
While working on a little project, i found that i needed to do some web service testing. So, i found the WebMethod i wanted to test, right clicked it and then selected Create Unit Test. When i did this, i got the following as a comment where the WebService was instantiated:

<pre class="code"><span>backend</span> target = <span>new</span> <span>backend</span>(); <span>// TODO: Use [AspNetDevelopmentServer] and TryUrlRedirection() to auto launch and bind web service.</span></pre>

backend is the name of the webservice, and this [AspNetDevelopmentServer] confused me. So, after some reading, I found you have to add the following to your code, just below the&nbsp; [<span>TestMethod</span>()] section:

<pre class="code">[<span>AspNetDevelopmentServerAttribute</span>(<span>"MyServerName"</span>, <span>@"&lt;insertPathToWebSite&gt;"</span>, <span>"/WebSiteAddress"</span>)]</pre>

<pre class="code">You also need the following using statement:</pre>

<pre class="code"><span>using</span> Microsoft.VisualStudio.TestTools.UnitTesting.Web;</pre>

There is some more info on the MSDN about this under [Testing Web Services][1], and also [Testing Web Sites and Web Services in a Team Environment][2]. Handy stuff!

[update] I forgot one fairly important thing:

after you instantiate your webservice object, you need to call the following:

<pre class="code"><span>WebServiceHelper</span>.TryUrlRedirection(target, testContextInstance, <span>"WebServiceName"</span>);</pre>

This will tell Visual Studio to use the the ASP.NET test web server for testing. 

[<img alt="kick it on DotNetKicks.com" src="http://www.dotnetkicks.com/Services/Images/KickItImageGenerator.ashx?url=http://blog.lotas-smartman.net/archive/2007/08/04/testing-webservices-using-unit-testing.aspx" border="0" />][3] 

<div class="wlWriterSmartContent" id="0767317B-992E-4b12-91E0-4F059A8CECA8:32e05881-b913-4240-8d5d-52d14b4ebbad" style="padding-right:0px;display:inline;padding-left:0px;padding-bottom:0px;margin:0px;padding-top:0px;">
  Technorati Tags: <a href="http://technorati.com/tags/WebServices" rel="tag">WebServices</a>, <a href="http://technorati.com/tags/Testing" rel="tag">Testing</a>, <a href="http://technorati.com/tags/Unit%20Testing" rel="tag">Unit Testing</a>, <a href="http://technorati.com/tags/WebMethod" rel="tag">WebMethod</a>, <a href="http://technorati.com/tags/Visual%20Studio" rel="tag">Visual Studio</a>, <a href="http://technorati.com/tags/MSDN" rel="tag">MSDN</a>, <a href="http://technorati.com/tags/AspNetDevelopmentServerAttribute" rel="tag">AspNetDevelopmentServerAttribute</a>
</div>

<pre></pre></p>

 [1]: http://msdn2.microsoft.com/en-us/library/ms243399(vs.80).aspx
 [2]: http://msdn2.microsoft.com/en-us/library/ms243136(VS.80).aspx
 [3]: http://www.dotnetkicks.com/kick/?url=http://blog.lotas-smartman.net/archive/2007/08/04/testing-webservices-using-unit-testing.aspx