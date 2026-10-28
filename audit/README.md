# osrd-jmr — Audit

## Objet

Dossier de travail local (`osrd-jmr`) : fork personnel du projet **OSRD**
(Open Source Railway Designer), maintenu sur le compte
`JMarianoIFSTTAR` (GitHub), destiné à des travaux de recherche du laboratoire
ESTAS (Université Gustave Eiffel) autour de la conception d'infrastructure
ferroviaire, la capacité, la grille horaire et la simulation.

Le dépôt est synchronisé avec l'amont OSRD (branche `dev`) sans modification
locale du code source : il sert de base d'étude et de développement.

## Structure (monorepo OSRD)

| Dossier | Rôle |
|---------|------|
| `core/` | Moteur de simulation / calcul de chemin (Kotlin/Gradle, modules `kt-osrd-*`) |
| `editoast/` | Backend d'API et de persistance (Rust), interface avec la base PostGIS |
| `front/` | Application web (React/TypeScript) |
| `gateway/` | Reverse-proxy d'authentification (Rust/actix) |
| `osrd_schemas/` | Schémas partagés (Python, génération de types) |
| `osrdyne/` | Ordonnanceur / couche intermédiaire (Rust) |
| `python/` | Outils Python (`railjson_generator`) |
| `tests/` | Jeux de données et tests d'intégration (Python) |
| `chart/` | Helm chart de déploiement Kubernetes |
| `docker/` + `docker-compose.yml` | Déploiement de la pile complète |

## État

- **Git** : branche `dev`, à jour avec `origin/dev` (0 commit en avance /
  0 en retard), copie de travail propre.
- **Remote** : `git@github.com:JMarianoIFSTTAR/osrd-jmr.git`.
- **CI** : workflows GitHub présents (`build.yml`, `pr.yml`, `release.yml`, …)
  — qualité, tests et images gérées par l'amont OSRD.
- **Build local** : non relancé lors de cet audit (pile Docker complète requise) ;
  état supposé conforme à l'amont `dev`.

> Les fichiers `README.md` / `ROADMAP.md` / `TODO.md` de ce dossier `audit/`
> reflètent le point de vue local (laboratoire) et ne remplacent pas le
> `README.md` d'amont situé à la racine du dépôt.
