---
title: Build your own Podcast/Videocast network
author: admin
layout: post
permalink: /build-your-own-podcastvideocast-network/
dsq_thread_id:
  - 26015425
  - 26015425
categories:
  - Uncategorized
---
earlier on I was talking about [how to build your own Podcast client][1]. Well, I have been thinking, and have come up with the idea of how to build your own Podcast or Video Cast (AKA Video Podcast, which I think is a stupid name) network. Not just for a single Podcast, but could be used for a whole bunch of them! 

So, the theory (and maths): I have a Podcast, and on average the file size weighs in at roughly 15 megs (some where as small as 6mb, one was as big as 30). I currently have 50 Podcast in my back catalog. we say that the total size for them 50 Podcast is 750mb. To host them on [Amazon&#8217;s S3][2] network, it would cost less then 15c per month! Actually, it would cost about 11.25c per month, just to host them there. 

Next we have how many times they are downloaded. My last Podcast was downloaded a total of 125 times. the one before that was downloaded 500 times. the one before that again was 1500 times! so, we take an average of the 3 (just for guess work) which is 700 (ish) and multiply that by the size of the last Podcast (which is &#8230;. drum roll&#8230;.&nbsp; 10.5Gb). that costs a total of about $2.10 a month to run. now, that&#8217;s for the last Podcast. We make the estimate that back catalog downloads will be downloaded at a rate of 2x times a day (60 downloads per Podcast, per month). Since I have a back catalog of 50, this would work out at 2940 downloads a month. this is a bit unrealistic, but its estimations&#8230;. so, 2940 downloads, at 15mb per download, works out at 44.1Gb per month, which is, $8.82 per month. 

Finally, we have the fact that BitTorrent can be used, very easily, and there are other theory&#8217;s including working with [EC2][3] for compression of Video/Audio, bulk uploading/download (eg, when moving from one host to another), and various other bits and pieces. 

So, what does the total come to? Well, here is the maths:

Original upload cost: 750mb @ 20c per gig transferred: 15c

Monthly hosting cost: 750mb @ 15c per gig hosted: 11.25c

last Podcast downloads: 700 \* 15mb \* 20c = $2.10

back catalog downloads: 60 \* 49 \* 15 * 20c = $8.82

Total price: $11.18.

my maths aren&#8217;t perfect. this will increase every month, depending on how many extra Podcast are added. Video is larger, so that has to be taken into account. if you use Amazon EC2 for Computing power, this will cost 10c per hour running, plus 20c per gig transferred to and from Amazon (excluding S3 bandwidth). with some hacking, you could easily have a Video Podcast in both standard def (WMV, MOV and DivX), iPod, Zune and PSP formats, with an accompanying audio only Podcast (MP3, WMA, OGG, MP4), have most of it processed by Amazon (you record a standard video with your camera, copy the WMV version to Amazon, and get a script running on your EC2 instance (which only runs when you want it to) to process that video into all different formats, upload to S3 and post links into a web service running your site. Anything&#8217;s possible! <img src="http://blog.lotas-smartman.net/wp-includes/images/smilies/icon_smile.gif" alt=":)" class="wp-smiley" />

 [1]: http://blog.lotas-smartman.net/archive/2007/01/16/19180.aspx
 [2]: http://www.amazon.com/s3
 [3]: http://www.amazon.com/ec2