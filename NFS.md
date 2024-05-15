Le NFS (Network File System) est un protocole de système de fichiers distribué

### Utilité :

* Partage de fichiers : Permet aux utilisateurs sur un réseau de partager des fichiers et des répertoires.


### Port(s) par défaut

* Utilise généralement le port 2049 (TCP et UDP)
*  111 (TCP et UDP), utilisé pour mapper les autres services RPC (Remote Procedure Call).


### Commandes principales : 

| Commandes                                                          | Utilité                                        |
| ------------------------------------------------------------------ | ---------------------------------------------- |
| `showmount -e <IP>`                                                | Affiche le système de fichier de l'IP précisée |
| `nmap -sV -p 111,2049 <target_ip>`                                 | Scan les ports du service NFS                  |
| `sudo mount -t nfs <target_ip>:/<share_name> /mnt/nfs`             | Monter un partage NFS (sans authentification)  |
| `nmap -p 111 --script=nfs-ls,nfs-statfs,nfs-showmount <target_ip>` | Donne des infos sur le NFS via nmap            |
