---
title: Community Server to DasBlog Migration
author: admin
layout: post
permalink: /community-server-to-dasblog-migration/
dsq_thread_id:
  - 26016261
dsq_needs_sync:
  - 1
categories:
  - Uncategorized
---
So, last night I talked about my work on Migrating the blog to DasBlog. I also mentioned I would post info about how I was going about doing this. Well, this is the post.

First, I have to get my data out of Community Server and into a format that DasBlog can read. there are 3 steps I have done for this:

  1. remove all comment spam from my blog. I get quite a lot, 99.9% of which is not published, but is kept in the DB (I have 1 or 2 false positives). so my first task is clear the DB of these comments. some 15000 where removed in the last couple of hours while trying this
  2. next, I migrate the blog posts, comments and categories/tags to [BlogML][1]. This is a XML format for storing your the content of your entire blog in. this allows easy migration from one blog to another. To do so, I used Keyvan Nayyeri&#8217;s [Community Server 2007 BlogML converter][2]. this allows me to export all my data easily.
  3. Finally, I import the data into DasBlog, which is quite simple too. I uses [Tam Tam Weblogs DasBlog BlogML importer][3] for this. This works great.

Now, in between part 2 and 3, there should be a 2a. I have noticed that there are spaces before and after the category names in the BlogML that is generated. this is causing a problem with the import, and when you click a category link, the URL returns a 400 error message. So, I have to preprocess the BlogML before importing into DasBlog. 

So far, so good. one or two little tweaks to the URL rewriting section, as I mentioned, and I will hopefully have everything working. I will post more as time goes on.

<div class="wlWriterSmartContent" id="0767317B-992E-4b12-91E0-4F059A8CECA8:2cfdd510-cf9e-4c39-b344-5d05e3ec2bcd" contenteditable="false" style="padding-right: 0px; display: inline; padding-left: 0px; padding-bottom: 0px; margin: 0px; padding-top: 0px">
  Technorati Tags: <a href="http://technorati.com/tags/DasBlog" rel="tag">DasBlog</a>, <a href="http://technorati.com/tags/Community%20Server" rel="tag">Community Server</a>, <a href="http://technorati.com/tags/BlogML" rel="tag">BlogML</a>, <a href="http://technorati.com/tags/Importing" rel="tag">Importing</a>, <a href="http://technorati.com/tags/Exporting" rel="tag">Exporting</a>
</div></p>

 [1]: http://blogml.org/
 [2]: http://nayyeri.net/archive/2007/05/29/community-server-2007-blogml-converter.aspx
 [3]: http://blogs.tamtam.nl/paulb/2007/08/14/dasBlogBlogMLImporter.aspx