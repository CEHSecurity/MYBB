MYBB
====
Guide to MyBB Forum Security 

Download: https://github.com/CEHSecurity/MYBB

About:
as a Hacker i always used Linux with plesk panel as we can login with SSH and Download a few Security Source code
to block attacks for example like bruteforce and other tools to crack cpanels passwords as we all know that plesk username
is <admin> all we need is the <password> of the user panel but we can block that on port 8880

OR

with mybb 50% of the time it is Plugins or source code that has the vulnerability for a attacker that want's to hack the
forum it will be easy since he could use a few things for example SQLi attack how this works is if u have a plugin 
he could go to a plugin on the domain /inc/plugins/cehsecurity.php?page=1; select SLEEP(5)-- for example or he could use SELECT * FROM mybb_users and then export the database from the website thats why we always deny plugins folder but even then if the folder has a deny all in htaccess there might be a form input in the site the attacker can use so say we have a valid form that connects to a database <input action="inc/plugins/cehsecurity.php" type = "text" class = "field_box"/> for me i use HTTPHeaders to see how it working so i would see if the site has a XSS in the form ?'"--></style></script><script>alert(1337)</script> if so the form might have a SQLi if not a XXE attack to use payloads 


