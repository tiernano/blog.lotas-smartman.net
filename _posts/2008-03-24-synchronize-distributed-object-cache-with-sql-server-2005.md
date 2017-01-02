---
title: Synchronize distributed object cache with SQL Server 2005
author: admin
layout: post
permalink: /synchronize-distributed-object-cache-with-sql-server-2005/
dsq_thread_id:
  - 26015919
categories:
  - Uncategorized
---
<img src="http://images.lotas-smartman.net/image.ashx?id=11b3f8d1-6795-4b18-ba0e-4977fb3b9e31" align="right" /> Check out this article over at Alachisoft, showing you how to use [Distributed Object Cache with SQL server 2005][1]. I can see where this comes in very handy. 

Say&nbsp;you have 4 front end web servers, all connecting to 2 load balanced App Servers, which in turn talk to 2 clustered DB servers. Well, you don&#8217;t want to hit all three tiers when making a web request, so you use Caching on the App tier. That will cache the info from the DB, and use it for each request from the front end. But what if the requests are the same? Well, you would cache some on the front end, and only go to the App tier if required. 

My thinking behind this would be as follows:

Using the [Caching Application Block][2], set the front end to cache the data for a set amount of time (say a minute). I think there is an option to invalidate the cache, if your App layer tell it to.

The App layer should tell the front end to invalidate cache once it gets a notification from the DB that it has changed. for this you would use the NCache. 

Depending on what data is being sent back from the App Servers, and depending on how frequent it could change, you may not cache all Data on the front end. 

<div class="wlWriterSmartContent" id="0767317B-992E-4b12-91E0-4F059A8CECA8:b79a806c-a2af-4fc3-8c55-d99620383995" style="padding-right:0px;display:inline;padding-left:0px;padding-bottom:0px;margin:0px;padding-top:0px;">
  Technorati Tags: <a href="http://technorati.com/tags/caching" rel="tag">caching</a>, <a href="http://technorati.com/tags/SQL%202005" rel="tag">SQL 2005</a>, <a href="http://technorati.com/tags/NCache" rel="tag">NCache</a>, <a href="http://technorati.com/tags/Caching%20Application%20Block" rel="tag">Caching Application Block</a>, <a href="http://technorati.com/tags/.NET" rel="tag">.NET</a>, <a href="http://technorati.com/tags/programming" rel="tag">programming</a>
</div></p>

 [1]: http://alachisoft.com/articles/synchronize_cache_with_db.html
 [2]: http://msdn2.microsoft.com/en-us/library/aa480456.aspx