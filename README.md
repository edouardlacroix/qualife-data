# qualife-data

Fichiers de données publiques utilisés par [QuaLife](https://github.com/edouardlacroix/QuaLife), générés par le script ETL (`build_db.py`) à partir de sources INSEE / data.gouv.fr (Filosofi, IPS écoles/collèges, délinquance SSMSI, découpage géographique).

Chaque fichier est un JSON agrégé à une maille géographique :

- `iris.json` — quartiers (IRIS)
- `communes-by-dept/{code_departement}.json` — fiches complètes des communes (écoles, IPS, délinquance, DVF...), une par département plutôt qu'un unique fichier national de ~60 Mo : le frontend n'a besoin que du département de la commune consultée à un instant donné (voir `lib/data.ts` dans le dépôt QuaLife, `loadCommuneShard`)
- `departements.json` — départements
- `regions.json` — régions
- `france.json` — niveau national
- `communes-index.json` — index de recherche (codes postaux, noms, population, IPS/délinquance résumés pour la carte nationale)

Ce dépôt n'est qu'un point de publication : il est régénéré et republié à chaque mise à jour du pipeline ETL, pas édité à la main.
