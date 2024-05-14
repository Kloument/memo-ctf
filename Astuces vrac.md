

Dans un url d'image ou autre du syle http://test.com/image.jpg

on peut ajouter n'importe quoi apres en rajoutant un # u genre :

http://test.com/image.jpg#.php

Cela nous renverra vers le lien en ignorant le # et ce qu'il y a derrière.
Il peut donc y avoir une faille, on peut ajouter le # et mettre  #.jpg pour faire croire au serveur s'il est mal configurer que l'extention est en .jpg. Cela peut etre utile dans un formulaire d'upload pour upload un reverse shell.
Ansi cela permet de bypass la secu si celle-ci est mal configuré.


* Penser à regarder les droits des dossiers ! --> possibilité de supprimer/remplacer des fichiers dont on à pas les droits mais qui sont dans le dossier dont on à les droits

