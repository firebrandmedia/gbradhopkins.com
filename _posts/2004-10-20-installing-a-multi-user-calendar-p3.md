---
layout: post
title:  "Installing a Multi-User Calendar (p3)"
date:   2004-10-20 07-51-49 -0500
categories: Web Design Tutorials
---

This is tutorial three (of what now looks like four) showing you how to install and customize a multi-user calendar on your web server/site. In this tutorial I will show you how to edit the CSS files to match the site calendar to your web site more exactly. For installation tips see tutorial 1 ([installing][1]) and 2 ([adding to your web page][2]).

As I recommended in part two of this tutorial, duplicate the .CSS files that you will be editing. For those unfamiliar with CSS, it is basically used to control the look (background, text, borders, links, roll overs, etc.) of the elements of your web page. It is especially useful because all of the styles for an entire web site can be contained within one or two files.

I would recommend using a CSS editor. I’m using Adobe GoLive CS, which has a built in CSS editor. The benefit of a program like this is that you can visually see how the changes you are making will look. Macromedia Dreamweaver, and most other commercial web page design programs have a CSS editor included. If you are hand coding, you can download a CSS editor. A quick [google search][3] will provide a number of results.



The CSS file that we will edit is default.css (see code below).

 

<STYLE TYPE="text/css">  


<!—  


/\*\*\*|\\*\*\*|\\*\*\*|\\*\*\*|\\*\*\*|\\*\*\*|\\*\*\*|\\*\*\*|\\*\*\*|\\*\*\*|\\*\*\*|\\*\*\*|\\*\*\*|\\*\*\*|\\*\*\*|\\*\*\*|\\*\*\*|\\*\*\*|\\*\*\*|\\*\*\*|\**  


\*\*\*|\\*\*\*|\\***| Formatting For Month Table and Text \*\*\*|\\*\*\*|\\*\*\*|\\*\*\*|\\*\*\*|\*\*  


\*\*\*|\\*\*\*|\\*\*\*|\\*\*\*|\\*\*\*|\\*\*\*|\\*\*\*|\\*\*\*|\\*\*\*|\\*\*\*|\\*\*\*|\\*\*\*|\\*\*\*|\\*\*\*|\\*\*\*|\\*\*\*|\\*\*\*|\\*\*\*|\\*\*\*|\\*\*\*|\**/  


  


A { font-family:arial, helvetica; color:#00F; text-decoration:underline }  


SPAN { font-family:arial, helvetica }  


TD { font-family:arial, helvetica }  


BODY { background-color:#FFF }  


  


/\**\*|\* month and year header at top of calendar \**\*|\*/  


.date_header { font-size:16px; font-family:arial, helvetica; font-weight:bold }  


  


/\**\*|\* color and size of calendar cells. \**\*|\*/  


.day_cell { background-color:#EDECD8; height:80; width: 95; }  


.empty\_day\_cell { background-color:#EEEEEE; height:80; width: 95; }  


.today_cell { background-color:#F5F4ED; height:80; width: 95; }  


  


/\**\*|\* day number in upper left corner of each cell \**\*|\*/  


.day_number { font-size:10px; font-family:verdana, arial, helvetica; color:#000 }  


  


/\**\*|\* title_txt is the text for each post on main page \**\*|\*/  


.title_txt { font-size:10px; font-family:verdana, arial, helvetica; color:#000 }  


.title_txt A:link { color:#00F; text-decoration:underline }  


.title_txt A:active { color:#00F; text-decoration:underline }  


.title_txt A:visited { color:#00F; text-decoration:underline }  


.title_txt A:hover { color:#00F; text-decoration:underline }  


  


/\**\*|\* time line under title text when event time given \**\*|\*/  


.time_str { font-size:9px; font-family:arial, helvetica }  


  


/\**\*|\* column headers or days of the week \**\*|\*/  


.column_header { background-color:#2663E2; font-size:12px; font-family:arial, helvetica; color:#FFFFFF; font-weight:bold }  


  


/\**\*|\* footprint text \**\*|\*/  


.footprint { font-size:10px; font-family:verdana, arial, helvetica; color:#000; font-weight:bold; }  


.footprint A { font-size:10px; font-family:verdana, arial, helvetica; color:#00F; font-weight:bold; }  


// end hiding—>  


</STYLE>  


As you can see in the code above, the different parts of the code indicate what will be effected by the changes that we make. (*note - Any of the items in the code above can be changed to suit your needs or purposes.*) We are going to focus specifically on the cells for the days of the week (see code below).

/\**\*|\* color and size of calendar cells. \**\*|\*/  


.day_cell { background-color:#EDECD8; height:80; width: 95; }  


.empty\_day\_cell { background-color:#EEEEEE; height:80; width: 95; }  


.today_cell { background-color:#F5F4ED; height:80; width: 95; }  


As you can see, we can change the background color, and the height and width of each of the different cells here.

*   .day_cell (these are the cells for the days of the month.) 
    *   .empty\_day\_cell (these are the cells that fill out the beginning and end of the month but are empty [no date].) 
        *   .today_cell (this is, well, todays cell.) </ul> 
            I want to make the cells match the color scheme of the site I am using it for ([Berkeley Baptist Church Calendar][4]) so I will leave the cell sizes as they are and focus on the background colors.
            
            If you are coding by hand and need the web color palette, you may want to visit the Visibone site for their [216-Color Webmaster’s Palette][5]. You can use it to find the colors you want, and simply type its value into the CSS code, in place of the bold text.
            
            .day_cell { background-color:#**EDECD8**; height:80; width: 95; }
            
            Here is the code for the colors that I chose:
            
            /\**\*|\* color and size of calendar cells. \**\*|\*/  
            
            
            .day_cell { background-color: #fffaf0; width: 95; height: 80 }  
            
            
            .empty\_day\_cell { background-color: #f5f5f5; width: 95; height: 80 }  
            
            
            .today_cell { background-color: #b0c4de; width: 95; height: 80 }
            
            Next, you’ll probably want to change the column header. This includes the blue header and the text for the days of the week. We can change the background color, font size, font family and font color.
            
            .column_header { color: #ffffff; font-size: 12px; font-family: arial, helvetica; font-weight: bold; background-color: #7cb3d2 }
            
            Some other items you may want to change are as follows:
            
            *   date_header - bold black text that indicates which month you are currently viewing. 
                *   day_number - the small number in the upper left of each day cell. 
                    *   title\_txt - the text that is displayed when a user adds an item to the calendar. You will probably want to edit the .title\_txt A:link, .title\_txt A:active, .title\_txt A:visited, and .title_txt A:hover code as well. </ul> 
                        As you can see from the before and after images (below) there are a number of changes that can be made by simply modifying a few lines of code in the default.css file.
                        
                        ![][6]
                        
                        ![][7]
                        
                        In the next part of this tutorial, we’ll modify the pop up windows that users see when logging in and viewing event information.
                        
                        Extra Resources:
                        
                        *   [Visibone 216-Color Webmaster’s Palette][5] 
                            *   [phpEventCalendar][8] </ul> </div>

 [1]: http://gbrad.firebrand-media.com/archives/2004/10/install_a_multi.html
 [2]: http://gbrad.firebrand-media.com/archives/2004/10/installing_a_mu.html
 [3]: http://www.google.com/search?q=css+editor&ie=UTF-8&oe=UTF-8
 [4]: http://www.berkeleybaptistwv.net/phpEventCalendar/
 [5]: http://www.visibone.com/colorlab/
 [6]: http://gbradhopkins.com/images/webdesign/phpEventCalendar/cal-old.gif
 [7]: http://gbradhopkins.com/images/webdesign/phpEventCalendar/cal-new.gif
 [8]: http://ikemcg.com/scripts/pec/index.html

