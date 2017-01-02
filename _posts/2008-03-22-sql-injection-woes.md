---
title: 'SQL Injection woes&#8230;'
author: admin
layout: post
permalink: /sql-injection-woes/
dsq_thread_id:
  - 26009137
categories:
  - Uncategorized
---
<div class="Section1">
  <p>
    <font size="3" face="Times New Roman"><span style='font-size:12.0pt'>I read an article in an IBM DB2 Magazine that has similar info. Looks like something that a lot of developers are going to have to work on fixing.</span></font>
  </p>
  
  <blockquote style='margin-top:5.0pt;margin-bottom:5.0pt'>
    <div>
      <div>
        <p>
          <font size="3" face="Times New Roman"><span style='font-size:12.0pt'>So I forgot to blog about the SQL Injection problems that I have come across.&nbsp; This certain one used SQL Injection to get into an admin side of a shopping cart website and made some changes to the payment parts and set the money to go to him/her.</span></font>
        </p>
        
        <p>
          <font size="3" face="Times New Roman"><span style='font-size:12.0pt'>The SQL Injection related to logging into a website with forms authentication with a Username and Password box.&nbsp; In Classic ASP you could see something like</span></font>
        </p>
        
        <blockquote style='margin-top:5.0pt;margin-bottom:5.0pt'>
          <p class="MsoNormal">
            <font size="3" face="Times New Roman"><span style='font-size: 12.0pt'>set adconn = Server.CreateObject(&ldquo;ADODB.Connection&rdquo;)<br /> set adRS = Server.CreateObject(&ldquo;ADODB.Recordset&rdquo;)&nbsp;<br /> adconn.Open connectionString<br /> strSQL = &ldquo;select * from tblUsers WHERE UserId = &lsquo;&rdquo; & Request.Form(&ldquo;username&rdquo;) & &ldquo;&rsquo; and Password=&rsquo;&rdquo; & Request.Form(&ldquo;password&rdquo;) & &ldquo;&rsquo;&rdquo;<br /> adRS.Open strSQL, adConn<br /> if adRS.EOF Then<br /> &nbsp;&nbsp; &lsquo; not a user authenticated<br /> else<br /> &nbsp;&nbsp; &lsquo; is a user authenticated<br /> end if</span></font>
          </p>
        </blockquote>
        
        <p>
          <font size="3" face="Times New Roman"><span style='font-size:12.0pt'>So if I put in the box &nbsp;junior&rsquo; or 1 = 1 &ndash;</span></font>
        </p>
        
        <p>
          <font size="3" face="Times New Roman"><span style='font-size:12.0pt'>So the statement would look like this:&nbsp; select * from tblUsers where UserId = &lsquo;junior&rsquo; or 1=1 &#8211; &#8216; and Password=&rsquo;passwordfield&rsquo;</span></font>
        </p>
        
        <p>
          <font size="3" face="Times New Roman"><span style='font-size:12.0pt'>Being that we used the double &#8211; SQL Server will only execute whether the UserId = junior or 1=1, which we all know that 1=1 so there will be a recordset coming back, and therefore it will be counted as authenticated.</span></font>
        </p>
        
        <p>
          <font size="3" face="Times New Roman"><span style='font-size:12.0pt'>Now this was a very simplistic example, and there are many more that are more complex, but it is fairly common to have situations like this where someone can get in and wreak some havoc. &nbsp;So please remember to use the ADODB.Command and ADODB.Parameter so that you do not run into the SQL Injection attacks that you can have with concatenated strings.</span></font>
        </p>
        
        <p>
          <font size="3" face="Times New Roman"><span style='font-size:12.0pt'>&nbsp;</span></font>
        </p>
      </div>
      
      <p class="MsoNormal">
        <font size="3" face="Times New Roman"><span style='font-size: 12.0pt'><img width="1" height="1" id="_x0000_i1025" src="http://blogs.msdn.com/benmiller/aggbug/90671.aspx" /></span></font>
      </p>
      
      <p class="ngrelatedlinks" align="right" style='text-align:right'>
        <font size="3" face="Times New Roman"><span style='font-size:12.0pt'><a href="http://services.newsgator.com/subscriber/Related.aspx?relurl=http%3a%2f%2fblogs.msdn.com%2fbenmiller%2farchive%2f2004%2f03%2f16%2f90671.aspx">Related&#8230;</a></span></font>
      </p>
    </div>
    
    <p class="MsoNormal">
      <font size="3" face="Times New Roman"><span style='font-size: 12.0pt'><br /> [<a href="http://blogs.msdn.com/benmiller/archive/2004/03/16/90671.aspx">Ben Miller Blog</a>]</span></font>
    </p>
  </blockquote>
</div>