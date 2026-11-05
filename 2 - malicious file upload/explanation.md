# 2 - INJECTION PHP ON PDP

## qu'est ce que c'est

Une injection se produit quand une application mélange des données fournies par l’utilisateur avec des instructions qu’elle exécute, sans séparer clairement les deux. L’interpréteur ne fait alors plus la différence entre “ce que le développeur a voulu” et “ce que l’utilisateur a écrit”.

## comment acceder au flag

apres avoir pu se connecter sur le compte, il suffit d'uploader un script en php dans la section pour uploader une photo de profil pour obtenir le flag

code test dans un fichier php : 

```php
<?php echo system('id'): ?>
```

![php](Resources/php.png)


## comment solutionner le probleme

vérifier le type de fichier (pas besoin d’un .pdf pour une pdp), et le contenu du fichier (notamment l'entête