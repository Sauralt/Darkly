# 1 - RESET PASSWORD

## what is it

The vulnerability comes from a flaw in the token: anyone can obtain this token and therefore the email address.
The token is returned to the user instead of being sent by email. If the link works instantly without an email, it means the proof-of-possession step has been removed. The server gives the key to whoever requests it, without verifying their identity.

## how to access the flag

By looking at the Benjamin forum, there is mention of a vulnerability:

![mdp11](Resources/mdp2.jpeg)

You just need to use the "forgot password" feature, enter the student's email, change the password, and log in with the new password.

![mdp22](Resources/mdp1.jpeg)

After logging into the student's account, the flag will be in their profile when you go to edit it.

## how to fix the problem

Use a more secure encryption system, add two-factor authentication, and limit the lifetime and number of requests in case of brute-force attempts.


