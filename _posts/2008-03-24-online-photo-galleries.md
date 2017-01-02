---
title: Online photo Galleries
author: admin
layout: post
permalink: /online-photo-galleries/
dsq_thread_id:
  - 26014885
  - 26014885
categories:
  - Uncategorized
---
This is the handy thing about having 2 blogs with 2 different types of readers. I have this blog with developers and technical people (probably) and I have [my photographic blog][1] with photographers and probably technical people. But now I am looking for a good online solution for online galleries. I have a lot of photos I would like to post to the net, but I don&#8217;t know which way to go about this. I COULD use [Flickr][2], which is nice, but then I can&#8217;t protect images too well. I also couldn&#8217;t decided later to sell images (if the market was there). Another idea would be [SmugMug][3]. it&#8217;s nice, but I don&#8217;t want to spend $150 on their pro suite to find out that it&#8217;s not for me, plus their 7 day trial seems too shot for my liking. Methinks 30 days might do it. 

My thinking also comes to the idea of rolling my own. With this idea I can do a lot of cheating, and customization. And I have been thinking a lot about this too. I use Apple&#8217;s Aperture for my image manipulation (mainly because of its RAW features). I posted about a [better web gallery using Aperture][4] which had some interesting ideas, and after playing with this, I think I have cracked the idea to an extent. I have managed to export all the metadata from the photos to a CVS file, which I have also managed to parse using C#, and it&#8217;s gotten to the stage where I am trying to get this into the DB in a quick and easy way (mainly delaying me is the installing of Vista a few days ago). My thinking behind this is if I can get that info into a DB, I can then build the gallery around it. I can have my images in 3 sizes: Thumbnail, 800&#215;600 and full size (about 8mega pixels). I can have the thumbnail and 800&#215;600 images free, which some sort of caption at the bottom of the image (still working on that) and then hide the full size one, only available when paid for (using [PayPal][5] or similar). This is the more technical question on this blog: has anyone tried anything like this? Are there any examples you have seen? Or is there something that does something like this already? Am I reinventing the wheel, so to speak? If so, drop me an email (<tierno@lotas-smartman.net>) or leave a comment! 

One thing I will say about both Flickr and SmugMug: their API seems very cool. I have played previously with the Flickr API and it rocks, and the SmugMug one looks very comprehensive.

**[update] **one futher thing i though i might add to this is the way i though of storing the photos. my thinking is that because this will (more then likely) be hosted in house on my broad band connection, i would need some sort of external storage site for my photos. I though of [Amazon&#8217;s S3][6] service. this will be cheap and secure. now, to figure out a way of securing all of this and making sure nothing gets screwed up&#8230;

Bk_keyworks: photography, apple aperture, c#

 [1]: http://photography.lotas-smartman.net/blog
 [2]: http://www.flickr.com
 [3]: http://www.smugmug.com
 [4]: http://photography.lotas-smartman.net/blog/2006/06/better-aperture-web-galery.html
 [5]: http://www.paypal.com
 [6]: http://www.amazon.com/s3