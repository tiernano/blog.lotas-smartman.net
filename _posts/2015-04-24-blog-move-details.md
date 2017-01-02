---
title: Blog move details
author: admin
layout: post
permalink: /blog-move-details/
dsq_needs_sync:
  - 1
categories:
  - Uncategorized
---
yesterday i [wrote that i had moved][1] my site to [Jekyll][2] and i also mentioned i would post how how i was doing this. Well, this is that post.

First, getting data out of [Wordpress][3] was a bit of a pain (in my case... screwing around with [NGinX][4] and [PHP-FPM][5], but that is out of scope for this blog post... if you have a "normal" enough blog check out [Jekyll Exporter][8] ([geekphotogrpaher][6] and [Tiernans Podcast][7] both wored first time...)... If not, your on your own... 

Anyway, i got a zip file out of Jekyll Exporter that included all my posts (some had to be modified...) and all my images. Styles etc, not so much... But new blog, new style! (if your on an RSS reader, check out the new site [here][9].

So, then i installed Jekyll on my machine... Again, out of scope for this post, but the [Jekyll][2] website had details on installing and running it. I installed [Sabayon Linux][10] on my [Godbox 2][11] a while back... more on that eventually...

so, once Jekyll was installed, i created a new site by typing

	jekyll new blogname

this created a load of files under the blogname folder. I then did some tweaking... i copied all my original posts, images and pages to that folder and then ran

	jekyll serve

this generates all the HTML (puts it into the _site folder in your blog directory) and then serves the html at [http://127.0.0.1:4000][12]. Hitting that page in your favourite browser then shows you how it will look.

I did some tweaks to [plugins][18] and [Permalinks][19] to get the site the way i wanted it, but once completed, i just ran

    jekyll build
    
all my final files where then in the _site folder. I then use [RSync][13] to transfer the contents of my _site folder to the server and heay presto! its live! Well, semi live...

The main server is hosted in house, on an [Ubuntu][19] box running [NGinX][4]. But i have 3 internet connections, so i have an [OVH][20] box in France running both [Varnish][21] as a front end and [HAProxy][22] as a backend. HAProxy is pointing at the 3 WAN ips i have, and if one falls over, it take it out of the loop. Varnish then is pointing at that and doing caching... Finally, to make things even more complicated (but hopefully faster) I use [Rackspace Cloud][23], which in turn uses [Akamai][24] as a CDN for the site... 

So, there you have it. It is a lot more complicated then it needs to be. I could easily just generate the site and push to [Amazon S3][25] and do [what i am doing on tiernanotoole.ie][26] or even easier, use [Github Pages][27]. Hell, I use [GitHub][29] to host the site (privately) already, and if i use them to host it, they would build the bloody thing too! Anyway, its working, im happy, and hopefully it means i will post more often... then again, not sure... One other thing i need to do, or at least think about doing, is to [automate it][30]... One of these days...

Either way, checkout the [tiernanotoole.ie][28] site, since there is a lot more technical stuff there, or [geekphotographer][6] which is, obviously, for geeks and photographers! 

If you are looking at starting a blog using Jelyll, Check out the following links:

* [Jekyll main site][2]
* [Jekyll Bootstrap][14] 
* [Jekyll Resources][17]
* [Jekyll Template Guide][15]
* [Jekyll Getting started guide][16]

UPDATE 2015/08/13: This site is now hosted on a box in the house, but fronted by [CloudFlare][31].

[1]:http://blog.lotas-smartman.net/finally-moved-to-jekyll/
[2]:http://jekyllrb.com/
[3]:http://wordpress.org
[4]:http;//nginx.org
[5]:http://www.php.net
[6]:http://www.geekphotographer.com
[7]:http://podcast.tiernanotoole.ie
[8]:https://wordpress.org/plugins/jekyll-exporter/
[9]:http://blog.lotas-smartman.net
[10]:http://www.sabayon.org
[11]:http://tiernanotoole.ie/Computers/GodBoxV2.html
[12]:http://127.0.0.1:4000
[13]:https://rsync.samba.org/
[14]:http://www.jekyllbootstrap.com/
[15]:http://jekyllrb.com/docs/templates/
[16]:http://jekyllrb.com/docs/home/
[17]: http://jekyllrb.com/docs/resources/
[18]: http://jekyllrb.com/docs/plugins/
[19]: http://www.ubuntu.com
[20]: http://www.ovh.ie
[21]: https://www.varnish-cache.org/
[22]: http://www.haproxy.org/
[23]: http://www.rackspace.com
[24]: http://www.akamai.com
[25]: http://aws.amazon.com/s3
[26]: http://tiernanotoole.ie/2014/01/23/CDNHostedBlog.html
[27]: https://pages.github.com/
[28]: http://tiernanotoole.ie/
[29]: http://www.github.com
[30]: http://tiernanotoole.ie/2012/08/29/NewSite.html
[31]: http://www.cloudflare.com
