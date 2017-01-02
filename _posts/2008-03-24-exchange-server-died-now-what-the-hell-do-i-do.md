---
title: Exchange server died, now what the hell do i do?
author: admin
layout: post
permalink: /exchange-server-died-now-what-the-hell-do-i-do/
dsq_thread_id:
  - 26012417
  - 26012417
dsq_needs_sync:
  - 1
categories:
  - Uncategorized
---
Well, arse! My&nbsp;Exchange 2003 server has just died. I dont know why, it could be memory, hard drive, or a mixture of the both. i took it down this morning, for a memory check. I bought a 512mb ddr dimm and it wasent working in the workstation, so i wanted to see if it was the memory or my board. well, its not my board. the memory caused the server to crash. so the ram that was in the server, again a 512mb ddr dimm, was tested in the workstation, and everything works grand over there. but when i took it back out and put it in the server again, the machine keeps comming up with fatial errors. and then a BlueScreenOfDeath! system totally dead. if i try boot into safe mode, it reboots with out getting anywhere. So, im screwed. and i dont meen that in a good way either. 

Due to me being lazy, i havent had a good backup of that system since, well, ever. i am still reading [the book][1] that tells me how to do a backup, but its written for Exchange 2000, and assumes you have tape backup and stuff. Actually it assumes i have more then one hard drive in the system, and some sort of raid setup, and also assumes i know what im doing!

So, under normal circumstances, i would just give up and reformat the system. but for now, i think i want to cheet. i will try and take the hard drive out of the server, put it into the workstation, try and copy the files i want to backup from the server on to the workstation, and burn them to DVD, then format the server hard drive, install Windows 2003 Server, Exchange 2003 and ISA 2004, and hope that everything works.once thats done, then try and rebuild the mail i have lost, which i reckon to be in the region of about quarter of a million emails, or so. yea, i know! i get LOTS of email. so, i better start this soon. now, where is my backup mail server&#8230;

 [1]: http://lsnbackup.blogspot.com/2005/02/exchange-2000-server-onsite-book.html