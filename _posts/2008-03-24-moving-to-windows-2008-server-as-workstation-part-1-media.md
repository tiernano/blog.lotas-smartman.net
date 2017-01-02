---
title: 'Moving to Windows 2008 server as Workstation: Part 1: Media'
author: admin
layout: post
permalink: /moving-to-windows-2008-server-as-workstation-part-1-media/
dsq_thread_id:
  - 26016492
  - 26016492
categories:
  - Windows Server 2008 Workstation
---
So, I have done some testing with a Virtualized Win2k8 Image and found out some interesting things. Firstly, you can install Windows Media Player on your Win2k8 server by selecting Desktop Experience in the Features section of the Server Manager. Problem is that Media sharing is not enabled, and by the looks of my searching online, <a mce_href="http://sadjadbp.spaces.live.com/blog/cns!21F12BB61B822DFA!286.entry" href="http://sadjadbp.spaces.live.com/blog/cns%2121F12BB61B822DFA%21286.entry">not possible</a>&#8230; Also, an interesting note: Windows Live writer will not install on a Server OS either&#8230; Now, everything else, in theory, should work just fine.

So, one idea to solve the problem is to Virtualize Windows Vista on the server. This means that when i need Vista, i just boot the image. I will also use it as a reason to test Hyper-V! <img src="http://blog.lotas-smartman.net/wp-includes/images/smilies/icon_smile.gif" alt=":)" class="wp-smiley" /> More on this later. Backing up stuff now, might try it out in the morning!

[**update**] one important media tool for a lot of users would be iTunes. For this test i used the x64 edition of iTunes, and my Virtual Machine knew about my [iPod touch][1] (16Gb) connected via USB. iTunes worked without problem, and seen the iPod touch and allowed me to sync with it. So, 2k8 will sync an iPod. Also, to note, Sharing music over a network with iTunes works. I am currently having problems with both my [AirPort Express][2] (not configured correctly, dont know where the PowerBook is at the moment&#8230;) and my [Apple TV][3] (currently in for repairs). I will try configure the Airport Express tomorrow and try it out, and once the Apple TV comes back, I will see if that works&#8230;

[update 2] some issues&nbsp;have come out aroudn iTunes&nbsp;8 and Hyper-V syncing with&nbsp;AppleTV. Read [more here][4].&nbsp;

 [1]: http://www.apple.com/iPodTouch
 [2]: http://www.apple.com/airportexpress
 [3]: http://www.apple.com/AppleTV
 [4]: http://blog.lotas-smartman.net/itunes-windows-server-2008-hyper-v-bad/