---
title: Thinking about building a SAN
author: admin
layout: post
permalink: /thinking-about-building-a-san/
dsq_thread_id:
  - 32036309
  - 32036309
categories:
  - Uncategorized
tags:
  - Cache
  - SAN
  - USB
  - ZFS
  - ZIL
---
So, i have been thinking about building a [ZFS][1] powered [SAN][2], and today i started thinking about using USB keys and drives&#8230; Why? SATA controllers with more than 4 ports are not cheap!

So, the way i was thinking was as follows (If anyone knows about ZFS and SANs, tell me if this is completely off the wall!)

  * Buy a basic Board and Chip, some RAM and a couple of PCI Express or PCI USB controllers
  * Stick in 2 Western Digital Raptors (i have 2 Spare 74Gb 10k drives here) and use them for ZIL storage. Or split them so one is for ZIL, the other for Cache
  * attach some USB Drives to the machine. I was thinking 16 x 32Gb USB Keys, but realized i can get a 500Gb external drive that takes no external power for about the same price&#8230;

In theory, when writing and reading, the external drives would be slower than expected, but with the ZIL and Cache Drives, things should (in theory&#8230;) be faster&#8230; Any thoughs?

 [1]: http://en.wikipedia.org/wiki/ZFS
 [2]: http://en.wikipedia.org/wiki/Storage_area_network