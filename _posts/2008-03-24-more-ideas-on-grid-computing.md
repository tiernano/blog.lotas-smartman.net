---
title: more ideas on Grid computing
author: admin
layout: post
permalink: /more-ideas-on-grid-computing/
dsq_thread_id:
  - 26015685
  - 26015685
categories:
  - Uncategorized
---
I know i keep going <a class href="http://blog.lotas-smartman.net/archive/2007/03/04/alchemi-net-based-enterprise-grid.aspx">on</a> and <a class href="http://blog.lotas-smartman.net/archive/2007/03/11/grid-computing-why-i-want-to-play-with-this.aspx">on</a> about this Grid computing idea, but its a really intriguing idea. the way i see it is that it enables both developers to get the most from their applications, and users to get the most from their hardware. So, my newest idea on how to use this is on the server backend. specifically, my server backend. the main place i see this being extreamly handy is the photography site. so, photos are uploaded to the photography site, with some data about those photos (keywords/tags). once the photos are uploaded, they are processed. Processing envolves resizing to different widths and also extracting meta data. then uploading the metadata and the photos to Amazon&#8217;s [S3][1], with the photo data (including meta data) also going to the SQL server. the reason for placing in both <a class href="http://www.amazon.com/s3">S3</a> and [Microsoft SQL Server][2] is backup. if the SQL copy goes away, i still have the [S3][1] data and can rebuild. 

So, this is where the extra processing horse power would come in handy. its not thats its needed, as such, but having 7 or 8 threads running at a time would speed things up conciderably. mind you, i would still be limited to my pipes upload connection, but, it should be still faster. And if i add machines to the grid that have their own internet connection&nbsp;(my sisters machine, a Virtual server externally, An Amazon <a class href="http://www.amazon.com/ec2">EC2</a> instance&#8230;) life would be even better. 

now to work out how to get it to work&#8230;

 [1]: http://www.amazon.com/S3
 [2]: http://www.microsoft.com/sql