#IHM (Interface Homme Machine)

##Role
Les interfaces homme machine sont des logicels qui permettent a l'utilisateur d'intéragir avec la machine.

##Différents types
principaux types d'IHM :

- Le [Moniteur](moniteur.md) ou interpreteur de commande,
- un CLI (command Line Interpreter) plus communement appelé shell, il permet de lancer des commandes, de parcourir le système ; les shell les plus connus pour linux sont sh, csh, ksh et bash
- Il existe aussi des interfaces utilisateurs plus complexes utilisant un mode graphique.

##Fonctionnement
L'interface homme machine utilise des périphériques d'entrée/sorties spécifiques :

- un clavier, pour saisir les commandes a executer
- un écran, qui affiche les informations
- une souris pour les environnement graphique

##Commandes internes
Le shell offre généralement des fonctions de base d'interaction avec le système

- visualisation d'informations système
- communication avec les peipheriques
- lancement de nouvelles taches
- generation de nouvelles taches

##Interactions avec le système
les interfaces homme machine communiquent avec le système en utilisant les API fournies par l'OS, mais aussi en utilisant les commandes de bases fournies par le monieur 