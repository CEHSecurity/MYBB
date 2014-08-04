MYBB
====
Guide to MyBB Forum Security 

Download: https://github.com/CEHSecurity/MYBB

About:
as a Hacker i always used Linux with plesk panel as we can login with SSH and Download a few Security Source code
to block attacks for example like bruteforce and other tools to crack cpanels passwords as we all know that plesk username
is <admin> all we need is the <password> of the user panel but we can block that on port 8880

OR

with mybb 70% of the time it is Plugins or source code that has the vulnerability for a attacker that want's to hack the
forum it will be easy since he could use a few things for example SQLi attack how this works is if u have a plugin 
he could go to a plugin on the domain /inc/plugins/cehsecurity.php?page=1; select SLEEP(5)-- for example or he could use SELECT * FROM mybb_users and then export the database from the website thats why we always deny plugins folder but even then if the folder has a deny all in htaccess there might be a form input in the site the attacker can use so say we have a valid form that connects to a database <input action="inc/plugins/cehsecurity.php" type = "text" class = "field_box"/> for me i use HTTPHeaders to see how it working so i would see if the site has a XSS in the form ?'"--></style></script><script>alert(1337)</script> if so the form might have a SQLi so for example if the form give a output of /search.php?q=search then i would use the simple /search.php?q=<script>alert("XSS")</script> then would bring a javascript popup with the text XSS always check forms as we could easy check if that form has a XSS or SQLi /search.php?q=SELECT * FROM mybb_users so if u want to stop forum being hacked try to check the PHP plugins script over if u are not good with PHP and Security then Hire somone to check the script for a Vulnerable with in script when i was working with mybb open source there always new 0days for the Mybb open source thats why we always check online to see if there any new SQLi for the mybb source but mybb.com security team are always on top of there so even then always check mybb website for new update on the open source if i was u i would not download a lot of plugins i would stick with what u need for example with my forum i have tabbed menu and plugins from http://mybbcentral.com/ as it all good do not use plugins if there been a leaked of it as it could have backdoors developed in them so then it would be easy :) 

