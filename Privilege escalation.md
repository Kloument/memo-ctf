

## Commandes principales :


| Commande                                                                                                   | Utilité + param                                                                                                |
| ---------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| `sudo -l`                                                                                                  | voir les commandes que l'on peut faire en tant que sudo sans être dans les sudoers                             |
| `find / -perm -u=s -type f 2>/dev/null`                                                                    | Pour trouver les SUID (à compléter)                                                                            |
| `find / -user bob 2>/dev/null`                                                                             | Voir les fichiers appartenant à un utilisateurs en particulier, ici bob                                        |
| `find / -type f -not -path "/proc/*" -not -path "/sys/*" -not -path "/home/death/*" -writable 2>/dev/null` | Voir tous les fichiers writables. Param : -not -path = qui ne sont pas dans un repertoire, par exemple /proc/* |
| `crontab -l`                                                                                               | Voir les crontab de l'user actuel                                                                              |
| `crontab -u bob -l`                                                                                        | Lister les crontab d'un user, ici bob. Demande souvent des doits élevés                                        |
| `cat /etc/crontab`                                                                                         | Affiche le fichier des crontab                                                                                 |



``

| Paramètre pour la commande find | Utilité                                                          |
| ------------------------------- | ---------------------------------------------------------------- |
| `-user`                         | Spécifier un user en particulier                                 |
| `-writable`                     | Chercher un fichier dans lequel l'utilisateur actuel peut écrire |
| `-not -path`                    | Exclure de la recherche un répertoire ex : "/proc/*"             |
| `2>/dev/null`                   | Rediriger les erreurs vers /dev/null                             |
| `-perm -u=s`                    | Fichiers qui à les perm SUID pour l'utilisateur actuel           |
