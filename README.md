# Snake

Mini-jeu Snake historique développé en JavaScript avec l’API Canvas du navigateur.

## Fonctionnalités

- plateau Canvas créé dynamiquement ;
- déplacement du serpent sur une grille ;
- contrôle avec les flèches du clavier ;
- génération aléatoire de la pomme ;
- croissance du serpent après avoir mangé une pomme ;
- score affiché dans le Canvas ;
- collisions avec les murs et le corps du serpent ;
- écran « Game Over » ;
- redémarrage avec la barre d’espace.

## Concepts travaillés

Le projet manipule notamment :

- Canvas 2D ;
- événements clavier ;
- tableaux de coordonnées ;
- fonctions constructrices `Snake` et `Apple` ;
- méthodes et état d’objet ;
- `switch` ;
- collisions ;
- `Math.random()` ;
- boucle de jeu via `setTimeout()`.

## Fichiers

- `index.html` : page hôte ;
- `script.js` : logique complète du jeu.

## Exécution

Ouvrir `index.html` dans un navigateur moderne.

## Contrôles

- `←` : gauche ;
- `↑` : haut ;
- `→` : droite ;
- `↓` : bas ;
- `Espace` : recommencer.

## Limites historiques

Le code utilise notamment l’ancienne propriété clavier `keyCode` et regroupe toute la logique dans un seul fichier JavaScript. La propriété `ctx.Baseline` utilisée pour le texte n’est pas la propriété Canvas standard `textBaseline`.

Le projet reste un exercice d’apprentissage et n’est pas présenté comme un moteur de jeu ou une application de production.

## Documentation

- `docs/ARCHITECTURE.md`
- `docs/ROADMAP.md`

## Statut

Mini-projet d’apprentissage historique.

## Consolidation prévue

Candidat à une future intégration dans `learning-javascript/games/snake/`.
