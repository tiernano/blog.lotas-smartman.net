---
title: 'ZFS, Amazon S3, CloudFiles, and a bit of automation&#8230;'
author: admin
layout: post
permalink: /zfs-amazon-s3-cloudfiles-and-a-bit-of-automation/
dsq_thread_id:
  - 26375342
  - 26375342
dsq_needs_sync:
  - 1
  - 1
categories:
  - Uncategorized
tags:
  - CloudFiles
  - photography
  - S3
  - Storage
  - ZFS
---
A while back i talked about a [company called Diomede][1] who had a new way of storing data… i wont go into too much detail here (check the old post) but basically they offered 3 ways of storing your data: online, near line and offline… online accessible instantly, near line available within 5 min of requesting it and offline within 4 hours…

this got me thinking, and again i mention a lot of stuff in the post, but now after playing with [ZFS][2] for a bit, i have been thinking a lot more about it… and i am going to explain this here explaining it using a photography workflow.

  * Photos are taken and stored on CF Cards. 
  * they are ingested into the main workstation on to a RAID 1 array for tagging and processing. this is online storage.
  * next they are transferred to my ZFS Server (which at the moment i don&#8217;t have, but am thinking about…). this is nearline storage, but with [GigE][3] and fast disks, this is nearly as fast as the RAID 1 array… the Online and Near Line storage arrays should be pretty much in sync with each other… any changes must be replicated.
  * nightly there is a ZFS snapshot taken (incremental) and uploaded to [Amazon S3][4] or [CloudFiles][5]… if very little has changed, this will be a quick upload. if there has been a lot of photos uploaded, then, well its going to take a while. S3 and CloudFiles are the Offline storage. 
  * finally, monthly a full ZFS snapshot should be uploaded.&#160; 

The biggest problem with this whole thing is bandwidth and i have said this multiple times before… in reality, you could use some sort of compression, but in a quick test with 32 files, 16 [CR2][6] files from my [Canon EOS 5D MK II][7], and 16 [XMP][8] side cars weighing in at a total of 384Mb, saved me 12mb using [Winzip][9] 12… its about 3% smaller… on a 113 hour upload, it would save you about 3 hours, but its not a great saving… 

Anyway, i have the hardware pretty much here… a couple of 1Tb hdds, and some smaller disks also… Mobo, Ram, Proc, etc. once i build this (first have to get my Home Server data off the drives…) i will start posting info.

 [1]: http://blog.lotas-smartman.net/online-nearline-and-offline-storage-offering-cheaply
 [2]: http://en.wikipedia.org/wiki/ZFS
 [3]: http://en.wikipedia.org/wiki/Gigabit_Ethernet
 [4]: http://www.amazon.com/s3
 [5]: http://www.rackspacecloud.com/cloud_hosting_products/files
 [6]: http://en.wikipedia.org/wiki/.CR2_file_format
 [7]: http://www.dpreview.com/news/0809/08091705canon_5dmarkII.asp
 [8]: http://www.adobe.com/products/xmp/
 [9]: http://www.winzip.com