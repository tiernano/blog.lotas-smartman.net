---
title: Backing up WordPress on Ubuntu to S3
author: admin
layout: post
permalink: /backing-up-wordpress-on-ubuntu-to-s3/
dsq_thread_id:
  - 33060362
  - 33060362
dsq_needs_sync:
  - 1
categories:
  - HowTo
tags:
  - Backup
  - MySQL
  - S3
  - Ubuntu
  - wordpress
---
Right… So, my blog is currently living on an [Ubuntu][1] box here in the house and is running 3 of my blogs (this one, [The Angry Viking][2] and [Tiernans Photography Blog][3]). With all the news about [WordPress being under attack][4], i though i better share some of my scripts i use for Backing up the sites…

  1. i am using [S3Sync][5] for the Upload to S3… 
  2. The code for the Script is available on [this Gist][6]. It was slightly modified (Removing my DB username and passwords, and only backing up one DB and Directory).
  3. I want this to run every night, but at the moment it is kicked off manually… 
  4. There should be a clean up part at the end deleting the uploaded file… Ideally the uploader should check if the upload file was finished before deleting also…

If there is anything anyone can see that could be changed, please leave a comment.

 [1]: http://www.ubuntu.org
 [2]: http://www.angryviking.net
 [3]: http://www.tiernanotoolephotography.com
 [4]: http://www.techcrunch.com/2009/09/05/security-threat-wordpress-under-attack/
 [5]: http://s3sync.net/wiki
 [6]: http://gist.github.com/182027