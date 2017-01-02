---
title: Image Site stats
author: admin
layout: post
permalink: /image-site-stats/
dsq_thread_id:
  - 26016458
  - 26016458
categories:
  - Uncategorized
---
So, for the last couple of months I have been using a custom Image hosting site. actually, May 21st 2007 6.58pm was the time I started testing it with logging, and may 22nd 2008 at 1.38am was the first time an external user hit the site. Ahh the power of logging <img src="http://blog.lotas-smartman.net/wp-includes/images/smilies/icon_smile.gif" alt=":)" class="wp-smiley" /> since then,&nbsp; it has served 52918 images to 15692 unique hosts. over 1.3Gb of images have been served, with the top 3 images using 375mb of bandwidth. there are 92 images and total size is a little over 340mb. 

&nbsp;

![][1] 

top image was hit over 5000 times, and the biggest image is just over 300k in size. All images are stored on Amazon S3 and served from there too. some updates to the project are in the works. Ideally, I would like to serve from both S3 US servers and the servers in the EU. since all the binary data of the images are stored in a Database, in theory this should not be a major problem. My problem is working out where to send the user&#8230; 

Speaking of which, the serving of images is done the following way. All images are referenced on this site as follows:

[http://images.lotas-smartman.net/image.ashx?id=26045268-2c24-4a5b-8033-073aed6c1a4f][2] (the image above).

when that gets clicked, the image.ashx file asks the DB if that file is on S3. if it is marked as no, then it gets uploaded, and redirects the user to the S3 URL. If it is already there, it just redirects the user, no question asked. There is some logging in the background (hence the cool stats!) and that&#8217;s pretty much it. 

When it comes to the EU and US S3 servers, my thinking is based around checking the users location based on a IP lookup using something like [MaxMind IP location][3]. obviously if a user is in the US, send them to the S3 server there. if in Europe, send them to the S3 server here. but if you get a user from Australia, where do you send them? China? Japan? It gets complicated then&#8230; Do you default to US servers or EU servers? Its something I will have to think about later on&#8230;

Anyway, i might make code available for some of this later on. watch this space!

 [1]: http://images.lotas-smartman.net/image.ashx?id=26045268-2c24-4a5b-8033-073aed6c1a4f
 [2]: http://images.lotas-smartman.net/image.ashx?id=26045268-2c24-4a5b-8033-073aed6c1a4f "http://images.lotas-smartman.net/image.ashx?id=26045268-2c24-4a5b-8033-073aed6c1a4f"
 [3]: http://www.maxmind.com/app/ip-location