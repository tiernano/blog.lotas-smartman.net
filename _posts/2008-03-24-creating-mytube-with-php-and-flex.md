---
title: 'Creating &quot;MyTube&quot; with PHP and Flex'
author: admin
layout: post
permalink: /creating-mytube-with-php-and-flex/
dsq_thread_id:
  - 26015849
  - 26015849
categories:
  - Uncategorized
---
OReilly&#8217;s OnLamp.com has an article showing you <a class href="http://www.onlamp.com/pub/a/php/2007/05/24/creating-mytube-with-flex-and-php.html?page=1">how to build a YouTube type website</a> using PHP and Adobe Flex. Interesting idea. They also talk about using <a class href="http://www.amazon.com/s3">Amazon S3</a> for the Video storage, but you could go one further and use <a class href="http://www.amazon.com/ec2">Amazon EC2</a> for the video Encoding too. Anyway, i suppose the all important question is: How do you do it with ASP.NET/C#/SQL2005/SilverLight? i find the video quality of Flash to be fairly low quality, especially if you think some broadband connections can cope with a lot more data. so, how about streaming 720p video from S3, directly to the user with SilverLight? you could do some inteligent stuff to. When the Silverlight app loads, it could check the bandwidth of the connection (C# and magic!) and select a video stream accordingly. just a thought&#8230;. <img src="http://blog.lotas-smartman.net/wp-includes/images/smilies/icon_smile.gif" alt=":)" class="wp-smiley" />