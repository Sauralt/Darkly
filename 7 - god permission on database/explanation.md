# 7 - GOD PERMISSIONS ON DATABASE

## what is it

Privilege escalation is not a specific attack technique—it is an objective: obtaining higher privileges than those normally granted. It is often the consequence of another vulnerability (mass assignment, IDOR, unprotected endpoint, injection, etc.) rather than a separate technical category.

## how to access the flag

Now that we have the admin logs thanks to the XML injection, we can log in to http://localhost:8090/_/ using the information provided on the dashboard.

![god](Resources/god.png)

By logging in with the admin credentials, we access the database. We can then grant ourselves full permissions by setting our profile to "god" and modifying anything we want. By going to the "internal_audit" table, we directly find the flag.

![god](Resources/god2.png)

## how to fix the problem

Well, mostly the same as with XML, since the breach comes from it, but also prevent the server from accessing sensitive data from XML files.