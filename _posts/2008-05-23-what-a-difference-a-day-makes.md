---
title: 'What a difference a day makes&#8230;'
author: admin
layout: post
permalink: /what-a-difference-a-day-makes/
dsq_thread_id:
  - 26016599
categories:
  - Uncategorized
---
And an upgrade to SQL server as your Graffiti Backend! 

here is the load time graph from [mon.itor.us][1] yesterday, before moving the DB to SQL server:

![][2] 

and here is a screen shot of the same server, same hardware, but with SQL as the Backend:

![][3] 

yes, that image is only for the first 9 hours, but check out the avg min and max times, compared to the above. also, that 2% downtime is my fault. I needed to take the IIS instance down, and then had a config setting wrong for SQL in the web.config&#8230; I will keep my eye on this one with interest! 

PS: the DE and AT times are a lot lower than the US times since this server is living in mainland Europe. the graph for when the server lived in Ireland is pretty much the same. I am not going to stick it up here, since I am too lazy&#8230;.

 [1]: http://mon.itor.us
 [2]: http://images.lotas-smartman.net/image.ashx?id=0763ec37-abe4-4500-a372-94f3dab146d9
 [3]: http://images.lotas-smartman.net/image.ashx?id=e05d7048-b7df-4260-8bfa-705d06f5abf9