---
title: Jungle Disk Server
author: admin
layout: post
permalink: /jungle-disk-server/
dsq_thread_id:
  - 38970061
  - 38970061
dsq_needs_sync:
  - 1
categories:
  - Uncategorized
tags:
  - Backup
  - Jungle Disk
  - Jungle Disk Server
  - MySQL
  - Server
  - SQL
  - SVN
  - Ubuntu
  - wordpress
---
A Few days ago on the Jungle Disk blog, it was announced they would be releasing a BETA of their new product: [Jungle Disk Server][1]. This sounded very interesting, and one of the more interesting features that was added was De-Duplication&#8230;. let me try explain with a bit of detail&#8230;

I am backing up my SVN server. I have 2 scheduled tasks: every 15 min, take the latest revesions that where not previously backed up and dump them to a file&#8230; then weekly, take a full backup. i ran this on a folder with 13 full backups (about 730mb a piece, totaling about 9Gb) and 31 smaller backups, averaging about a meg and a half&#8230; there is a LOT of duplicated data here: every full backup is the equivilant of the last weeks full backup and the smaller 15min backups&#8230; and it goes on. De-Duplication looks at all the blocks, and figures out of they have already been backed up&#8230; If so, it wont back it up again, put puts a pointer to that block in the backup db&#8230;

So, we say the last full backup is 750mb&#8230; that shold be all that is needed&#8230; Jungle Disks first backup of this server found 8.45Gb and uploaded 149mb! Thats it! there is compression going on there also, but that is pretty impressive! A Full backup has been run since then, and it brough the total file size to 9.17Gb, and the upload was 4.47mb! Very, VERY Cool!

So, at the moment, i have it backing up my SQL server, my Ubuntu server (where the blogs live, both the WordPress dirs and the MySQL server itself) and also my SVN Box. So far so good! Check if out.

 [1]: http://blog.jungledisk.com/2009/10/06/jungle-disk-server-edition-free-public-beta/