---
title: 'Rackspace&#8217;s Hosted Virtual Desktop'
author: admin
layout: post
permalink: /rackspaces-hosted-virtual-desktop/
dsq_thread_id:
  - 313815568
dsq_needs_sync:
  - 1
categories:
  - Articles
tags:
  - Hosted Virtual Desktop
  - Rackspace
  - VMs
---
Racksapce announced a while back (Few days ago) that there where releasing something called a [Hosted Virtual Desktop Environment][1]&#8230; The idea was that they would host a VM on their network (or in some cases, racks of servers, each with lots of VMs) and you just connect with a thin client and start work&#8230;

The idea sounds interesting&#8230; and i am actually managing to write this post from a Rackspace HVD test environment (The current machine is a Quad Core Opteron with 15.5Gb of RAM, 160Gb HDD, hosted in the US with a very nice interest connection. Its running Windows 2008 R2 Server Enterprise Edition, and has a copy of Office 2010). FireFox and IE are installed, and, as a basic machine, its nice&#8230; I am not an Admin on the box, so I wouldn&#8217;t be able to install Visual Studio or anything like that, which would make testing this a bit more interesting, but then again, there is a bit of LAAAAGGGG&#8230;..

  * Firstly, by my calculations, the VM is about 180ms away from my house in Dublin, Ireland, which means you can notice the lag while typing&#8230;
  * There is a feature for making this work quicker, but its an admin feature and i cant seem to enable it&#8230; don&#8217;t know if it would make a difference&#8230;
  * In the Rackspace white paper, there is mention of using [Akamai][2] as an Application Accelerator&#8230; Wondering if that would that make a difference&#8230;
  * [YouTube][3], as you can probably guess, is not usable&#8230; Video is very buggy&#8230; one thing to node though: a Full 1080P HD video on YouTube does load Very Quickly!

Now, why would you need this? That&#8217;s a bit of a though question&#8230; If you are a company with a massive internet pipe, and have low ping times to either an Akamai pop or a Rackspace Data center, this could allow you to reduce hardware costs&#8230; buy a couple of thin client boxes, connect them to some monitors, and your good to go&#8230; no need to have dedicated hardware&#8230;

It might also be useful for On the Go type people&#8230; connect anywhere with an mobile device, and your at your main desktop machine&#8230; Not sure it would work for programmers though&#8230;.

Interesting idea&#8230; and i can say, in all fairness, this is the first time i have written a post on a Virtual Desktop Environment&#8230; and it was interesting&#8230; and just a little slow&#8230;.

[Bonus Material&#8230; some screen shots of the box. click for larger images]

[<img class="alignnone size-medium wp-image-4189" title="Task Manager on my HDV" src="http://blog.lotas-smartman.net/wp-content/uploads/2011/05/HVD-TaskManager-265x300.png" alt="" width="265" height="300" />][4]

[<img class="alignnone size-medium wp-image-4188" title="HVD-SystemProperties" src="http://blog.lotas-smartman.net/wp-content/uploads/2011/05/HVD-SystemProperties-300x264.png" alt="" width="300" height="264" />][5]

 [1]: http://www.rackspace.com/hostedvirtualdesktop/
 [2]: http://www.akamai.com
 [3]: http://www.youtube.com
 [4]: http://blog.lotas-smartman.net/wp-content/uploads/2011/05/HVD-TaskManager.png
 [5]: http://blog.lotas-smartman.net/wp-content/uploads/2011/05/HVD-SystemProperties.png