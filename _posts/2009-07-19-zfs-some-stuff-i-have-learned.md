---
title: 'ZFS: some stuff i have learned'
author: admin
layout: post
permalink: /zfs-some-stuff-i-have-learned/
dsq_thread_id:
  - 26109546
  - 26109546
categories:
  - Uncategorized
tags:
  - Amazon S3
  - Backup
  - iSCSI
  - SVN
  - TimeMachine
  - VMWare
  - ZFS
---
Ok, this is more of a Random Post than anything else, but here goes nothing…

I have been playing with [ZFS][1] for the last couple of weeks, under a [VMWare][2] VM with a copy of [Nexenta Core][3] and i am quite impressed.

Some things i have learned to do and how they work below:

  * some basics on creating ZFS pools: [Part 1][4] and [Part 2][5]. very handy stuff. even shows how to break and fix pools! Very cool! 
  * [ZFS and ISCSI][6]. the big thing this shows is backing up OSX to ZFS using time machine, but [@harryd71][7] says in [this tweet that iSCSI cant be used to restore][8]… you would need to reinstall your OS then recover files manually… 
  * Constantin’s Blooog (not a miss type, its actually called that!) has a tip to [get faster iSCSI performance out of Windows][9]. Not sure if this works yet… my perf is about 25mb/s from iSCSI and the same from SMB, and the VM is using the same drives… if i move to a separate machine, we se what happens then. 
  * 2 posts on getting ZFS snapshots backed up to Amazon S3: one for [EC2 based machines][10], but could work with all… and one [including Encryption][11]. This is a very cool idea. only problem is i have a LOT of data i would like backed up: about 80+ Gig of photos, growing more and more each month… couple Gig of SVN archives, few more Gig of DB and website backups&#160; and more… need more upload bandwidth for this to work quickly enough… 
  * Constantin’s Blooog has a post on using [ZFS with USB Disks][12]. He also has [tips for ZFS starters][13] and a script for [Replicating ZFS Snapshots][14]… 
  * Last, but not least, Don MacAskill from [Smugmug][15] has a [section dedicated to ZFS on his blog][16]. Very cool stuff here. 

So, thats pretty much it. i will leave you with this (click to see the full size)

[<img style="border-right-width: 0px; display: inline; border-top-width: 0px; border-bottom-width: 0px; border-left-width: 0px" title="vsan-zpool-status" border="0" alt="vsan-zpool-status" src="http://blog.lotas-smartman.net/wp-content/uploads/2009/07/vsanzpoolstatus_thumb.png" width="244" height="120" />][17]

this is the status of my mini SAN here… not doing a lot, but those disks are all 16Gb, in RAID 6 (ZRAID2). and its nice and fast!

 [1]: http://en.wikipedia.org/wiki/ZFS
 [2]: http://www.vmware.com
 [3]: http://www.nexenta.org/os
 [4]: http://flux.org.uk/howto/solaris/zfs_tutorial_01
 [5]: http://flux.org.uk/howto/solaris/zfs_tutorial_02
 [6]: http://www.opensolaris.org/os/project/qosug/how-tos/zfs_iscsi_integration/
 [7]: http://twitter.com/harryd71
 [8]: http://twitter.com/harryd71/status/2602656030
 [9]: http://blogs.sun.com/constantin/entry/x4500_solaris_zfs_iscsi_perfect
 [10]: http://blogs.sun.com/ec2/entry/zfs_snapshots_to_and_from
 [11]: http://kenai.com/projects/zfs-backup-to-s3/pages/Home
 [12]: http://blogs.sun.com/constantin/entry/opensolaris_home_server_zfs_and
 [13]: http://blogs.sun.com/constantin/entry/7_easy_tips_for_zfs
 [14]: http://blogs.sun.com/constantin/entry/useful_zfs_snapshot_replicator_script
 [15]: http://www.smugmug.com
 [16]: http://blogs.smugmug.com/don/tag/zfs/
 [17]: http://blog.lotas-smartman.net/wp-content/uploads/2009/07/vsanzpoolstatus.png