---
title: the problem with building a solution as i need it
author: admin
layout: post
permalink: /the-problem-with-building-a-solution-as-i-need-it/
dsq_thread_id:
  - 26015560
  - 26015560
dsq_needs_sync:
  - 1
categories:
  - Uncategorized
---
Well, a while back i started building a <a class href="http://www.tiernanotoolephotography.com/">photography site</a>. This was built as a project, a test and a engineering practice. there where a few goals:

1: Build a photography site that was easy to upload photos to

2: Build it on <a class href="http://www.amazon.com/s3">Amazon&#8217;s S3</a> for storage, C# for the programming language, SQL as the backend Data Store and ASP.NET as the web interface

3: Build it scalable (or as scalable as posible). this envolved me building this in teirs and also having different teirs on different machines. So, the front end sits on the web server, which then calls a webservice in the back, which hosts the business logic and the data teir, which, technically calls a different machine for data. so there are 3 machines. Yes, this is very overkill for a project of this size, but it was an engineering test.

The problem with this is now that they are complete, to an extent, i want to add stuff to this. the problem with adding stuff (namley a better tagging system, a MobLog section (more like Flickr) and a way of backing the DB up to S3, so if the DB server dies, it can be regenerated.) The last point also makes sense for uploading to a new machine. but, thats another story. 

The idea of Tagging the photos is kind of there already in a keywording system. the problem with the keywording system is it is designed for only 1 keyword, to an extent. Also, the idea of the MobLog section is an interesting challange, because this would involve a database reorg, which may cause problems. Anyway, this is my new task for the weekend! <img src="http://blog.lotas-smartman.net/wp-includes/images/smilies/icon_smile.gif" alt=":)" class="wp-smiley" /> this should be fun. 

PS:&nbsp;This just proves im single. Im sitting here, on Valantines night, thinking in code&#8230;. Ugh&#8230;. <img src="http://blog.lotas-smartman.net/wp-includes/images/smilies/icon_sad.gif" alt=":(" class="wp-smiley" />