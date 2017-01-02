---
title: rebuilding the photography site with SQS, Serialization and more
author: admin
layout: post
permalink: /rebuilding-the-photography-site-with-sqs-serialization-and-more/
dsq_thread_id:
  - 26015562
categories:
  - Uncategorized
---
So, over the last couple of days I have been thinking about rebuilding the photography site to add more stuff to it. I [mentioned on Wednesday][1] what I wanted to add to it, so I wont go into much details here. Well, one of the sections I mentioned was &#8220;backup the database to S3&#8243;. Well, I have been thinking of how to do this, and came up with a cunning plan&#8230;

Binary Serialization. So, they theory is simple. each photo that is uploaded is a single entity. it has sub entities (versions, which are resized versions of the photo, meta data, which is basically a value and a name, and a tag, which is just used for easy tagging of the photos). So, the theory is that once the object is fully created (after the processing stage, which I will go into in a minute) the data is dumped into a binary blob, and uploaded to S3. If, for some reason, something goes wrong, the app can go looking for these blogs of data, import them, and be able to regenerate the DB from scratch, or at least from a blank DB. this also makes life easier for migrating to different boxes.

The next section is the processing stage. At the moment, a photo is uploaded in all its full glory (if taken with my 350D, its about 8MP in size and weighs in at roughly 4mb). this is placed in the processing queue. at the moment, the server does all the work. this is grand for the moment because there are very few photos uploaded at a time. but, it takes time. so, next idea: a proper queuing system. this is where [Amazon SQS][2] comes in. so, the solution. A photo hits the web server to get processed. server uploads the original to S3, and generates a GUID based on this, which is placed in the SQS queue. a client then connects to the queue, and gets an item to process (there could be multiple clients so they shouldn&#8217;t get the same item). once it gets the item, it then downloads the original photo, does its processing (pull out all Meta Data, resize to the new sizes, upload to S3, place the binary blob on to S3 and then place data into the DB). 

Lets see what we can build over the weekend, shall we? <img src="http://blog.lotas-smartman.net/wp-includes/images/smilies/icon_smile.gif" alt=":)" class="wp-smiley" />

[update] Another interesting idea Flickr has for their API is [Machine Tags][3]. So, for example, you could have the following types of tags (from the flickr site):

medium:paint=oil

or 

medium:photo=digital

camera:model=&#8221;Canon 350D&#8221;

or anything.

this can then be queried using their API. I&#8217;m wondering how open my API should be&#8230;</p> 

Tags: <a href="http://technorati.com/tag/AmazonSQS" rel="tag">Amazon SQS</a> <a href="http://technorati.com/tag/AmazonS3" rel="tag">Amazon S3</a> <a href="http://technorati.com/tag/Photographysite" rel="tag">Photography site</a> <a href="http://technorati.com/tag/programming" rel="tag">programming</a>

 [1]: http://blog.lotas-smartman.net/archive/2007/02/14/the-problem-with-building-a-solution-as-i-need-it.aspx
 [2]: http://www.amazon.com/gp/browse.html?node=13584001
 [3]: http://www.flickr.com/groups/api/discuss/72157594497877875/