# 4 API ENDPOINT ACCESS

## qu'est ce que c'est

Une API expose des points d’accès (endpoints) qui permettent de lire ou modifier des données. Un endpoint non protégé, c’est une route qui exécute une action ou renvoie des données sans vérifier que l’appelant en a le droit — voire sans vérifier qui il est du tout.

C’est une faille de contrôle d’accès, cousine de l’IDOR : l’IDOR concerne quelle ressource précise tu peux toucher, l’endpoint non protégé concerne si tu peux appeler la route du tout.

## comment acceder au flag

en etant connecte a un utilisateur student, on peux acceder en trouvant des indices donnes dans le projet dont robots.txt lorsque l'on met un invalid path.

![api](Resources/api.png)

en allant sur /api/grades et en regardant un peu les informations, on trouve un nouveau flag

 ![api](Resources/api2.jpeg)

## comment solutionner le probleme

Bloquer l'accès à ceux qui ne devraient pas l’avoir (via une clé, un rôle protege comme il faut etc)