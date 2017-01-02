---
title: 'CDN Hosted Blog: Part 2'
author: admin
layout: post
permalink: /cdn-hosted-blog-part-2/
dsq_thread_id:
  - 126657610
  - 126657610
dsq_needs_sync:
  - 1
categories:
  - Articles
tags:
  - AWS
  - Blog
  - cdn
  - CloudFront
  - hosting
---
So, this morning Amazon has announced that your can [set the Root Object of a CloudFront distribution][1]. this now means that you can have an index.htm file (like the front page of this blog) hosted, and tell Amazon to host that when someone goes to the main page. and since you can use a CNAME to make the URL look like (like mine which is [cdn.lotas-smartman.net][2]) you can put your contents of your blog on CloudFront and build a fully hosted web site. no more redirects or Proxy servers, as i sugested in my previous post! Theory now would go as follows:

  * host your website somewhere (like, say, realblog.lotas-smartman.net). this could be a WordPress or any other type of blog for that matter.
  * have your CloudFront site pointing to blog.lotas-smartman.net
  * on post (or every few hours) check the WordPress DB (or what ever else your using) and post the new (or updated) HTML to the site.
  * It probably makes sense not to use WordPress to manage your comments&#8230; [Disqus][3] might be a better option since its externally hosted&#8230;

I now have something to work on this weekend&#8230; <img src="http://blog.lotas-smartman.net/wp-includes/images/smilies/icon_smile.gif" alt=":)" class="wp-smiley" />  
<!-- EAVB_VNFYYSYMEB -->

 [1]: http://aws.typepad.com/aws/2010/08/new-amazon-cloudfront-feature-default-root-object.html
 [2]: http://blog.lotas-smartman.net/a-cdn-hosted-blog
 [3]: http://disqus.com/