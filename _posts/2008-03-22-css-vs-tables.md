---
title: CSS Vs Tables
author: admin
layout: post
permalink: /css-vs-tables/
dsq_thread_id:
  - 26004053
categories:
  - Uncategorized
---
Hmmmm. I know im using tables on my sites at the moment, but i plan to learn

CSS. It makes site load quicker, its easer to under stand, and its also east to

do as Don says in this post, make 2 or 3 styles of the page. for example: Don

mentions a copy for printing and one for screen. you could also have one for

small screens like the [Sony P800][1]

or the [Nokia][2]

[7650][3],

[9210][4], etc. You could have one for

Opera, IE, Mozilla, etc. So instead of writing for 6 or so different

browsers/platforms, you only have to write one main one and some CSS files too.

<table cellSpacing="0" cellPadding="0" width="100%" bgColor="#cccccc" border="0" id="table1">
  <tr>
    <td style="font-family: Verdana,Sans-serif; font-size: 10pt">
      <p>
        <a class="black" href="http://DotNetWebLogs.com"><b>Feed: </b>Aggregated</p> 
        
        <p>
          posts from .NET Weblogs</a>
        </p>
        
        <p>
          &nbsp;<a class="black" href="http://dotnetweblogs.com/DonXML/posts/5101.aspx"><b>Title:</p> 
          
          <p>
            </b>Pet Peeve . Using HTML Tables to Control Web Page Layout</a> </td> 
            
            <td align="right" style="font-family: Verdana,Sans-serif; font-size: 10pt">
              <p>
                <b>Author: </b>Don XML&nbsp;
              </p>
              
              <p>
                &nbsp;</td> </tr> 
                
                <tr bgColor="#666666" height="1">
                  <td colSpan="2" style="font-family: Verdana,Sans-serif; font-size: 10pt">
                    &nbsp;
                  </td>
                </tr></table> 
                
                <table cellSpacing="2" cellPadding="2" width="100%" border="0" id="table2">
                  <tr>
                    <td style="font-family: Verdana,Sans-serif; font-size: 10pt">
                      <p>
                        <font face="Tahoma" size="2">I haven.t seen much on this topic in the</p> 
                        
                        <p>
                          .Net world, but I thought I.d throw it out there.&nbsp; A while back I
                        </p>
                        
                        <p>
                          finally moved from the Table camp to the CSS camp for controlling the
                        </p>
                        
                        <p>
                          layout of web pages.&nbsp; Seems like most of the .Net world still lives in
                        </p>
                        
                        <p>
                          the Table camp, and it bugs me that VS.Net encourages it.&nbsp; Does anyone
                        </p>
                        
                        <p>
                          else have a problem with this?&nbsp; Create an HTML using Tables to control
                        </p>
                        
                        <p>
                          the layout (or pull it down from
                        </p>
                        
                        <p>
                          <a style="color: #66c; text-decoration: none" href="http://www.donxml.com/TableLayout.htm"></p> 
                          
                          <p>
                            here</a>), and then view it in the Design window.&nbsp; Now do the same using
                          </p>
                          
                          <p>
                            Divs with CSS (or get it from
                          </p>
                          
                          <p>
                            <a style="color: #66c; text-decoration: none" href="http://www.donxml.com/CssLayout.htm"></p> 
                            
                            <p>
                              here</a>).&nbsp; Looks terrible, and is impossible to edit in the design
                            </p>
                            
                            <p>
                              window (not that I do that, but for newbies I can see them using it).&nbsp;
                            </p>
                            
                            <p>
                              Now look at the actual code for each example.&nbsp; Isn.t the CSS version
                            </p>
                            
                            <p>
                              much easier to read and create?&nbsp; It does a much better job separating
                            </p>
                            
                            <p>
                              the look and feel of the web page from the process that created it.&nbsp;
                            </p>
                            
                            <p>
                              Plus it lets the browser decide what the natural flow for the device
                            </p>
                            
                            <p>
                              that the page is displayed on.&nbsp; </font>
                            </p>
                            
                            <p>
                              <font face="Tahoma" size="2">One added bonus of using CSS instead of</p> 
                              
                              <p>
                                tables.&nbsp; Printing.&nbsp; You don.t need a printer pretty version of each and
                              </p>
                              
                              <p>
                                every page.&nbsp; Instead you create 2 separate Styles (either in line or as
                              </p>
                              
                              <p>
                                a link) and use the media option.&nbsp; The default media option is .all.,
                              </p>
                              
                              <p>
                                but you can set them to .print. or .screen., and thus have 2 different
                              </p>
                              
                              <p>
                                styles, one for the screen and one for the printer.&nbsp; And you don.t have
                              </p>
                              
                              <p>
                                to change your content at all, just set the divs that you don.t want
                              </p>
                              
                              <p>
                                rendered set to display:none.</font>
                              </p>
                              
                              <p>
                                <font face="Tahoma" size="2">For more cool CSS tips and tricks check</p> 
                                
                                <p>
                                  out Eric Meyer.s
                                </p>
                                
                                <p>
                                  <a style="color: #66c; text-decoration: none" href="http://www.meyerweb.com/eric/css/edge/"></p> 
                                  
                                  <p>
                                    site </a>(and while you are at it, buy his
                                  </p>
                                  
                                  <p>
                                    <a style="color: #66c; text-decoration: none" href="http://search.barnesandnoble.com/booksearch/isbnInquiry.asp?isbn=073571245X&#038;itm=1"></p> 
                                    
                                    <p>
                                      CSS book</a>)..</font>
                                    </p>
                                    
                                    <p>
                                      <font face="Tahoma" size="2">Don XML</font></td> </tr> </table
                                    </p>

 [1]: http://www.sony-ericsson.com/p800
 [2]: http://www.nokia.com
 [3]: http://www.nokia.com/phones/7650
 [4]: http://www.nokia.com/phones/9210