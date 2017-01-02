---
title: updated datatable stuff
author: admin
layout: post
permalink: /updated-datatable-stuff/
dsq_thread_id:
  - 26009435
categories:
  - Uncategorized
---
<div class="Section1">
  <p>
    I posted a bit of code yesterday to make a datable with misc data in it. But, while in bed, i remembered that it has to be sorted. So, this morning, after some reading of different sites, I managed to get it working. Make the following modification:
  </p>
  
  <p class="MsoNormal" style='margin-left:36.0pt;text-autospace:none'>
    <span style=';font-family:"Courier New"'>&nbsp; dt.DefaultView.Sort = &#8220;column1 desc&#8221;&nbsp;&nbsp;&nbsp;</span>
  </p>
  
  <p class="MsoNormal" style='text-autospace:none'>
    <span style=';font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; dt.AcceptChanges() <font color="green"><span style='color:green'>&#8216; accept the changes again, just in case</span></font></span>
  </p>
  
  <p style='margin-left:36.0pt'>
    <span style=';font-family:"Courier New"'>&nbsp; DataGrid1.DataSource = dt.DefaultView&nbsp; <font color="green"><span style='color:green'>&#8216; set the datasource of the datagrid to the new table</span></font></span>&nbsp;
  </p>
  
  <p>
    Place this code just after all loops and before the last dt.acceptchanges(). Actually remove that last dt.acceptchanges and past this code in. only problem for me is its sorting slightly wrong. Im going to see if I can fix this. I think I know whats wrong though. It sees my data as strings and there fore 99 is the first one, and 101 is somewhere afterwards. If you mod the code, check it out to see what I mean.
  </p>
</div>