# 5 PATCH METHOD HTTP

## what is it

The principle of PATCH

In HTTP, methods have different roles for a resource:

GET: read
POST: create
PUT: replace an entire resource
PATCH: modify part of a resource (only certain fields)
DELETE: delete

Unlike PUT, which requires the full object, PATCH only affects the fields sent. This is exactly why it is a good candidate when looking for vulnerabilities: it encourages developers to write logic such as “I accept a subset of fields and apply them,” and this logic is often less strict than creation logic.

## how to access the flag

By going to /staff, an indication is left telling us to use PATCH on /api/profile.

![patch](Resources/patch.jpeg)

By entering this command in the terminal using the PATCH method instead of GET to modify the HTTP permissions in /api/profile:

```shell
curl -X PATCH http://localhost:4942/api/profile \
-H "Content-Type: application/json" \
-H "Cookie:YOUR_COOKIE" \
-d '{"role":"cadet"}'
```

The user becomes a cadet on the site, allowing access to the dashboard and the new flag.

![patch](Resources/patch2.png)

## how to fix the problem

Add a check to verify that the person performing the request is authorized to do so (for example, using a key or proper role validation).