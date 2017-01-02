---
title: Integrating Amazon Mechanical Turk into Windows Workflow Foundation
author: admin
layout: post
permalink: /integrating-amazon-mechanical-turk-into-windows-workflow-foundation/
dsq_thread_id:
  - 26015508
categories:
  - Uncategorized
---
[Amazon&#8217;s Mechanical Turk][1] is one of&nbsp;many services that Amazon&nbsp;offers to&nbsp;developers. This one is a little more interesting then EC2 or S3, but in a very different way. [EC2][2] and [S3][3] allow you to buy Computing Power, but Mechanical Turk allows you to buy Man hours. Let me explain a bit.

You create a HIT (Human Intelligence Task) which asks a user to do something. something that a computer may be possible to do, but a human would be better at (say&nbsp;reviewing a document as assigning it keywords, as the example does). Each HIT has an allotted completion time, price, and some other bits a pieces. once you say the HIT is accepted, the person on the other end gets paid for completing their task. 

Very simple, and yet extremely useful task. So, in the [article here][4], they talk about using [Windows Workflow Foundation][5] to map out what to do. Very cool, very interesting idea. </p> 

**Technorati Tags:** <a href="http://technorati.com/tag/programming" rel="tag">programming</a> &#8211; <a href="http://technorati.com/tag/Mechanical%20Turk" rel="tag">Mechanical Turk</a> &#8211; <a href="http://technorati.com/tag/Amazon%20AWS" rel="tag">Amazon AWS</a> &#8211; <a href="http://technorati.com/tag/Windows%20Workflow%20Foundation" rel="tag">Windows Workflow Foundation</a>

 [1]: http://www.amazon.com/Mechanical-Turk-AWS-home-page/b/ref=sc_fe_l_2/002-2787390-9969626?ie=UTF8&node=15879911&no=3435361&me=A36L942TSJ2AJA
 [2]: http://www.amazon.com/ec2
 [3]: http://www.amazon.com/s3
 [4]: http://developer.amazonwebservices.com/connect/entry.jspa?externalID=635&categoryID=56
 [5]: http://msdn2.microsoft.com/en-us/netframework/aa663328