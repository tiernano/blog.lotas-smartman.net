---
title: Cachability, Amazon S3, CDNs, website speed and Proxys
author: admin
layout: post
permalink: /cachability-amazon-s3-cdns-website-speed-and-proxys/
dsq_thread_id:
  - 26016555
categories:
  - Uncategorized
---
So, one thing that i have noticed over the last couple of months is how slow my blog has become. it may be because the machine that is hosting the blog is running slower than it should be. it could be the data backend. it could (but hopefully isent) the [ISA server][1] sitting infront of the network.&nbsp;it could be a number of things. I will be installing Windows Server 2008 on my Dual Opteron machine in the next few days and will move the blog to that, hopefully speeding up the responces.

but while playing around, i found some other interesting peices of information. when checking the [Cachability][2] of the blog, i found that there is a 97kb Javascript file (Prototype.js) being pushed down to users, and its not marked as cachable. this is a bad thing. if you hit the site a couple of times a day, there is a good chance you will have to download that file multiple times! also, nearly nothing on the site is marked as cachable! so, i have to do some tweaking with the IIS server to enable these files to be marked as cachable.

Speaking of which, my image site has been modified. Now all images that are served from [Amazon S3][3]&nbsp;are marked as cachable for 6 hours. i have to look into this a bit more, and may increese the time to something a bit more, like 12 or 24 hours, or maybe even 2 or 3 days.

there is method in my madness around caching. If i can reduice the amound of traffic comming out of my network (not just this site, but also [thehairyone.net][4] and [kicks.motorloggr.com][5]) then the sites are faster for users to view and means i dont have to worry about slow page views. if i can get all the extra bits (no pun intended), like javascript, CSS, images, etc, cachable, or hosted externally, either by Amazon S3 or on a CDN (like [Coral][6] or [CacheFly][7]), it will make site site faster, more usable, and hopefully give a better user experiance!

comments welcome!

 [1]: http://www.microsoft.com/isa
 [2]: http://www.ircache.net/cgi-bin/cacheability.py
 [3]: http://www.amazon.com/s3
 [4]: http://www.thehairyone.net
 [5]: http://kicks.motorloggr.com
 [6]: http://www.coralcdn.org/
 [7]: http://www.cachefly.com