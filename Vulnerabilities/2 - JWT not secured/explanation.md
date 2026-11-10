# 2 - JWT not secured

## What is it

The JSON Web Token is not secured, since we know the secret from the comments, we can use it to login without any password making the higher ranked members vulnerable. Even the website admins could do what they want since they have the secret.

## How to fix it
Adding a server side verification, separating the admin users of the secret from others users, shortening the token's life and make it less obvious to replicate and even better : NOT LEAK IT