# 3 - IDOR PRIVATE NOTES

## qu'est ce que c'est

Une IDOR, c’est quand une application utilise un identifiant fourni directement par l’utilisateur (dans une URL, un formulaire, une requête API) pour accéder à une ressource, sans vérifier que cet utilisateur a le droit d’accéder à cette ressource précise.

## comment acceder au flag

Sans etre connecte sur le compte d'un utilisateur, on peux acceder aux notes prives d'un membre du staff du site.

![idor](Resources/idor.png)

dans le forum, un membre du staff (wil) a mit un message parlant d'une maintenance, il suffit de voir son profil pour acceder au flag

![idor2](Resources/idor2.png)


## comment solutionner le probleme

Toujours vérifier les autorisations côté serveur et surveiller les fonctions les plus sensibles.