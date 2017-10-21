# Gestionnaire de mémoire

Ce module permet de gérer la mémoire globale de la machine et de la répartir pour les différentes taches en fonction de leurs besoins. 

## Reservation de la memoire pour les taches
Lors de l'initialisation des [tâches](#Tache.md), le [gestionnaire de tâches](TaskManager.md) va réserver une plage de mémoire, qui ne sera utilisable que par cette tâche.
La mémoire réservée pour chaque tâche comportera différentes zones :

- Code : contient le code exécutable du programme
- Pile : contient les données utiliséées par le programme pour stocker les données d'exécution :
	- paramètres de fonctions
	- pointeurs de retour
	- valeurs de retour
- Tas : zone de mémoire libre utilisée pour stocker les variables du programme.

Chacune de ces zones sont référencees par des pointeurs.

## Mémoire et contexte de programme
Pour notre exemple, on peut considérer que la gestion des contextes se fera directement par l'OS, pour cela il devra réserver des registres qui serviront de références pour la gestion des contextes. 

## Composant gestionnaire de memoire
La gestion de contexte peut aussi être confiée à des composants spécifiques (MMU), qui permettent de gérer des zones de mémoire en assurant la protection d'usage de ces zones vis à vis des autres programmes. Cette solution facilite grandement la gestion de la mémoire, en garantissant une isolation forte des zones mémoire entre elles.