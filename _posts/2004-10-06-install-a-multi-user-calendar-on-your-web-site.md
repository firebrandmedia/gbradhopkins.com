---
layout: post
title:  "Install a Multi-User Calendar on Your Web Site"
date:   2004-10-06 14-25-48 -0500
categories: Web Design Tutorials
---

A calendar that is editable by multiple users can be a great resource for businesses, churches, clubs or other groups that have a web site. In this tutorial I will show you how to add a free calendar to your web site.

Requirements: To use phpEventCalendar your web server must have MySQL and PHP installed.

Download: phpEventCalendar is free under the [GNU General Public Licence (GPL) agreement][1]. Visit [ikemcq web works][2] to download the necessary files. You will find four different files that are available for download. Make sure that you download the most recent version. It is only necessary that you download one of the files (either pec-0.2.tar.gz or pec-0.2.zip) and then any language files that you may need.

Let’s get started. Once you download the compressed phpEventCalendar file, decompress (unzip) it and copy it to your web site folder. I would also recommend that you now upload the entire phpEventCalendar folder to your web server.

While your calendar is uploading, you will need to create the MySQL database that it will use to maintain the events that will be added to the calendar. ![][3]My web server uses a very common User Interface called cPanel X. Using the Manage MySQL function I created a database for the calendar (called bbc_calendar). You may have to check the documentation for your web server to find out how to create a MySQL database.

Now that your database is created and your files are uploaded, you will edit the config.php file found in the phpEventCalendar folder. Open the config.php file in a text editor. There are four lines of code that need edited. They are found on lines 19 through 22.

define("DB_NAME", ""); // db name  
define("DB_USER", ""); // db username  
define("DB_PASS", ""); // db password  
define("DB_HOST", "localhost"); // db server

On each of these lines you will add information between the two quotes (""). DB Name will be the name of the database that you created (mine was bbc_calendar). DB Username will be the username that you use to log-in to your database (mine was the same as my login for my webserver). DB Password is the password you use to log-in and DB Server was left as is. The result should look like this:

define("DB_NAME", "calendar-database-name"); // db name  
define("DB_USER", "username"); // db username  
define("DB_PASS", "password"); // db password  
define("DB_HOST", "localhost"); // db server

Once you have edited the config.php file, save it and upload it to the phpEventCalendar folder on your web server.

Now that everything is uploaded, we need to test our installation. To do this, we will go to our web site and then point our browser to the createtables.php file, which is found in our phpEventCalendar folder.

http://www.yourwebserver.com/phpEventCalendar/createtables.php

If you have edited and uploaded everything correctly, you will see "Installation Complete. Click Here to view the calendar." If you see this message, congratulations, your calendar is installed properly. You can now click on Click Here to view the calendar.

Finishing Touches

Once you have reached your properly installed calendar, you should log-in (using the default: admin & password) and change the admin account name and password to something unique. You can also delete the createtables.php file off of your web server.

Working Sample: [Berkeley Baptist Church phpEventCalendar][4]

Adding Users

The beauty of phpEventCalendar is its ability to be administered by multiple users. Users can have two different levels of access,![][5] Administrator (which allows them to add & edit events and add other users) and Editor (which allows them to add & edit events but not add other users).

Adding Events

Once logged-in, adding events is a simple process. First, click on the number of the day that you would like to add the event to. This will open an Add New Event window. You then give the event a name that will be displayed on the calendar, type in a description of the event (optional) and add a start and finish time (optional) for the event and hit post.

Visitors can then click on the title of the event to see more details for each event.

This is the first in a four part series that will cover the installation and customizing of the phpEventCalendar. In part two, I will show you how to customize the calendar to match your web page. If you have any questions about the calendar, feel free to post them on the message board.

 [1]: http://www.gnu.org/copyleft/gpl.html
 [2]: http://www.ikemcg.com/scripts/pec/downloads.html
 [3]: http://gbradhopkins.com/images/webdesign/phpEventCalendar/manage-mysql.gif
 [4]: http://www.berkeleybaptistwv.net/phpEventCalendar/index.php
 [5]: http://gbradhopkins.com/images/webdesign/phpEventCalendar/addnewevent-window.gif

