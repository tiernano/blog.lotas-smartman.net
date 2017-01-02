---
title: A CDN Hosted Blog
author: admin
layout: post
permalink: /a-cdn-hosted-blog/
dsq_thread_id:
  - 113764098
  - 113764098
dsq_needs_sync:
  - 1
categories:
  - Articles
tags:
  - Blog
  - cdn
  - wordpress
---
So, with the event of [Amazon&#8217;s Cloud Front][1] and [RackSpace][2][ Cloud&#8217;s Cloud Files][2] (with the backing of [Limelight Networks][3]) the world and its mother can now use cheap and cherfull CDNs for hosting images, CSS and JS files for their blogs. but what about the rest of the blog?

In theory, a blog is 99% static. With the help of the likes of [Disqus][4], you dont even need to manage your own comments. so, other than updates to the core template (which is probably not very often) and new blog posts (which for me is currently not very often), the rest of the site is very static. So, why cant that be hosted in a CDN? I am using a plugin on my WordPress install called [W3 Total Cache][5], and one of the options is to generate the HTML for a page, save it to disk, use a URL Rewrite to point to that HTML file for a certin amount of time, and, in theory, take some load of the server&#8230; the first time the page is generated, it should run though the PHP CGI engine (this site runs on IIS7 now) and then be built into a HTML page and passed to IIS to serve. the second time, its just served from IIS from disk, as a standard HTML page&#8230; and this got me thinking&#8230;

How hard would it be to take that outputted HTML page and upload to [Amazon S3][6] or RackSpace CloudFiles? using the same HTTP Redirect, just serve it from the CDN and bobs your uncle? Now, me not being a PHP dev, the answer chould be &#8220;Very&#8221;&#8230; but the question then comes up of, why cant it not be done anywhere else? this is, to some extent, how the [image hosting site][7] I built works. i upload images to a SQL DB, which gives me a nice URL to use. I open the URL, and if the file has not be uploaded to the CDN, it uploads and redirects me to the CDN location. the next request just gets redirected to the CDN.

So, the next question: is it posible to build a Proxy system that will proxy requests to and from the IIS box. request comes in, if its already on the CDN, redirect to the CDN. If not, show the main site, and in the background push the page to the CDN. you would need to do some magic around Search Engines (since they might get confused with CDN links and your main page) and also around logged in users (especially if you are using [WordPress][8]). anyway, its a theory&#8230; throwing it out there. main reason i was thinking about it is the fact that my server is hosted in house on a Cable Modem&#8230; so ping times can be a little slow&#8230; as can response times&#8230; ideally, this should make visiting this blog a little faster&#8230; but also any blog hosted by it&#8230; or at least, thats the theory&#8230;

[Update] added some code on GitHub with a demo of a HTML Module. some work needs to be done, but will add it in over time&#8230;

 [1]: http://aws.amazon.com/cloudfront/
 [2]: http://www.rackspacecloud.com/cloud_hosting_products/files
 [3]: http://uk.limelightnetworks.com/index.php
 [4]: http://www.disqus.com
 [5]: http://wordpress.org/extend/plugins/w3-total-cache/
 [6]: http://aws.amazon.com/s3
 [7]: http://blog.lotas-smartman.net/image-site-stats
 [8]: http://www.wordpress.org