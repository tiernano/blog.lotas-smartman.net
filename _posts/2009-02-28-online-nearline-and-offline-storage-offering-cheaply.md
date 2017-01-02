---
title: Online, NearLine and OffLine storage offering cheaply
author: admin
layout: post
permalink: /online-nearline-and-offline-storage-offering-cheaply/
dsq_thread_id:
  - 
  - 
dsq_needs_sync:
  - 1
categories:
  - Uncategorized
---
Found this post over at TechCrunch about a company called [Diomede who are offering green file storage][1]. there offer you three ways of storing your data and differing prices:

  * Online: Immediate access, like any cloud storage provider at the moment, at a cost of about $0.05 per gig, which is very cheap also.
  * NearLine: available within 5 min of requesting the data. costs about 4.5c per Gig.
  * OffLine: available within 4 hours of requesting. costs only 2c per gig.

this started to make me think about my cloud data usage. I currently have about 110gb stored in the cloud ([Amazon S3][2]), mostly photos i have taken and backed up, backups of my SVN server and also images hosted on my Images site. they are stored between the US and EU (planning on moving just to hosting in the EU, but never got around to it fully). The images for the image hosting site are required immediatly, but the backups are not as important&#8230; i dont think waiting 4 hours would be an issue if i needed to download my 50gb or so of photos. Sure, its going to take at least that amount of time to download it, and it would probably be done over night anyway&#8230;

It has started making me think about storage needs though. and my thinking behind it is that even as a home user, 3 levels of stoage is nearly now a necessity. by 3 levels i mean Online, NearLine and OffLine. but not in the same way as above:

  * Online: stuff on your C Drive, or in your local machine. important content should be in RAID 1, not so important should be just on standard disks and temporary stuff, or least important could be on RAID 0.
  * Nearline: [Windows Home Server][3] would be great for this. this is what i use. My videos, ISO Images (from MSDN, etc) and Photos are all stored here.
  * OffLine: really, this is online, but i concider this offline in that its not in the house. This is stuff stored "in the cloud", like Amazon. not there immediatly, but can be there soon enough.

the biggest problem with "offline storage" is upstream bandwidth. I have 2 lines into the house, one running at 1.5mb up and the other at just 1. to upload 50gb, it would take about 75 horus, non stop on the 1.5Mb line and 113 on the 1mb line&#8230; yea, i could split the lines and use all bandwidth, but most people dont have that kind of option. ideally, some sort of faster uplink to the storage providers would be handy, or having the ISP giving you a dedicated line direct to the stoage provider.[NTL/UPC][4], my cable modem provider, have a modem which has both data and phone. based on what i think is going on, there are 2 seperate connections to their network going on here: one just for VOIP and one just for data&#8230; If you could add a third just for stoage (SAN or NAS type solution) it would be very cool&#8230; and something i would pay for if i 1) dident use my internet bandwidth for it and 2) had a very fast connection to it&#8230; just a thought&#8230;

 [1]: http://www.techcrunch.com/2009/02/27/diomede-offers-green-file-storage-in-the-cloud-for-a-fraction-of-the-cost/
 [2]: http://www.amazon.com/s3
 [3]: http://www.microsoft.com/windows/products/winfamily/windowshomeserver/default.mspx
 [4]: http://www.upc.ie