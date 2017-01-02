---
title: RedHat 9.0 install info and notes
author: admin
layout: post
permalink: /redhat-90-install-info-and-notes/
dsq_thread_id:
  - 26004748
categories:
  - Uncategorized
---
I installed [ Redhat 9.0][1] last night over the Internet. It was easer then expected.

Read more for details.

<!--more-->

I had a copy of the Redhat boot CD. It&#8217;s just a CD with the boot stuff on it.

It&#8217;s taken over from the floppy option used before. Now instead of having 4 different floppies (PCMCIA, Net, Net drivers disk and there was an other one, but I never used it!) there is now one 16mb ISO. The ISO boots the machine and has the normal options. How do you want to install (FTP, HTTP, Network or CDROM/Hard drive) is the first question that comes up, then asking you about your network info, and finally where you want to install from. I installed over the Internet (because I can!) and I told Redhat where my router was, what I wanted as my IP and my DNS settings. It then asked where I wanted to install it from (in my case a local mirror in Ireland) and it started to download the second stage install file. I was hoping it would be in a GUI like the install from CD usually is, but unfortunately it was not. Redhat have opted for the command like kind of way of installing. Its not the X GUI, but I supose it is a GUI of some sort. Well, maybe not GUI, but a UI none the less.&nbsp;

It asked a few more questions, partition info, what I wanted to install (workstation, server, developer workstation or custom) and me being me decided to go for developer workstation. The partitions where easy to set-up. I told Redhat what way I wanted them set-up and it did it. I could have told it to auto partition, but the last time I got it to auto partition, it made my /home drive small. Since I work mainly from /home (get it! :P) I wanted a fairly large /home directory. So I partitioned my self.&nbsp;

Everything went well, and the install process its self took about 6 &#8211; 8 hours. Well i&#8217;m not exactly sure how long it took, but I started about 8pm, and when I woke up at 6am, it was finished.

I-m assuming about 10 hours max, but I think the timer was saying about 6. As I said, I did install from the Internet and my connection, although faster then most @ 600k, is not the fastest. I would like to run a local mirror the next time I have to install a copy of Linux because it would make it quicker. The final thing I can talk about now is the look of the new system and what it actually has. It found all my hardware first. Including my CDWriter (it asked did I want to set my kernel option to add IDE SCSI support, so

that&#8217;s what&#8217;s needed for CDR Support. I know from previous experience!) And also found both my sound cards (Creative labs Vibra 128 PCI and onboard AMD something or other). It found my video card and monitor and got them working grand. Ohhh and it found the network card, which is a good thing since I

haven&#8217;t a clue exactly what it is! (Intel network card that came onboard with the motherboard). So, ill post another write up later when I have more time with the machine. So far

it&#8217;s pretty cool. No problems.&nbsp;

Going to install [ VMWare][2] and Windows under it for development and testing, and also messing. Its installing the updates from the redhat network site and also

[ Ximian Desktop 2][3]. They should work by tonight.

 [1]: http://www.redhat.com
 [2]: http://www.vmware.com
 [3]: http://www.ximain.com