---
title: Running SVN + SSH on Windows Home Server
author: admin
layout: post
permalink: /running-svn-ssh-on-windows-home-server/
dsq_thread_id:
  - 
  - 
dsq_needs_sync:
  - 1
categories:
  - Uncategorized
---
I have been running a Windows Home Server for a couple of months now, and other than some small issues with hardware (one of the hard drives failed, but i lost nothing!) i have been very happy with the experiance. i have used it to stream music and video to my XBox 360, and AFAIK the PS3 can see it too. I have also used it to store my iTunes collection, and this works flawlessly. but now, there is a way to get it to act as an SVN server.

Coderhaus has a post showing you [how to setup SSH and SVN on your Home Server][1]. with SSH, you can securley access your SVN server from a remote connection, and only have port 22 open. there are quite a few steps on how to set it up, about 35 in total, but i think it would definatly be worth it. you also have the advantage of having your share replicated, so your nice and safe&#8230; but, if you want to be safer (say, your house burns down) you may want to look at [how i was backing up my SVN server using Mozy][2] that i wrote back in 2007. [update] added missing link&#8230; sorry.

 [1]: http://www.coderhaus.com/?p=8
 [2]: http://blog.lotas-smartman.net/subversion-server-windows-apache-and-backing-up/