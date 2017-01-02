---
title: iTunes + Windows Server 2008 + Hyper-V = BAD?
author: admin
layout: post
permalink: /itunes-windows-server-2008-hyper-v-bad/
dsq_thread_id:
  - 
  - 
dsq_needs_sync:
  - 1
categories:
  - Uncategorized
---
[UPDATED: 2011/10/04] I know this post is very old, but i though i should post that this issue ended up being a problem with a network driver on the machine&#8230; The MacPro has a couple on Intel Pro Network cards onboard, so a trip to Intel&#8217;s Driver site, a download, and i was good to go&#8230; So, if for what ever reason, you are having a simular issue, try the latest network drivers.

In the [first installment][1] of my [Windows Server 2008 as a Workstation][2] series, i talked about Media and how iTunes needed to work perfectly for me to be happy. Well, Over the last couple of days things could have been better&#8230;. I have noticed some interesting things that iTunes 8 has been doing which i am not liking&#8230; I have said before that i have the iPhone, iPod touch and Apple TV, and the main things i sync with iTunes being the Apple TV and the iPhone. Well, up until a few days ago, the AppleTV was out of action (well, wasent being used all that often). Then iTunes 8 came out with the HD TV shows, and the Keynote from Tuesday, so i decided to hook up the AppleTV and watch the keynote. All has gone terribly wrong since&#8230;

after about 20min (give or take) of the AppleTV being synced with iTunes, W2k8 looses all network connectivity. it only happens with iTunes syncing. I have managed to repro this about 8 or 9 times in the last few days, and it is starting to annoy me a lot, since the only way to get network back is reboot. The machine i am running this on is Mac Pro, and i tried reinstalling iTunes and nothing helps. This really sucks a lot. I have another machine here running 2k8 with Hyper-V and i am going to give that a try, and although i do have a third box running 2k8 and no hyper-v, it is a production box, so that wont be used for testing&#8230; Any one else seeing this?

[update] just to note: this did not happen before on the previous version of iTunes (7.7.1?). this seems to be a new thing with 8. Maybe its releated to the [BSOD that was happening on Vista][3]?

 [1]: http://blog.lotas-smartman.net/windows-server-2008-workstation/moving-to-windows-2008-server-as-workstation-part-1/
 [2]: http://blog.lotas-smartman.net/windows-server-2008-workstation/
 [3]: http://www.tuaw.com/2008/09/12/itunes-8-causes-windows-vista-bsod/