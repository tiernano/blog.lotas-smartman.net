---
title: EC2 Best Practices
author: admin
layout: post
permalink: /ec2-best-practices/
dsq_thread_id:
  - 
  - 
categories:
  - Uncategorized
---
The Space program blog has a post with some info about [EC2 Best Practices][1]. Some interesting things in here. One of the most important ones I though was as follows:

> *Keep your database as small as possible. Store as much data as possible on Amazon Simple Storage System (S3), NOT in your database and just store the S3 key to the data in your database. Consider putting any blob or large text fields in S3. This will make it much easier and faster to manage database backups, plus your database will perform better.*

This is something I have wanted to do for a while. Take, as an example, my image hosting site (no link since its all mainly Back End stuff). At the moment, most stuff is hosted in the SQL server, mainly because of laziness. If I wanted it to work very well on [Amazon EC2][2], I would store basic info in the DB, but make sure it can be taken back from S3. how? Serialization. 

With the image site, the most important part to store is the images. Think of it as an object. It has a URL, a name, a content type, binary data and a unique ID (I use GUID&#8217;s). My thinking is this info should be placed in an object, and then serialized any which way you want (XML is probably the best). 

When an new image is uploaded, the main image is placed in S3 storage, and the XML object file is placed there too. If your DB goes belly up, you should have a script or program to ask [S3][3] for all XML objects, and place them into the DB. this allows for easy replication of the DB. Also, it means the DB servers don&#8217;t really have to know about one another. 

[update] The Space Program Blog also has this post about getting [MySQL running on EC2 in the /mnt storage partition][4]. Mind you, they mention that if anything goes wrong it goes away, but still handy! <img src="http://blog.lotas-smartman.net/wp-includes/images/smilies/icon_smile.gif" alt=":)" class="wp-smiley" /> 

[[Via AWS Blog][5]] 

<div class="wlWriterSmartContent" id="0767317B-992E-4b12-91E0-4F059A8CECA8:03ed7e81-d487-4961-bd9a-4798a593f3a0" style="padding-right:0px;display:inline;padding-left:0px;float:none;padding-bottom:0px;margin:0px;padding-top:0px;">
  Technorati Tags: <a href="http://technorati.com/tags/EC2" rel="tag">EC2</a>, <a href="http://technorati.com/tags/S3" rel="tag">S3</a>, <a href="http://technorati.com/tags/The%20Space%20Program" rel="tag">The Space Program</a>, <a href="http://technorati.com/tags/AWS" rel="tag">AWS</a>, <a href="http://technorati.com/tags/OOP" rel="tag">OOP</a>, <a href="http://technorati.com/tags/XML" rel="tag">XML</a>, <a href="http://technorati.com/tags/MySQL" rel="tag">MySQL</a>
</div>

 [1]: http://blog.spaceprogram.com/2007/06/third-app-migrated-to-amazon-ec2.html
 [2]: http://www.amazon.com/ec2
 [3]: http://www.amazon.com/s3
 [4]: http://blog.spaceprogram.com/2007/06/amazon-ec2-ephemeral-storage-mnt-and.html
 [5]: http://aws.typepad.com/aws/2007/06/ec2_best_practi.html