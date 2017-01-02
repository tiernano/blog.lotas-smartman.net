---
title: More on Desktop in the Cloud
author: admin
layout: post
permalink: /more-on-desktop-in-the-cloud/
dsq_thread_id:
  - 427648194
dsq_needs_sync:
  - 1
categories:
  - Articles
tags:
  - cloud
  - desktone
  - Rackspace
  - virtual hosted desktop
---
So, today an email came accross my inbox, which, in one way, i though should be marked as spam, but in another way, though it was an interesting idea, so i checked it out&#8230; Now, just to make things clear: I though it **could** be spam, but it may not be&#8230; I could have signed up for some information, and this is where it came from, but i dont know&#8230;

Anyay, the email was from a company called [desktone][1], who specilize in Virtual Desktops in the cloud. This is something that interested me and something i have tried before with [Rackspace&#8217;s Hosted Virtual Desktop offering][2]. their idea is a lot, by the looks of things, like Rackspaces, and, from the ping and speed test results, run in the same datacenter. but this has gotten me thinking&#8230;

I carry a late 2008 MacBook Pro with 8Gb ram and 500Gb HDD, running OSX Lion. I bring ths to college with me, and it does 90% of what i need. but for the rest, like Visual Studio coding, i remote desktop into the GodBox at home and do my major coding there&#8230; and it has me thinking: this could be very handy for smaller companies: in the place i work currently, we are all issued with Laptops. this makes moving around the place a lot easier&#8230; there are a few inherent problems with laptops that i can see:

  * they are more expensive then desktop machines of equivilant power
  * they are less upgradable (memory aint too hard, but most wont allow multiple drives, and upgrading graphics is usually out of the question&#8230;
  * if all your data is stored on the laptop, and you loose it, your screwed, especially if 1) its not backed up and 2) its confidential or sensitive&#8230;
  * and if you do loose it, it might take you a couple of days to get back to a good state&#8230;

With something like virtual desktops and a medium build client* you could have the best of both worlds. my thoughs behind it are as follows:

  * big box in a datacenter or in the office, with lots of CPU, memory and HDD space.
  * large enough pipe between the big box and clients. if its in the office, and you only have a few remote users, but lots of internal users, GigE in the office will probably do, depending on users, and decient internet connection (minimum of about 10-20MB both ways) for external users
  * on the big box, something like HyperV and System Center Virtual Machine Manager, VMWare and what ever they have, or Xen, etc&#8230; what ever the Virtualization software, it should support snapshots, creating VMs from a base image, etc, etc&#8230; something that will allow users to create a new VM easily (within their allotted VM capacity) and re-create machines based on previous snapsots&#8230; so if someting does go wrong, you can go back in time, or start from a good known state&#8230;
  * as for this medium build clients, you will probably want to use something ike BitLocker on the HDD for security, sync your documents folder with a file share any time it changes (this way it should be in sync with your VM), backups, etc&#8230;

Its an interesting idea, and something i like reading about&#8230; And if your not into the idea of some else hosting your desktop, like the Lads at Rackspace or desktone, you can always spin up your own instance on Amazon EC2 or Windows Azure and use them&#8230;

*Medium build client is somewhere between thick and thin client&#8230; still have processing power on board to allow work when &#8220;offline&#8221; but uses the power of the remote sever when connected&#8230;

 [1]: http://www.desktone.com/
 [2]: http://blog.lotas-smartman.net/rackspaces-hosted-virtual-desktop