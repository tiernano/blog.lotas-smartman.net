---
title: HowTo add a new search engine to IE7
author: admin
layout: post
permalink: /howto-add-a-new-search-engine-to-ie7/
dsq_thread_id:
  - 26013487
categories:
  - Uncategorized
---
Ok. this is something i have wanted for a while (well 24 hours or so) now: how to add a new search engine to IE7. Well, its not all that hard, though if something goes wrong, your on your own! Sorry. Anyway, open regedit, and go to the HKEY\_LOCAL\_MACHINE/SOFTWARE/Microsoft/Internet Explorer/Search Scopes. Add a new Key named What ever you want it to be called. in there you need to add the following: a string named DisplayName. this is the name that is shown in the browser. a DWORD called SortIndex which should be 5 (but if you have extra engines already there it will be one up) and another string named URL with the URL of the search engine. the URL should be the results page, but where the keyword is entered, you should change it to %s. exit any IE windows that are open, open a new instance, and your new search engine will be there. it could be used for stuff like a search engine for [WikiPedia][1], [MSDN][2], [Google Groups][3], or anything for that matter. Hope this helps!

 [1]: http://www.wikipedia.org
 [2]: http://msdn.microsoft.com
 [3]: http://groups.google.com