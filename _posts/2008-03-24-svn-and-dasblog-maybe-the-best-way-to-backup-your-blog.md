---
title: 'SVN and DasBlog: maybe the best way to backup your blog'
author: admin
layout: post
permalink: /svn-and-dasblog-maybe-the-best-way-to-backup-your-blog/
dsq_thread_id:
  - 26016268
categories:
  - Uncategorized
---
It just came to me in a dream: [SVN][1] and [DasBlog][2] should go very well together. I don&#8217;t mean for source code (though DasBlog is already living in SVN), but I mean content, the site, and config files. (by the way, dont ask why i was dreaming of DasBlog&#8230;)

Since everything is stored in XML files, including the content (comments and posts) my theory is that everything could easily be backed up&nbsp; to SVN, every couple of hours. I have already talked about [my SVN setup at home][3], including how it is backed up regularly, so it would tie in here very easily. 

My theory goes as follows:

  * On the server, install the SVN client, and add your DasBlog directory to your SVN repository. 
  * commit everything, which will be your first commit. because everything is being added, it may take some time&#8230;.
  * add a batch script to your scheduled tasks which adds anything in your content folder (recursively) to SVN and then checks in. using the svn argument -m or &#8211;message, you can add your message to the checkin&nbsp;automatically (maybe something like checking in blog automatically for %insertdatehere%)
  * that&#8217;s it. everything commits, and your SVN server is set to backup every x hours (mine is done every 2 hours I think). 

this will be one of the first things I need to implement once the blog is operational. if anything changes, I will post it here!

<div class="wlWriterSmartContent" id="0767317B-992E-4b12-91E0-4F059A8CECA8:16950ca4-4881-4af9-ace5-014cf3e2c17d" contenteditable="false" style="padding-right: 0px; display: inline; padding-left: 0px; padding-bottom: 0px; margin: 0px; padding-top: 0px">
  Technorati Tags: <a href="http://technorati.com/tags/DasBlog" rel="tag">DasBlog</a>, <a href="http://technorati.com/tags/SVN" rel="tag">SVN</a>, <a href="http://technorati.com/tags/Backup" rel="tag">Backup</a>, <a href="http://technorati.com/tags/Blogging" rel="tag">Blogging</a>
</div></p>

 [1]: http://subversion.tigris.org/
 [2]: http://www.dasblog.info/
 [3]: http://blog.lotas-smartman.net/archive/2007/08/10/subversion-server-windows-apache-and-backing-up.aspx