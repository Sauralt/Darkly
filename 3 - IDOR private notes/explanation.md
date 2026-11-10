# 3 - IDOR PRIVATE NOTES

## what is it

An IDOR is when an application uses an identifier supplied directly by the user (in a URL, form, or API request) to access a resource without verifying that the user is allowed to access that specific resource.

## how to access the flag

Without being logged into a user's account, it is possible to access the private notes of a staff member on the site.

![idor](Resources/idor.png)

On the forum, a staff member named Wil posted a message about maintenance. It is enough to view his profile to access the flag.

![idor2](Resources/idor2.png)

## how to fix the problem

Always verify permissions on the server side and monitor the most sensitive functions.