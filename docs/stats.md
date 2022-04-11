# Stats

La colonne `stats` est générée de la manière suivante :
- l'action `scans.yml` fait appel à la Github Action du repository `betagouv/check-url-action@main` (cf. [Job "Stats page"](../.github/workflows/scans.yml))
    - à partir des paramètres `baseUrl` et `uri`, l'action appelle la route `[url]/[uri]` (cf. [stats-action](https://github.com/betagouv/check-url-action/blob/main/src/index.js))
    - un fichier `stats.json` est généré, comprenant la note attribuée à cette URL selon certains critères (URI standard, réponse de l'API, etc.)