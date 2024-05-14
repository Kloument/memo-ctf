

## Commandes principales :

``
```
sudo -l
find / -perm -u=s -type f 2>/dev/null

```


Voir les fichiers appartenant à un utilisateur en particulier 
`find / -user bob 2>/dev/null`


Lister tous les fichiers writables : 

`find / -type f -not -path "/proc/*" -not -path "/sys/*" -not -path "/home/death/*" -writable 2>/dev/null`
Spécification : 
qui ne sont pas dans /proc/*
qui ne sont pas dans /sys/*
qui ne sont pas dans /home/death/*
-writable = dans lesquels on peut écrire 