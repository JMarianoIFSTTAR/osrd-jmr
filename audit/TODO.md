# TODO — Actions / corrections prioritaires

Checklist priorisée (P1 > P2 > P3) issue de l'audit du fork local OSRD.

## P1 — Fondations

- [ ] **Formaliser l'objectif du fork** : documenter (ex. `audit/PROJET.md`) la
      problématique de recherche et le périmètre d'utilisation de ce dépôt
      local, distinct du dépôt OSRD amont.
      *Effort : faible — à la main.*

## P2 — Reproducibilité & validation

- [ ] **Vérifier le build local complet** : lancer `docker compose up -d --build`
      une fois et consigner les éventuels écarts avec l'amont `dev`
      (état supposé conforme, non testé lors de l'audit).
      *Effort : moyen — dépend de la machine.*
- [ ] **Valider `flake.nix` / `process-compose`** : tester l'environnement Nix
      reproductible du labo comme alternative à Docker.
      *Effort : moyen.*
- [ ] **Définir un cycle de sync amont** : créer une note/script pour rebaser
      `dev` sur l'amont OSRD (aujourd'hui manuel, 0 divergence).

## P3 — Veille & contribution

- [ ] **Suivre les workflows CI** : surveiller `build.yml` / `pr.yml` et l'état
      des pipelines sur `origin`.
- [ ] **Préparer une contribution amont** : identifier un premier sujet
      (issue/PR) si un correctif ou une extension du labo est généralisable.
