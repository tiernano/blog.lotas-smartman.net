---
title: Now thats a spam message!!!
author: admin
layout: post
permalink: /now-thats-a-spam-message/
dsq_thread_id:
  - 26005915
categories:
  - Uncategorized
---
I have started using [MDaemon][1] as a mail server for my network. i used it before, and its great, so im using it again. but using the spam filters are quite funny. i just got a peice of spam with the following rating:

&#8212;- Start SpamAssassin results 112.30 points, 5 required; 

* 1.9 &#8212; Sent with &#8216;X-Priority&#8217; set to high 

* 0.8 &#8212; From: does not include a real name 

* 2.7 &#8212; BODY: Claims you can be removed from the list 

* 0.2 &#8212; BODY: Talks about opting in (capitalized version) 

* 0.3 &#8212; BODY: Offers a limited time offer 

* 0.7 &#8212; BODY: Gives a lame excuse about why you were sent this spam 

* 0.3 &#8212; URI: URL of page called &#8220;remove&#8221; 

* 100.0 &#8212; From: address is in the user&#8217;s black-list 

* 1.1 &#8212; Subject is all capitals 

* 0.5 &#8212; Message has X-MSMail-Priority, but no X-MimeOLE 

* 1.7 &#8212; Subject has lots of exclamation marks 

* 1.2 &#8212; message body is 25-50% uppercase 

* 0.6 &#8212; Message looks like Outlook, but isn&#8217;t 

* 0.3 &#8212; AWL: Auto-whitelist adjustment 

&#8212;- End of SpamAssassin results

Now as you can see, it only got 112.3 as a result because the address is in the blacklist. but i also got one rated at 42.6 and there is no black list on that one!! i love [spamassassin][2]!

 [1]: http://www.mdaemon.com
 [2]: http://www.spamassassin.org