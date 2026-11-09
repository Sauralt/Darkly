# 2 - MALICIOUS FILE UPLOAD

## qu'est ce que c'est

C’est ce qu’on appelle un “malicious file upload” menant à une RCE (Remote Code Execution), via une injection de commande une fois le fichier exécuté. C’est l’une des failles les plus critiques qui existent, car elle donne un accès direct au serveur, pas juste aux données.

## comment acceder au flag

apres avoir pu se connecter sur le compte, il suffit d'uploader un script dans la section pour uploader une photo de profil pour obtenir le flag

code test dans un fichier : 

```php
<?php echo system('id'): ?>
```

![php](Resources/php.jpeg)


## comment solutionner le probleme

vérifier le type de fichier (pas besoin d’un .pdf pour une pdp), et le contenu du fichier (notamment l'entête)