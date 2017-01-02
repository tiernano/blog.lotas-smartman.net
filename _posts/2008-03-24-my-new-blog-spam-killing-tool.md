---
title: my new blog spam killing tool
author: admin
layout: post
permalink: /my-new-blog-spam-killing-tool/
dsq_needs_sync:
  - 1
categories:
  - Uncategorized
---
Ok. So a few days ago, my site was hit with a major amount of blog spam. Now I used to be able to just delete all spam coming from a single IP address, but now because my site is going though an ISA server, everything comes from the same IP address. So if I tried that, it would kill real comments too. So, the only way to distinguish the blog spam from real comments is via the comment author URL. So, after some hacking I have this piece of code for you: 

<p class="MsoNormal">
  <span lang="EN-IE">&nbsp;</span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size: 10.0pt; font-family: Courier New">&nbsp;&nbsp;&nbsp; <span style="color:blue">Private</span> <span style="color:blue">Sub</span> Button1_Click(<span style="color:blue">ByVal</span> sender <span style="color:blue">As</span> System.Object, <span style="color:blue">ByVal</span> e <span style="color:blue">As</span> System.EventArgs) <span style="color:blue">Handles</span> Button1.Click</span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size: 10.0pt; font-family: Courier New">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ListBox1.Items.Add(TextBox1.Text)</span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size: 10.0pt; font-family: Courier New">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; TextBox1.Text = ""</span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size: 10.0pt; font-family: Courier New">&nbsp;&nbsp;&nbsp; <span style="color:blue">End</span> <span style="color:blue">Sub</span></span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size: 10.0pt; font-family: Courier New">&nbsp;&nbsp;&nbsp; <span style="color:blue">Private</span> <span style="color:blue">Sub</span> Button2_Click(<span style="color:blue">ByVal</span> sender <span style="color:blue">As</span> System.Object, <span style="color:blue">ByVal</span> e <span style="color:blue">As</span> System.EventArgs) <span style="color:blue">Handles</span> Button2.Click</span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size: 10.0pt; font-family: Courier New">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span style="color:blue">Dim</span> sqltext <span style="color:blue">As</span> <span style="color:blue">String</span></span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size: 10.0pt; font-family: Courier New">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; sqltext = "delete from wp_comments where comment_author_url like &#8216;"</span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size: 10.0pt; font-family: Courier New">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span style="color:blue">Dim</span> sqltextend <span style="color:blue">As</span> <span style="color:blue">String</span></span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size: 10.0pt; font-family: Courier New">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; sqltextend = "';"</span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size: 10.0pt; font-family: Courier New">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span style="color:blue">For</span> i <span style="color:blue">As</span> <span style="color:blue">Integer</span> = 0 <span style="color:blue">To</span> ListBox1.Items.Count &#8211; 1</span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size: 10.0pt; font-family: Courier New">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; TextBox2.Text = TextBox2.Text & vbCr & sqltext & ListBox1.Items.Item(i).ToString & sqltextend</span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size: 10.0pt; font-family: Courier New">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span style="color:blue">Next</span></span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size: 10.0pt; font-family: Courier New">&nbsp;&nbsp;&nbsp; <span style="color:blue">End</span> <span style="color:blue">Sub</span></span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size: 10.0pt; font-family: Courier New; color: blue">&nbsp;</span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size: 10.0pt; font-family: Courier New">&nbsp;&nbsp;&nbsp; <span style="color:blue">Private</span> <span style="color:blue">Sub</span> TextBox1_KeyDown(<span style="color:blue">ByVal</span> sender <span style="color:blue">As</span> <span style="color:blue">Object</span>, <span style="color:blue">ByVal</span> e <span style="color:blue">As</span> System.Windows.Forms.KeyEventArgs) <span style="color:blue">Handles</span> TextBox1.KeyDown</span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size: 10.0pt; font-family: Courier New">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span style="color:blue">If</span> e.KeyCode = Keys.Enter <span style="color:blue">Then</span></span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size: 10.0pt; font-family: Courier New">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ListBox1.Items.Add(TextBox1.Text)</span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size: 10.0pt; font-family: Courier New">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; TextBox1.Text = ""</span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size: 10.0pt; font-family: Courier New">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span style="color:blue">End</span> <span style="color:blue">If</span></span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size: 10.0pt; font-family: Courier New">&nbsp;&nbsp;&nbsp; <span style="color:blue">End</span> <span style="color:blue">Sub</span></span>
</p>

<p class="MsoNormal">
  <span lang="EN-IE">&nbsp;</span>
</p>

<p class="MsoNormal">
  <span lang="EN-IE">Now, what does it do? Firstly, I should tell you what you need. So a form with 2 text boxes (textbox1 and textbox2). Textbox2 should be set to multiline = true. You need 2 buttons and a list box also. </span>
</p>

<p class="MsoNormal">
  <span lang="EN-IE">So, the code above allows you to either type or paste a URL you want to delete from your comments into textbox1, and either hit enter or click button1. This will add it to the list box and clear textbox1 for a new URL. Next, the button2 click event. </span>
</p>

<p class="MsoNormal">
  <span lang="EN-IE">When this is clicked, a SQL query is generated based around sqltext and sqltextend. So, the final things I do are just copy and paste this query that has been generated directly into the MySQL console application, and it deletes any comments that should be killed. Pretty simple. Hardest part is getting the list of comments. I have no idea how to get the comments directly, because of the way my system is set up. Sorry.</span>
</p>

<p class="MsoNormal">
  <span lang="EN-IE">So, for future plans, I am working on a place to store the URLs so you will have a list of URLs you should delete all the time. Also, connection to the SQL server that holds your wordpress DB may be on the cards. </span>
</p>

<p class="MsoNormal">
  <span lang="EN-IE">Final idea might be a reporting system where it would keep the list of comments that you have, and each time it is run, assuming it is connected to the SQL DB, it would log how many comments with each URL had been deleted, and you could have some sort of reporting system. </span>
</p>

<p class="MsoNormal">
  <span lang="EN-IE">Hopefully this helps someone. Its helping me at the moment. The storing of URLs is handy. Ohh, and a system for checking if a comment has already been added would be on the cards too.</span>
</p>