# Qu'est qu'un OS (Operating System)

## Qu'est ce que c'est
Ce terme désigne le logiciel intégré dans toute machine qui dispose d’un microprocesseur, et qui doit exécuter des programmes.

## Son rôle
l'OS permet de gérer tous les éléments matériels d'une machine afin de permettre aux programmes de s'exécuter dans de bonnes conditions.

## Comment ca marche
l’OS est constitué de plusieurs éléments indispensables :

- procédure d'initialisation:
	- initialisation de la mémoire
	- initialisation du matériel
	- initialisation des tables d’[interuptions](interruptions.md)
	- initialisation des [entrées-sorties](IO.md)
	- initialisation des listes de tâches
	- lancement des tâches système
	- …
- un [gestionnaire de mémoire](GestMemoire.md)
- un gestionnaire d'[entrées sorties](IO.md)
- un [gestionnaire de tâches](TaskManager.md)
- un [scheduler](scheduler.md) qui permet de gérer l'exécution des tâches


## Moniteur
Le [moniteur](moniteur.md) est un process un peu particulier qui doit permettre de communiquer avec l'OS, c'est un espèce de shell qui est généralement lancé à la fin de la procédure d'initialisation, il doit permettre de lancer quelques commandes de base afin de visualiser des informations du système, et/ou lancer des tâches. 