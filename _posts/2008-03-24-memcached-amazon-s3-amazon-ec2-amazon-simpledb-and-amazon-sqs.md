---
title: Memcached, Amazon S3, Amazon EC2, Amazon SimpleDB and Amazon SQS
author: admin
layout: post
permalink: /memcached-amazon-s3-amazon-ec2-amazon-simpledb-and-amazon-sqs/
dsq_thread_id:
  - 26016360
  - 26016360
dsq_needs_sync:
  - 1
categories:
  - Uncategorized
---
<p mce_keep="true">I have been thinking a lot since the announcment of [Amazon&#8217;s SimpleDB][1]. This is now a very stratigic peice that allows very large, scalable web applications. I have been thinking of ways to use this, and one idea i have had is an image uploading site.</p> <p mce_keep="true">The peices fit together as follows:</p> <p mce_keep="true">A couple of the small [EC2][2] instances as front end web servers. these would actually serve the images, take uploads of the images, generate the HTML to send to the brower, etc. Next, 1 or 2 large instances, which would act as Application Servers. These would sit in the back, running custom web service software, which would be called by the front end, and these would also talk to the SimpleDB backend and the Caching layer. There would be no need for a Database layer, as such, since all your data will be stored on [SimpleDB][3], but you would have a layer in the back of [Memcached Servers][4]. what would happen is when a request for the DB comes in, if its not already in cache, a query to SimpleDB goes out, and then its placed in cache. next time that request is made, no round trip to SimpleDB is required. </p> <p mce_keep="true">Also, a bunch of image processing servers would be handy to have. you would use [SQS][5] to queue items. your memcached servers or backend servers could be set to take images and process them, and if more then X number of images are in the queue, load up a new image processing instance. if X doubles, load 2 instances, etc. Images would be uploaded to S3, and could be servers either from your EC2 servers, or directly from S3. You could do things smart. If the user is making the request from somewhere close to the US, serve from EC2 (since the servers seem to be there). if the user is requesting from Europe or close, send them to your Europeen S3 site. </p> <p mce_keep="true">one of the limitations of SimpleDB is the 1024 byte limit for attributes. This could be solved by storing meta data, and larger text objects in an XML file, which is stored in S3. a link to this is stored in SimpleDB, and cached in Memcache for quick usage. </p> <p mce_keep="true">Amazon are definatly chaning the game for developing large sites. i hope i get my hands on a SimpleDB account soon! </p>

 [1]: http://blog.lotas-smartman.net/archive/2007/12/14/amazon-releases-in-limited-beta-amazon-simpledb.aspx
 [2]: http://www.amazon.com/ec2
 [3]: http://www.amazon.com/b/ref=sc_fe_c_1_3435361_1?ie=UTF8&node=342335011&no=3435361&me=A36L942TSJ2AJA
 [4]: http://www.danga.com/memcached/
 [5]: http://www.amazon.com/gp/browse.html?node=13584001