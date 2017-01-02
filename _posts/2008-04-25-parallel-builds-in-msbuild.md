---
title: Parallel builds in MSBuild
author: admin
layout: post
permalink: /parallel-builds-in-msbuild/
dsq_thread_id:
  - 26016550
  - 26016550
dsq_needs_sync:
  - 1
categories:
  - Uncategorized
---
SWEET! Scott Hanselman has a post on his blog showing you how to get [MSBuild to build in Parallel][1]. this could come in very handy. we have&nbsp;a machine here for building our projects on, and you could be talking 4 or 5 projects, if not more, all linked together. to enable parallel builds on them, it would speed up the build big time&#8230; especially concidering there are 2 quad core procs in this box! <img src="http://blog.lotas-smartman.net/wp-includes/images/smilies/icon_smile.gif" alt=":)" class="wp-smiley" />

 [1]: http://www.hanselman.com/blog/FasterBuildsWithMSBuildUsingParallelBuildsAndMulticoreCPUs.aspx