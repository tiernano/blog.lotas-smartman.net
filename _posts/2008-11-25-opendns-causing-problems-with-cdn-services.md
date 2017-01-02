---
title: 'OpenDNS causing &quot;Problems&quot; with CDN services'
author: admin
layout: post
permalink: /opendns-causing-problems-with-cdn-services/
dsq_thread_id:
  - 26016750
  - 26016750
dsq_needs_sync:
  - 1
categories:
  - Uncategorized
---
So, I have been using [OpenDNS][1] for quite some time now for my internal network, and I have also been using [SimpleCDN][2] for hosting my images, CSS, etc for the blog and a few other sites for a couple of months too. Well, today, while checking which was faster (Amazon’s new [CloudFront][3] or [SimpleCDN][2]) I started to do some ping time checks and found out something interesting…

It seems that the way CDNs figure out the best place to send you is based around your DNS server… Since i am using OpenDNS, they think i am somewhere else… for example, here is a traceroute report using 2 different DNS servers. the first is using my local ISPs (BT Ireland) and the second is using OpenDNS. See the difference?

![][4]

Same happens with SimpleCDN… as you can see, round trip times go from between 28 and 47ms all the way up to 184… that&#8217;s not good… now thinking about not using OpenDNS anymore because of this… <img src="http://blog.lotas-smartman.net/wp-includes/images/smilies/icon_sad.gif" alt=":(" class="wp-smiley" />

 [1]: http://www.opendns.com
 [2]: http://www.simplecdn.com
 [3]: http://aws.amazon.com/cloudfront/
 [4]: http://images.lotas-smartman.net/image.ashx?id=cf59b9e1-653e-42d2-93aa-2f52fb3c70d1