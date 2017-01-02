---
title: Image Web Site running a lot faster now, thanks to S3!
author: admin
layout: post
permalink: /image-web-site-running-a-lot-faster-now-thanks-to-s3/
dsq_thread_id:
  - 26015900
categories:
  - Uncategorized
---
[<img src="http://images.lotas-smartman.net/image.ashx?id=29d68d25-74d7-44bc-a53a-5f1696a5c401" align="right" />][1] Well, I have done some modification to the image site I [mentioned before][2], and and have gotten it doing what I wanted. I have an upload page, where I upload the file to my SQL Server, and it gives me a URL which I paste into a blog entry. Then, when it gets requested for the first time, it uploads the image to Amazon S3, puts the URL into the DB, and redirects the user to the correct place. From then on, it just does the redirect. no waiting. Pretty sweet, if I do say so myself! Maybe some time over the near future, if I get a chance, I will do a proper write up on how this was done&#8230; maybe&#8230; <img src="http://blog.lotas-smartman.net/wp-includes/images/smilies/icon_smile.gif" alt=":)" class="wp-smiley" />

<div class="wlWriterSmartContent" id="0767317B-992E-4b12-91E0-4F059A8CECA8:40640fdc-9c8a-4229-b901-ffd72efaecb1" style="padding-right:0px;display:inline;padding-left:0px;padding-bottom:0px;margin:0px;padding-top:0px;">
  Technorati Tags: <a href="http://technorati.com/tags/Amazon%20S3" rel="tag">Amazon S3</a>, <a href="http://technorati.com/tags/Image%20hosting" rel="tag">Image hosting</a>, <a href="http://technorati.com/tags/SQL" rel="tag">SQL</a>, <a href="http://technorati.com/tags/programming" rel="tag">programming</a>
</div></p>

 [1]: http://www.amazon.com/s3
 [2]: http://blog.lotas-smartman.net/archive/2007/06/05/images-on-this-site-to-be-redesigned.aspx