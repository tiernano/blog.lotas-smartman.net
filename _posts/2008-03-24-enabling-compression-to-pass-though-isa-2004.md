---
title: Enabling compression to pass though ISA 2004
author: admin
layout: post
permalink: /enabling-compression-to-pass-though-isa-2004/
dsq_thread_id:
  - 26012050
  - 26012050
categories:
  - Uncategorized
---
[TristanK has this post: ISA 2004 vs HTTP Compression][1] on his blog. ISA 2004 server, out of the box, does not accept or forward the header that tells the web server (be it inside or outside) that your browser supports HTTP compression. this is a security feature because if it is compressed ISA cant check it for different things. There is, how ever, a work around. i will be trying this out when i get home to see if it works. if it does, then cool! i can compress my sites and make them faster and use less bandwidth. Lets hope this is the case. if not, well im then back to square one&#8230;

 [1]: http://weblogs.asp.net/tristank/archive/2005/01/12/351223.aspx