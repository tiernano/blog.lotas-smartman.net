---
title: All my spam should now be cleaned out of Comments
author: admin
layout: post
permalink: /all-my-spam-should-now-be-cleaned-out-of-comments/
dsq_thread_id:
  - 26015395
  - 26015395
categories:
  - Uncategorized
---
Finally, i got around to cleaning my comments system. I get a lot of spam, so with the help of the [Akismet .NET 2.0 API][1], about half an hour of coding and some patients, i managed to build an app that will query my SQL server asking for all unmoderated comments, run them though [Akismet][2], and then say if they are spam or not. There is some minor checking on my end (i get a SQL query from the app, which i run, look at the results, decided to delete, and then do so). the only reason i havent told it to delete the comment or not is because it found some false positives, and some true negitives (is that a word?) its found at least 1 comment which was not spam to be spam, and 4 or 5 spam comments and said they where grand. i have submitted them to be checked, but they are not showing up just yet. So far, so good! <img src="http://blog.lotas-smartman.net/wp-includes/images/smilies/icon_smile.gif" alt=":)" class="wp-smiley" />

 [1]: http://www.codeplex.com/AkismetApi
 [2]: http://www.akismet.com