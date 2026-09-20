# TP JavaScript - Tic Tac Toe

Dans ce TP, vous allez créer un jeu de morpion en JavaScript à partir d’une structure HTML et CSS déjà fournie.

Le but est de mettre en pratique la manipulation du DOM, les événements, les tableaux, les conditions et la logique de jeu, tout en respectant une bonne séparation entre HTML, CSS et JavaScript.

## Contenu déjà présent

Le fichier `index.html` contient déjà :

1. le titre de la page
2. le texte indiquant le joueur actif
3. un plateau 3x3 avec 9 cases vides
4. un espace pour afficher le message de victoire ou de match nul
5. un bouton `Rejouer` permettant de recommencer une partie

Votre mission consiste à relier ces éléments avec le code JavaScript pour obtenir un jeu pleinement fonctionnel.

Le fichier `styles.css` contient un style simple, suffisant pour tester votre logique sans perdre du temps sur le design.

## Conseils

- Commencez par la version de base avant de passer au mode sans fin
- Séparez clairement la logique du jeu et l’affichage dans le code
- Testez les cas de victoire et les cas de match nul
- Garde votre code lisible, organisé et facile à comprendre
- Vérifiez régulièrement le bon fonctionnement de chaque étape avant d’aller plus loin

## Consignes

### Partie 1 : réaliser le morpion “classique”

À partir de la structure déjà présente dans `index.html`, vous devez créer un jeu de morpion complet.

#### Étape 1 : préparer le jeu

- [ ] Définir les symboles des joueurs (par exemple : ❌ et ⭕)
- [ ] Ajouter un événement `click` sur chaque case
- [ ] Définir le joueur 1 comme joueur actif au début de la partie
- [ ] Afficher le joueur actif dans la zone prévue

#### Étape 2 : jouer une partie

- [ ] Quand un joueur clique sur une case vide, on place son symbole dans cette case
- [ ] Quand un joueur clique sur une case déjà remplie, rien ne se passe
- [ ] Si un joueur aligne 3 symboles en ligne, en colonne ou en diagonale :
  - [ ] Afficher `Le joueur X a gagné !`
  - [ ] Bloquer les clics sur le plateau
  - [ ] Activer le bouton `Rejouer`
- [ ] Si toutes les cases sont remplies sans gagnant :
  - [ ] Afficher `Match nul !`
  - [ ] Activer le bouton `Rejouer`
- [ ] Sinon, on change de joueur et la partie continue

#### Étape 3 : recommencer une partie

- [ ] Vider toutes les cases
- [ ] Revenir au joueur 1
- [ ] Réafficher le joueur actif
- [ ] Réinitialiser le message de jeu
- [ ] Vérifier que la partie peut recommencer normalement

> Rappel : la partie est gagnée lorsqu’un joueur aligne 3 symboles sur une ligne, une colonne ou en diagonale.

### Critères de validation du morpion classique

La version de base est considérée comme correcte si :

- les joueurs peuvent jouer chacun leur tour ;
- les cases déjà occupées ne peuvent pas être remplacées ;
- une victoire est détectée correctement ;
- un match nul est détecté correctement ;
- le bouton `Rejouer` réinitialise la partie ;
- le message affiché correspond à l’état du jeu.

## Partie 2 : mode “sans fin”

Une fois la version classique terminée, vous devez ajouter une variante plus avancée : le mode sans fin.

> Astuce : sauvegardez votre code actuel dans un fichier `tic-tac-toe-normal.js` avant de commencer cette partie.

### Règles du mode sans fin

- Chaque joueur ne peut avoir que 3 symboles visibles sur le plateau à la fois.
- Quand un joueur place son 4e symbole, le plus ancien de ses symboles est supprimé, la case se vide et le jeu continue.
- La partie s’arrête uniquement lorsqu’un des joueurs gagne.
- La grille ne peut pas être remplie, donc il n’y a pas de match nul dans ce mode.

### À retenir

- Le mode sans fin est plus complexe que le mode classique.
- Il faut gérer correctement l’ordre des coups et les suppressions de symboles.
- Il faut continuer à vérifier les conditions de victoire, sans dépendre d’une grille complètement remplie.

Bonne chance pour le TP !
