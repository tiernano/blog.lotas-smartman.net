---
title: Subversion Server, Windows, Apache and Backing up
author: admin
layout: post
permalink: /subversion-server-windows-apache-and-backing-up/
dsq_thread_id:
  - 26016122
  - 26016122
dsq_needs_sync:
  - 1
categories:
  - Uncategorized
---
Since my Opteron is not 100% operational, I have not got my TFS server running. So, I am currently using Subversion. But since there are 3 things that are definite in this world (Death, Taxes and Hard drive failures) I need a backup solution. And I have found it. In this post over at Spears.at, the author has info on [setting up a SVN server][1]. but in section 4.1 and 4.2, they talk about how to backup your SVN repository. This is very cool.

I am currently doing the following for backups of the SVN system:

every 6 hours, a full dump is taken of the SVN box. this is BZ2 compressed, and copied to 2 external hard drives (3 copies exist in total).

then, an incremental dump is taken. using the script on the site above, it only dumps the newest revisions from the last one (say, 6 hours ago it backed up 149, and I check in 3 new revs, bringing it to 152, it would only backup 150, 151 and 152). this is dropped into a directory, and also copied to the 2 external drives. 

Now, what happens if all drives die? Simple: Online backup. I have [Mozy][2] watching the directory with the small revisions (mind you, all 150 in my case are in there) and it only sends what has changed. since this started Wednesday night, it had to send 400+Mb to the server, but the changes I made last night only mean I sent 3mb.

This is very cool, and because I am backed up in 4 places in total, one of which is off site, I am very happy.

In reality, I could add more, by compressing the latest revision and pushing it to S3. or a external server somewhere, but Mozy seem very secure, so I am happy with them!

[Full Disclosure: Yes, I am a Mozy affiliate, and make money if you sign up, which is free by the way for 2Gb storage, but, even if I wasn&#8217;t making money, still happy with their service!]</p> 

<div class="wlWriterSmartContent" id="0767317B-992E-4b12-91E0-4F059A8CECA8:04937b84-922a-4bdb-bdbc-9700e876e2f3" style="padding-right:0px;display:inline;padding-left:0px;padding-bottom:0px;margin:0px;padding-top:0px;">
  Technorati Tags: <a href="http://technorati.com/tags/Mozy" rel="tag">Mozy</a>, <a href="http://technorati.com/tags/Backup" rel="tag">Backup</a>, <a href="http://technorati.com/tags/SVN" rel="tag">SVN</a>, <a href="http://technorati.com/tags/TFS" rel="tag">TFS</a>, <a href="http://technorati.com/tags/Hard%20Drives" rel="tag">Hard Drives</a>
</div>

 [1]: http://svn.spears.at/
 [2]: http://www.mozy.com/?ref=3f9a896b&kbid=31440&m=4&i=59