`ffuf` est un outil d'exploration de répertoires et de fuzzing sur les applications web. Il est conçu pour être rapide et flexible, avec de nombreuses options de personnalisation pour répondre aux besoins des testeurs de pénétration.

### `far:ThumbsUp`Avantages :

- Rapidité et efficacité dans l'exploration de répertoires.
- Grande flexibilité dans les options de personnalisation.
- Prend en charge de nombreux protocoles, notamment HTTP et HTTPS.
- Gestion intelligente des délais et de l'ajustement de vitesse en fonction des réponses.
- Options de filtrage avancées pour des résultats plus précis.

### `far:ThumbsDown`Inconvénients :

- Peut être difficile à configurer pour les débutants.
- Consomme beaucoup de ressources système lors de l'exécution de gros fuzzing.
- Ne prend pas en charge nativement la découverte de sous-domaines.

### `fas:PencilAlt`Syntaxe & Exemple :

**Syntaxe générale** : `ffuf -u URL -w WORDLIST [options]`
- Exemple : `ffuf -u http://example.com/FUZZ -w wordlist.txt -mc 200`
    - `-u http://example.com/FUZZ`: URL cible avec `FUZZ` en tant que point d'insertion.
    - `-w wordlist.txt`: Chemin vers la liste de mots.
    - `-mc 200`: Afficher uniquement les réponses avec le code de statut HTTP 200.

**Recherche sous-domaine (subdomains) :** 
```
ffuf -w subdomains.txt -u http://website.com/ -H “Host: FUZZ.website.com
```



### `fas:Terminal`Commandes principales :

|Options|Utilité|
|---|---|
|`-u` ou `--url`|Spécifie l'URL cible.|
|`-w` ou `--wordlist`|Chemin vers la liste de mots (obligatoire).|
|`-t` ou `--threads`|Nombre de threads à utiliser (connexions parallèles).|
|`-fs` ou `--follow-redirects`|Suit les redirections lors du fuzzing.|
|`-mc` ou `--match-status`|Filtrer les réponses par codes de statut HTTP.|
|`-ml` ou `--match-len`|Filtrer les réponses par longueur de réponse.|
|`-fc` ou `--filter-status`|Filtrer les réponses en excluant certains codes de statut HTTP.|
|`-fl` ou `--filter-len`|Filtrer les réponses en excluant certaines longueurs de réponse.|
|`-s` ou `--silent`|Mode silencieux, affiche uniquement les résultats positifs.|