# 6 - INJECTION XML

## what is it

The XML format allows the definition of entities: reusable shortcuts in a document, similar to variables. The XML standard also allows the declaration of external entities, which look for their content elsewhere — on the local disk or even on the network.

If an application parses an XML file provided by the user (upload, API call, SOAP flow, etc.) with a parser whose feature has not been disabled, the user can define their own external entities, and the parser will fetch what they point to. This is no longer just data; it is an instruction.

## how to access the flag

After discovering the vulnerability using the PATCH method, an indication is left by "Emilie" saying that the XML agenda is not valid server-side.

![XML](Resources/XML.png)

This clue tells us that we must perform an XML injection in the agenda. We therefore use another .xml file that extracts information from /internal/config (an indicator left in robots.txt and on the dashboard).

![XML](Resources/XML2.png)

EXAMPLE SCRIPT:
```xml
<?xml version="1.0"?>
<!DOCTYPE agenda [
<!ENTITY xxe SYSTEM "http://localhost:4942/internal/config">
]>
<agenda>
<event>
    <title>&xxe;</title>
    <date>2042-01-15</date>
</event>
</agenda>
```

After importing the file, we obtain the new flag, along with admin login information that will be useful right after.

![XML](Resources/XML3.png)

## how to fix the problem

Validate user inputs, disable the use of external XML files when unnecessary, use secure parsers to prevent malicious behavior, and avoid exposing too much information in error cases.