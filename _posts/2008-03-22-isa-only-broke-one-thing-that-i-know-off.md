---
title: 'ISA only broke one thing, that i know off&#8230;'
author: admin
layout: post
permalink: /isa-only-broke-one-thing-that-i-know-off/
categories:
  - Uncategorized
---
Right. In one way when i got [ISA Server][1] running infront of my network, i was kind of expecting something to go wrong. It usually does when i try something new, and this time there was no difference. Firstly, ISA is VERY Secure. This acutally took some time to figure out. my DNS queries where not going though and my connection to the internet was running very slow. I figured out that DNS is blocked by default, so after opening it, it works grand now. So, then i started forwarding ports. So i forwarded port 80 to my linux/apache server and told it to include http host info. after fixing the router to forard all port 80 traffic to the ISA box, i tried all my sites and they all worked. pretty sweet. but whats broke i hear you ask. Well, [The-hairy-one.com][2] is kind of broke. Its not majorly broke, just slightly. Its mainly to do with the [Regional][3] section of the site. Firstly, most of it wouldent load at all because high bit charters and normalisation checking was enabled. this ment that certin charicters where blocked. So, when you visited these before you just got an ISA 500 error. this is fixed, but now you get an error saying that a page was not found on dmoz.org. Now to do some hacking and see if i can get a better Open Directory Script&#8230;

 [1]: http://www.microsoft.com/isa
 [2]: http://www.the-hairy-one.com
 [3]: http://www.the-hairy-one.com/cgi-bin/pod.pl/Regional/