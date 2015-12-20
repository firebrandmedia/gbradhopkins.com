---
layout: post
title:  "Not Seeing any Google Custom Search Engine Results in Analytics?&nbsp; Here&#8217;s the Fix!"
date:   2016-12-10 17=21-59 -0500
categories: Web Design Tutorials
---

I’m a big fan of and use it on most all of the sites that I build.  I recently installed a [Google Custom Search Engine (CSE)][1] to a [site][2] of mine and was hoping to use Google Analytics to track the searches that were performed on the site in the Google CSE.  

The problem is that after a couple days, there were still no results.  It was off to the Google CSE Discussion Group to search for the answer - and I found it.

By the way, the Google CSE Discussion Group seems to not be monitored by anyone at Google or if it is, it’s not a priority to respond to queries.  But there are still answers to be found from fellow users.

The answer I found was to edit the Profile Settings in Google Analytics for the site in question.  Now, I’m going to assume that you’ve set **Site Search** to ‘Do Track Site Search.’  If you haven’t, do that.  Next, you need to add a Query Parameter to the parameters that are already in place (term,search,query).  The query parameter that you want to add is ‘q’ (see image). Now hit ‘Save Changes.’ 

![Picture 5.png][3]

That’s it.  Now, just wait for the results to be displayed in Google Analytics.

 [1]: http://www.google.com/sitesearch/
 [2]: http://www.inthepanhandle.com/
 [3]: http://www.gbradhopkins.com/archives/Picture%205.png

