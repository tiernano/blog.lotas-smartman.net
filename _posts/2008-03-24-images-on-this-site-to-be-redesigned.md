---
title: Images on this site to be redesigned
author: admin
layout: post
permalink: /images-on-this-site-to-be-redesigned/
dsq_thread_id:
  - 26015897
  - 26015897
categories:
  - Uncategorized
---
<img src="http://images.lotas-smartman.net/image.ashx?id=c5202ba9-c3bc-4ab8-88c4-be2331bf7687" align="right" /> Over the past couple of weeks, I have been building an Image serving site. The images that are being served are not photos, but more blog images. an example of this is this photo of Steve Jobs and Bill Gates, which was also used in [this post][1]:

![][2] 

At the moment, the way the image is hosted is as follows: The image is stored in a SQL server as a binary blob. there is an ASHX handler which does most of the real work. So, the URL for that image is:

> [http://images.lotas-smartman.net/image.ashx?id=8e9642ef-ff31-4253-93ce-4c79e2484ea5][3]

When you click on it, at the moment (or once the image is requested, like above) the ASHX file checks the requesting client. If it is the [Coral Web Cache][4] requester, the binary data is returned. If its anything else, you are redirected to a Coralized version of the image, like so:

> [http://images.lotas-smartman.net.nyud.net:8080/image.ashx?id=8e9642ef-ff31-4253-93ce-4c79e2484ea5][5]

The problem I have is that something is slow. I cant figure out if it is Coral, or my site, but something is slowing down the loading of the site. 

So, a redesign is needed. My thinking is as follows.

> Upload an image to the server, as it currently is done (into a SQL DB as a SQL blob).
> 
> stick the file into [Amazon S3][6], and insert the new URL into the DB. the same URL (as above, non Coralized) will still work as planed (so I don&#8217;t have to fix all images on the site). 
> 
> If Coral comes a knocking, send on the correct URL (redirect to Amazon S3). 
> 
> anything else gets redirected to the correct URL too. 

The advantage of having pages redirected is simple: tracking and change. I can now have a good count of visitors seeing images, and also check if someone is robbing an image they shouldn&#8217;t, and also, if someone comes out with better, cheaper hosting, I can modify the system to use them instead! <img src="http://blog.lotas-smartman.net/wp-includes/images/smilies/icon_smile.gif" alt=":)" class="wp-smiley" />

Now, in theory it shouldn&#8217;t be too hard. in practice, well, we will see when I start coding this&#8230; heay? <img src="http://blog.lotas-smartman.net/wp-includes/images/smilies/icon_smile.gif" alt=":)" class="wp-smiley" />

<div class="wlWriterSmartContent" id="0767317B-992E-4b12-91E0-4F059A8CECA8:226abde0-3758-4d42-8241-4b0460a91569" style="padding-right:0px;display:inline;padding-left:0px;padding-bottom:0px;margin:0px;padding-top:0px;">
  Technorati Tags: <a href="http://technorati.com/tags/CoralCDN" rel="tag">CoralCDN</a>, <a href="http://technorati.com/tags/Amazon" rel="tag">Amazon</a>, <a href="http://technorati.com/tags/S3" rel="tag">S3</a>, <a href="http://technorati.com/tags/CDN" rel="tag">CDN</a>, <a href="http://technorati.com/tags/images" rel="tag">images</a>, <a href="http://technorati.com/tags/ASHX" rel="tag">ASHX</a>
</div>

 [1]: http://blog.lotas-smartman.net/archive/2007/06/04/bill-gates-and-steve-jobs-interview-at-d5.aspx
 [2]: http://images.lotas-smartman.net/image.ashx?id=8e9642ef-ff31-4253-93ce-4c79e2484ea5
 [3]: http://images.lotas-smartman.net/image.ashx?id=8e9642ef-ff31-4253-93ce-4c79e2484ea5 "http://images.lotas-smartman.net/image.ashx?id=8e9642ef-ff31-4253-93ce-4c79e2484ea5"
 [4]: http://www.coralcdn.org/
 [5]: http://images.lotas-smartman.net.nyud.net:8080/image.ashx?id=8e9642ef-ff31-4253-93ce-4c79e2484ea5 "http://images.lotas-smartman.net.nyud.net:8080/image.ashx?id=8e9642ef-ff31-4253-93ce-4c79e2484ea5"
 [6]: http://www.amazon.com/s3