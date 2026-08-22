# Architecture de Snake

## Vue d’ensemble

`Snake` est un mini-jeu navigateur construit autour d’un unique fichier `script.js` et d’un Canvas HTML5 créé dynamiquement au chargement de la page.

## Composants principaux

### Boucle de jeu

`refreshCanvas()` joue le rôle de boucle principale :

1. avance le serpent ;
2. vérifie les collisions ;
3. détecte la consommation d’une pomme ;
4. repositionne la pomme si nécessaire ;
5. efface et redessine le Canvas ;
6. programme l’itération suivante via `setTimeout()`.

### Serpent

La fonction constructrice `Snake` contient :

- `body` : tableau de coordonnées ;
- `direction` : direction courante ;
- `ateApple` : indicateur de croissance ;
- `draw()` ;
- `advance()` ;
- `setDirection()` ;
- `checkCollision()` ;
- `isEatingApple()`.

### Pomme

La fonction constructrice `Apple` contient :

- `position` ;
- `draw()` ;
- `setNewPosition()` ;
- `isOnSnake()`.

### Entrées clavier

`document.onkeydown` traduit les touches fléchées en directions et la barre d’espace en redémarrage.

### Rendu

Le score, le serpent, la pomme et l’écran de fin sont dessinés directement avec le contexte Canvas 2D.

## Flux simplifié

```text
window.onload
   ↓
init()
   ↓
refreshCanvas()
   ├── advance()
   ├── collision ? → gameOver()
   ├── apple ? → score + croissance
   ├── drawScore()
   ├── snake.draw()
   ├── apple.draw()
   └── setTimeout(refreshCanvas)
```

## Limites architecturales historiques

- toute la logique est imbriquée dans `window.onload` ;
- aucune séparation entre moteur, rendu et contrôles ;
- pas de gestion explicite d’états `playing` / `game-over` ;
- timing basé sur `setTimeout()` plutôt que sur une boucle de rendu dédiée ;
- anciennes APIs clavier via `keyCode` ;
- constantes du jeu codées directement dans le script.

## Architecture cible possible

```text
snake/
├── index.html
├── src/
│   ├── game.js
│   ├── snake.js
│   ├── apple.js
│   ├── renderer.js
│   └── input.js
└── tests/
```

Cette organisation cible reste une piste pédagogique et n’est pas implémentée dans le dépôt historique.
