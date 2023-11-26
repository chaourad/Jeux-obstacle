 # Simulation des Véhicules et d'Obstacles avec la bibliothèque p5.js

## Description
Ce projet est une simulation interactive en 2D mettant en scène des véhicules et des obstacles dans un environnement créatif. Utilisant p5.js, une bibliothèque JavaScript reconnue pour son potentiel artistique, le projet simule des véhicules capables de poursuivre des cibles, d'éviter des obstacles de manière dynamique et de suivre un leader. Cette simulation offre un aperçu captivant des comportements autonomes dans un espace bidimensionnel.


## Installation 

Pour installer et lancer ce projet sur votre machine, suivez ces étapes :

1. **Ouvrir un Terminal** : Sur votre ordinateur, ouvrez un terminal.

2. **Cloner le Projet** : Clonez le dépôt GitHub du projet en utilisant la commande :
   ```bash
   git clone https://github.com/chaourad/Jeux-obstacle.git
3. **Installer l'Extension Live Server** : Ouvrez Visual Studio Code. Si vous n'avez pas l'extension Live Server, installez-la. Pour cela, allez dans l'onglet des extensions, recherchez Live Server et cliquez sur installer.

4. **Ouvrir le Projet** :Dans Visual Studio Code, ouvrez le dossier du projet que vous venez de cloner.

5.  **Lancer le Projet** : Faites un clic droit sur le fichier index.html dans l'explorateur de fichiers de Visual Studio Code et sélectionnez Open with Live Server. Cela ouvrira le projet dans votre navigateur par défaut.

## Fonctionnalités

### Suivi du Leader
- **Leader Suivant la Souris** : Le leader suit le mouvement de la souris, utilisant un comportement de `seek` ou `arrive` pour se déplacer de manière fluide et réactive.
- **Queue leu leu** : Les véhicules suivent un point spécifique situé juste derrière le leader ou le véhicule qui les précède. Ce point est calculé en fonction de la position et de la direction du véhicule précédent, permettant ainsi une file ordonnée et organisée.

### Comportement d'Arrivée
- Les véhicules, à l'exception du leader, utilisent le comportement d'`arrive` pour se diriger vers un point derrière le véhicule qui les précède. Cela leur permet de maintenir une distance constante avec le leader tout en suivant son chemin.

### Comportement de Séparation
- **Évitement de Collision** : Un comportement de séparation est implémenté pour prévenir les collisions et les superpositions entre véhicules.
- **Contrôle Utilisateur** : Un curseur est fourni dans l'interface utilisateur pour permettre aux utilisateurs de régler dynamiquement la distance de séparation entre les véhicules, offrant ainsi une expérience interactive et personnalisable.

### Évitement de la Zone devant le Leader
- **Zone d'Évitement** : Une zone d'évitement est calculée et visualisée devant le leader, par un rayon de 40 pixels.
- **Réaction Dynamique** : Lorsqu'un véhicule (autre que le leader) pénètre dans cette zone, il active un comportement d'évitement (`evade`) pour s'éloigner rapidement de cette zone, assurant ainsi une navigation sûre et fluide.

### Comportement d'Évasion
- **Réaction à la Proximité** : Le comportement d'`evade` est utilisé comme l'inverse de `pursue`. Lorsqu'un véhicule se retrouve trop proche de la zone d'évitement devant le leader, il s'éloigne de ce point, évitant ainsi les collisions et les embouteillages.

## Démo


