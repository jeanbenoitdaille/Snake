# Roadmap pédagogique de Snake

Cette roadmap décrit des pistes d’évolution possibles du mini-jeu historique sans prétendre qu’elles sont déjà implémentées.

## Étape 1 — Stabilisation

- remplacer `keyCode` par `KeyboardEvent.key` ;
- corriger `ctx.Baseline` en `ctx.textBaseline` ;
- formaliser un état de jeu explicite ;
- empêcher les redémarrages multiples de lancer plusieurs boucles concurrentes.

## Étape 2 — Qualité de jeu

- accélération progressive ;
- pause/reprise ;
- écran de démarrage ;
- meilleur affichage du score ;
- conservation du meilleur score localement.

## Étape 3 — Architecture

- séparer modèle, rendu et contrôles ;
- extraire `Snake` et `Apple` dans des modules ;
- centraliser les constantes ;
- remplacer les fonctions constructrices par des classes modernes si souhaité.

## Étape 4 — Tests

Tester séparément :

- déplacements ;
- interdiction du demi-tour immédiat ;
- collisions ;
- croissance ;
- génération d’une pomme hors du serpent ;
- calcul du score.

## Étape 5 — Accessibilité et compatibilité

- commandes alternatives ;
- interface mobile/tactile ;
- messages lisibles par technologies d’assistance ;
- Canvas responsive.

## Statut

Roadmap prospective d’un projet d’apprentissage historique.
