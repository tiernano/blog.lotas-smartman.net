---
title: XBox Live and Linksys RV042
author: admin
layout: post
permalink: /xbox-live-and-linksys-rv042/
dsq_thread_id:
  - 26016604
  - 26016604
dsq_needs_sync:
  - 1
categories:
  - HowTo
---
This post is more a post for me, than a general post, but it could come in handy for others.

<img alt="xbox live" align="right" src="http://images.lotas-smartman.net/image.ashx?id=5d4e430a-6d9d-4f83-9930-b509482d7a1f" />A while back,&nbsp;i got a Linksys RV042 for my home router. this was all well and good (2 internet connections, linked to [give me massive bandwidth][1]!). Its all great. but, my XBox 360 failed to connect to XboxLive. this started to annoy me, as i wanted to play games&#8230; Well, i found the issue. Its all to do with the [MTU setting on the Linksys Router][2].

To fix it, login to your router, go to the firewall tab and set the **MTU** setting to **Manual**, **1365**. i changed the setting, saved, and XBox live loads first time! works great!

&nbsp;

 [1]: http://blog.lotas-smartman.net/dual-wan-connections-rock/
 [2]: http://forums.linksys.com/linksys/board/message?board.id=Wired_Routers&message.id=13325#M13325