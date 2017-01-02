---
title: dotTEXT webservice info
author: admin
layout: post
permalink: /dottext-webservice-info/
dsq_thread_id:
  - 26013384
categories:
  - Uncategorized
---
after some coding and messing around, I have decided to share my findings with you, the great people who read my blog. all 6 or so of you. anyway, the address of the webservice is <http://www.yourhost.com/yourdirectory/services/simpleservice.asmx>. if you own the server, like me, and don&#8217;t have the directory hooked up, you done need the yourdiectory part. to post stuff, you use the InsertCategoryPost or SimplePost method. each take a username, password, datetime, title and body as parameters, but the category one takes an array of categories, which are strings. there is a get categories method which returns an array of strings. I am posting this on my pocket pc with a little app I built using this knowledge. go forth and make new posting apps for dotTEXT my readers!