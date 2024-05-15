
Outils simple permettant de chercher les répertoires d'un site web en fonction d'une wordlist


### `far:ThumbsUp`Avantages :

* simple d'usage
* 

### `far:ThumbsDown`Inconvénients :

 * peu de fonctionnalités avancées
 * pas de couleurs


### `fas:PencilAlt`Syntaxe  & Exemples : 
* `gobuster {mode} {options}`


```
gobuster dir -u http://example.com -w wordlist.txt -t 10
```

```
gobuster dns -d example.com -w wordlist.txt
```

```
gobuster s3 -w wordlist.txt
```

Modes disponibles :
* `dir`: Recherche de répertoires et de fichiers.
- `dns`: Recherche de sous-domaines.
- `s3`: Recherche de buckets S3 (AWS).
- `vhost`: Recherche d'hôtes virtuels.
###  `fas:Terminal` Commandes principales :

#### Options générales : 

| Options              | Utilité                                                         |
| -------------------- | --------------------------------------------------------------- |
| `-w` ou `--wordlist` | Chemin vers le fichier de liste de mots (obligatoire).          |
| `-u` ou `--url`      | URL de la cible (obligatoire dans les modes `dir` et `vhost`).  |
| `-t` ou `--threads`  | Nombre de threads à utiliser (nombre de connexions parallèles). |
| `-p` ou `--proxy`    | Utiliser un proxy (format `http://localhost:8080`).             |
| `-q` ou `--quiet`    | Mode silencieux (affiche uniquement les résultats).             |
| `-k` ou `--insecure` | Ignorer les vérifications des certificats SSL/TLS.              |
| `-x php`             | Chercher les extensions précisées après le -x                   |

### Options du mode `dir`

|Option|Utilité|
|---|---|
|`-x` ou `--extensions`|Extensions à rechercher (séparées par une virgule).|
|`-s` ou `--status`|Codes de statut HTTP à afficher (séparés par une virgule).|
|`-e` ou `--exclude-length`|Exclure les résultats basés sur la longueur de la réponse.|

### Options du mode `dns`

|Option|Utilité|
|---|---|
|`-d` ou `--domain`|Domaine cible (obligatoire).|
|`-r` ou `--resolver`|Résolveur DNS à utiliser (facultatif).|
|`-q` ou `--quiet`|Mode silencieux (affiche uniquement les résultats).|

### Options du mode `s3`

|Option|Utilité|
|---|---|
|`-f` ou `--format`|Format d'affichage (par exemple, `txt`, `json`).|
|`-q` ou `--quiet`|Mode silencieux (affiche uniquement les résultats).|

### Options du mode `vhost`

| Option               | Utilité                                                |
| -------------------- | ------------------------------------------------------ |
| `-w` ou `--wordlist` | Chemin vers le fichier de liste de mots (obligatoire). |
| `-u` ou `--url`      | URL de la cible (obligatoire).                         |
| `-t` ou `--threads`  | Nombre de threads à utiliser.                          |
| `-q` ou `--quiet`    | Mode silencieux (affiche uniquement les résultats).    |




