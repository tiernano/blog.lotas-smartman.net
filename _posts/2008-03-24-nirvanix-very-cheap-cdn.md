---
title: 'Nirvanix: Very cheap CDN?'
author: admin
layout: post
permalink: /nirvanix-very-cheap-cdn/
dsq_thread_id:
  - 26016496
  - 26016496
dsq_needs_sync:
  - 1
categories:
  - Uncategorized
---
I found a company called [Nirvanix][1], and started looking into what they are doing. its an Amazon S3 competitor. but, they way its done is interesting. They have 2 options: base storage or Global Storage Delivery Network. Base storage is much like Amazon S3: Store in either US or EU data centre. your charged 18c per Gig stored on their server and 18c per gig transferred, either up or down. There are some other options, but you should really check their site. 

The one that is more interesting is the SDN, or Storage Delivery Network. You are charged 25c per Gig a month hosted on the Global SDN, 48c per gig per month if you want it in 2 Geographically dispersed nodes and 71c per GB/month if you want it on 3&#8230; Its a bit confusing, but, comparing it to the likes of Akamai, its a lot cheaper. 

There is a minimum fee of $1 a month, and there is a full [API][2] for uploading files to the servers. Check the [pricing site for more][3].

The only reason i have not signed up yet, and i have asked them to fix this, is their signup form is not encrypted, and its asking for Credit Card Details&#8230; Hmmmm&#8230;.

 [1]: http://www.nirvanix.com/
 [2]: http://developer.nirvanix.com/sitefiles/1000/API.html
 [3]: http://www.nirvanix.com/gettingStarted.aspx