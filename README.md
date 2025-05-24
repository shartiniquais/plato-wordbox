# Comment utiliser

## Configuration

1. Télécharger Plato sur votre ordinateur via Google Play Jeux, par exemple.
2. Utiliser le fichier `bbox.py` pour sélectionner les coordonnées de la fenêtre de jeu (la grille de lettres).

Dans le fichier `manager.py` :

- `GRID_SIZE` : définit la taille de la grille (mettre `4` pour une grille 4x4, `5` pour une grille 5x5, etc.).
- `MIN_WORD_LENGTH` : définit la longueur minimale des mots que le bot recherchera.  
  Si vous souhaitez une longueur minimale supérieure à 4, il faudra créer un fichier `mots{taille}.txt` contenant uniquement des mots d’au moins cette taille.
- `BBOX` : spécifie les coordonnées de la grille, obtenues avec `bbox.py`.
- `WORDS_FILE` : peut être modifié pour utiliser une autre liste de mots.  
  Attention : `MIN_WORD_LENGTH` sert uniquement à choisir quel fichier texte sera lu.  
  Si vous changez `WORDS_FILE`, assurez-vous qu’il correspond bien à la longueur minimale définie.

## Lancer le bot

1. Lancez une partie dans le jeu.
2. Dès que la grille s’affiche, exécutez `manager.py` puis revenez rapidement sur le jeu pour que le bot puisse prendre une capture d’écran.
3. Assurez-vous que la grille est bien alignée avec la `BBOX` choisie.
4. Le bot analysera alors chaque caractère et identifiera tous les mots possibles.
5. Une fois l’analyse terminée, appuyez sur **Entrée** dans la console, puis retournez sur le jeu : le bot commencera à jouer automatiquement.

### Astuce

En cas de problème pendant que le bot déplace la souris, déplacer le curseur en haut à gauche de l’écran activera un **failsafe** qui terminera immédiatement le programme.
