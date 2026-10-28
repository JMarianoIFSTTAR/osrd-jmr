# ROADMAP — Perspectives d'amélioration / de développement

Perspectives pour l'utilisation et le développement du fork local OSRD.

## Court terme

- **Pérenniser le suivi amont** : définir une stratégie régulière de
  rebasage/synchronisation de `dev` avec l'amont OSRD pour rester à jour
  (aujourd'hui : manuel, 0 divergence).
- **Écrire la problématique de recherche** : formaliser l'objectif scientifique
  (capacité, STDCM, simulations) dans un document dédié, distinct du code.

## Moyen terme

- **Instrumenter les tests** : exploiter `tests/` et les fixtures OSRD pour
  valider des scénarios de recherche (import d'infrastructures, rolling stocks,
  STDCM) sans dépendre de la pile Docker complète.
- **Configurer un environnement Nix reproductible** : activer/valider
  `flake.nix` + `process-compose` pour un dev reproductible sur les machines du
  labo (alternative à Docker).

## Long terme

- **Contribution amont** : préparer d'éventuelles contributions (issues/PR) à
  OSRD si les travaux du laboratoire aboutissent à des correctifs ou extensions
  génériques.
- **Extension métier (si besoin)** : selon les besoins de recherche, prévoir
  des modules d'analyse (conflits, marges, alternatives) adossés à `core/` et
  `editoast/`, idéalement proposés à l'amont.
