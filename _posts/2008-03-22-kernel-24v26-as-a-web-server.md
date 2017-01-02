---
title: Kernel 2.4V2.6 as a web server
author: admin
layout: post
permalink: /kernel-24v26-as-a-web-server/
categories:
  - Uncategorized
---
IBM has this article on how Kernel 2.6 fairs agenst 2.4 when it comes to web serving. 

> Many improvements have been made in the Linux 2.6 kernel to favor enterprise applications. This article presents results from the IBM Linux Technology Center&#8217;s Web serving testing efforts, comparing the Linux 2.4 and 2.6 kernels from various aspects. The highlights here are the key enhancements in the 2.6 kernel, the test methodologies, and the results of the tests themselves. Bottom line: the 2.6 kernel is much faster than 2.4 for serving Web pages, with no loss in reliability.

So to be a spoilsport, Kernel 2.6 manages to serve 5 times more web pages then 2.4 does. now the system they are using is no slouch either. 8 way PIII with 9Gb ram and 2Gb swap. its runing [Redhat 7.3][1] and has [Apache][2] 2.0.47.

 [1]: http://www.redhat.com
 [2]: http://www.apache.org