---
title: 'I dont need to know where i am, i want to know where i&#039;ve been&#8230;'
author: admin
layout: post
permalink: /i-dont-need-to-know-where-i-am-i-want-to-know-where-ive-been/
dsq_thread_id:
  - 26016731
dsq_needs_sync:
  - 1
categories:
  - Uncategorized
---
&nbsp;So, i have had an idea, but its one that kind of needs community support to get it off the groud, so thats why its being posted here. i am hoping to start prototyping this up soon so any feedback is welcomed. The idea is something simular to [Fire Eagle][1], but with a twist&#8230;. Fire Eagle tells you, and applications, where you are now (or your last known position). What i want to propose is a system that tells you where you have been: i.e. log the GPS location you send to it all the time. Now why, you may ask, would you want to do this: well, Geo-Coding. if you have a large DB in the sky with your location info (secured), and you have a load of photos on your machine which where taken in the time window, together you can link them together. A web service/rest call to the service with authentication (including the authentication from the user) and a time will return a GPS cordinate for that user. some ideas of how you would use this service:

  * As i said, Photography: you bring your phone with you on a photo shoot. it has built in GPS, a data connection and some software for the logging. it automatically sends your location back at a predefined time interval (say, 5 seconds). you take your photos, get home, run your workflow, which includes some software to call the web service requesting locations. all meta data is saved in your files, and your happy!
  * live above, but with video. even better, if recording video, and your interval is low (say 1 second), you could track your movments with the camera. walking down a street, taking video along the way, you could see where you where walking, where you stopped and where you finshed. handy!
  * You go and fill up your car with Petrol or Deisel (dont put the wrong fuel in&#8230; it breaks your car!). you get a reciept with the date and time on it. you go home and you want to put the price on a petrol pricing site (another idea i have, but havent started on&#8230;). so, since you know the time you filled up at (on the reciept) and the service knows where you filled up, you can enter the price and location into the site (price, again, on reciept) and your sorted!!!&nbsp;
  * Finally, and this is a bummer one, but you get a speeding ticket (booo!!) and your not sure where you got it. Irish Speeding tickets do include the location, but its the whole road, not a particular point. they do, how ever, have the date and time info. put it into the service and you get a map back with your location at that time. now you know where you where, but you still get penelty points and your still screwed out of the fine&#8230; booo!!!

So, theres the idea. I envision third parties writing the clients for devices (Mobile phones, Pocket PCs, etc) and others using the service for getting data out of. to start with, i will be writing some basic clients (upload data from GPX files, requesting locations for photos, etc). I have even got a name: Where The Heck Was I? domain name is a nice easy to remember WTHWI.com, which goes nowhere at the moment, but will soon.&nbsp;

So, there you have it. Any questions, comments, ideas, please leave in the comments section.

 [1]: http://fireeagle.yahoo.net/