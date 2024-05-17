
Nmap est un outil de scan réseau très utilisé, c'est sans doute l'outil de scan réseau le plus connu.


### Avantages :

* Grande communauté
* Nombreuses fonctionnalité
* Documentations clair

### Inconvénients :

 * ?


### Syntaxe : 
* nmap {type de scan} {options} {machine cible}
###  `fas:Terminal` Commandes principales :

| Options                           | Utilité                                                                                                                                                            | Exemple Complet              |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------------------------- |
| -A                                | scan agressif (exhaustif ) sur l’hôte cible pour déterminer le système d’exploitation, les services disponibles et leurs versions, etc.                            | nmap -A {machin              |
| -O                                | détermine le système d’exploitation sur lequel tourne la machine cible                                                                                             | nmap -O {cible}              |
| -sV                               | détermine les versions des services disponibles sur l’hôte cible et trouve éventuellement  une vulnérabilité existante pour une version particulière d’un servic   |                              |
| -p {port}<br>-p {minport-maxport} | scan un port spécifique ou une plage de port                                                                                                                  <br> | nmap -p 80<br>nmap -p 21-100 |
| -oN output.txt                    | sauvegarde le résultat du scan dans un fichier output.txt sous le format de sortie normal                                                                          |                              |
| -p-                               | Scan tous les ports                                                                                                                                                | nmap -p- {cible}             |


### Nmap reconnait six états de port. Il s'agit de :

- **ouvert (open)** : une application accepte des paquets UDP ou des connexions TCP sur ce port. Trouver des ports ouverts est d'ailleurs le principal objectif du scan de port,
- **fermé (close)** : le port fermé reçoit et répond aux paquets émis par Nmap. Un port fermé est accessible, mais il n'y a pas d'application en écoute,
- **filtré (filtered)** : le dispositif de filtrage des paquets peut être des règles de routeurs filtrants, un pare-feu dédié ou un pare-feu logiciel,
- **non-filtré (unfiltered)** : cet état signifie simplement qu'un port est accessible, mais que l'outil est incapable de déterminer s'il s'agit d'un port ouvert ou fermé,
- **ouvert/filtré (open/filtered)** : les ports dont Nmap est incapable de déterminer s'ils sont des états ouverts et filtrés sont mis dans l'état open/filtered,
- **fermé/filtré (closed/filtered)** : lorsque Nmap est incapable de déterminer si un port est filtré ou fermé, il utilise l'état closed/filtered.

L'état fermé/filtré est seulement utilisé par le scan Idle qui est basé sur les identifiants de paquets IP.

