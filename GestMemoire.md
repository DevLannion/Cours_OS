# Gestionnaire de mémoire

Le gestionnaire de mémoire permet de gérer la memoire globale de la machine et de la répartir pour les différentes taches en fonction de leurs besoins

## Reservation de la memoire pour les taches
Lors de l'initialisation des taches, le gestionnaire de tache va reserver une plage de memoire, qui ne sera utilisable que par cette tache.
La memoire reservée pour chaque tache comportera differentes zones :

- Code : contient le code executable du programme
- Pile : contient les données utiliséées par le programme pour stocker les données d'execution :
	- parametres de fonctions
	- pointeurs de retour
	- valeurs de retour
- Tas : zone de memoire libre utilisée pour stocker les variables du programme.

Chacune de ces zones sont référencees par des pointeurs

## Memoire et contexte de programme
Pour notre exemple, on peut considerer que la gestion des contexte se fera directement par l'OS, pour cela il devra reserver des registres qui serviront de references pour la gestion des contextes. 
Généralement la gestion de contexte est confiée a des composants spécifiques (MMU) qui permettent de gerer des zones de mémoire en assurant la protection d'usage de ces zones vis a vis des autres programmes.

## Composant gestionnaire de memoire
Sur certains systèmes, on peut avoir un composant qui gérera la mémoire a votre place (MMU), avec ce genre de composants la gestion de la memeoire est grandemen