---
title: RSync and Amazon S3
author: admin
layout: post
permalink: /rsync-and-amazon-s3/
dsq_thread_id:
  - 26016547
  - 26016547
dsq_needs_sync:
  - 1
categories:
  - Uncategorized
---
So, over the last week, I have been backing up my photos to Amazon S3 using [S3Backup][1]. The problems with S3Backup are 1: its not easily scriptable (I can kick off a backup job, but I cant say just backup this directory&#8230;) 2: it syncs Whole file changes. So, I make a small touch up to a photo, which, on disk only changes a few bytes (working a lot of [DNG][2] files), S3Back will upload the whole 8mb+ file&#8230; and finally, its only relatively stable&#8230; Its crashed a few times. 

So, it got me thinking: there must be an easier way. I found a post over at &#8220;Clic!Dev, &#8216;Tate and many more projects!&#8221; (what a name for a blog!)&nbsp; which talks about [Cheap Server Backup with Amazon S3][3]. In the tutorial, they use RSync. they use a Linux box for running the RSync server, and I don&#8217;t have one. all my machines are running various versions of Windows&#8230; I suppose I could run it in a Virtual Machine, but things gets complicated if the machine reboots&#8230; 

Anyway, after a bit more looking I found [S3RSync][4]. Its a service which has some [Amazon EC2][5] machines running, and you connect to them, which in turn connects to S3 and backs up your data. probably in a similar manner as the first option&#8230; I have requested more info, but as of yet have heard nothing. not sure which way they charge for usage either&#8230; once I get more info I will post it. 

finally, for future reference, check out this article over at Gaztronics.net, explaining how to setup and use [RSync on Windows][6]. they go into detail on setting up Windows as both the Client and Server, and setting up a Linux server also. Pretty handy stuff.

 [1]: http://s3bk.com/
 [2]: http://www.adobe.com/dng
 [3]: http://nexus.zteo.com/2007/08/06/cheap-server-backup-with-amazon-s3/
 [4]: http://www.s3rsync.com
 [5]: http://www.amazon.com/ec2
 [6]: http://www.gaztronics.net/rsync.php