# qualife-data

Fichiers de données publiques utilisés par [QuaLife](https://github.com/edouardlacroix/QuaLife), générés par le script ETL (`build_db.py`) à partir de sources INSEE / data.gouv.fr (Filosofi, IPS écoles/collèges, délinquance SSMSI, découpage géographique).

Chaque fichier est un JSON agrégé à une maille géographique :

- `iris.json` — quartiers (IRIS)
- `communes.json` — communes
- `departements.json` — départements
- `regions.json` — régions
- `france.json` — niveau national
- `communes-index.json` — index de recherche (codes postaux, noms)

Ce dépôt n'est qu'un point de publication : il est régénéré et republié à chaque mise à jour du pipeline ETL, pas édité à la main.
