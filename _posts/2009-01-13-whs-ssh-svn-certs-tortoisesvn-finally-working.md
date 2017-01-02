---
title: WHS + SSH + SVN + Certs + TortoiseSVN = Finally working!
author: admin
layout: post
permalink: /whs-ssh-svn-certs-tortoisesvn-finally-working/
dsq_thread_id:
  - 26003707
  - 26003707
dsq_needs_sync:
  - 1
categories:
  - HowTo
---
yesterday I posted about [how to get Windows Home Server to act as a SVN server over SSH][1]. Well, after a lot of following steps, sometimes multiple times last night, I gave up and went to bed… 

Then today, I decided to mess around a bit more, and found the following post on the [TortoiseSVN][2] site showing you [how to get TortoiseSVN working over SSH][3]. This is all well and good, but, at the end it didn&#8217;t work, and it got me a bit angry…

further searching helped me find this post by [Rene Gourley][4] (hope I pronounced that correctly…) explaining [HOW TortoiseSVN uses Putty to get certs and connection info][5]… This was the eye opener! I was putting the server name into my url (in my case svn+ssh://svn@tiernanohs/repository) where I should have been using the name I saved in putty (SVN) instead of the server name… TortoiseSVN looks for the session name, not the server name! Annoying, I will admit, but now its working! 

now all I have to do is get it talking to the MacBook Pro and my MSI Wind, and poke some holes in the firewall and I can work remotely!

 [1]: http://blog.lotas-smartman.net/running-svn-ssh-on-windows-home-server/
 [2]: http://tortoisesvn.net/
 [3]: http://tortoisesvn.net/ssh_howto
 [4]: http://renegourley.wordpress.com/
 [5]: http://renegourley.wordpress.com/2007/04/30/tortoisesvn-ssh-and-certificates/