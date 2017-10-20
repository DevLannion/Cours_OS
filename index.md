# QU'est qu'un OS (Operating System)

## Qu'est ce que c'est
Ce terme désigne le logiciel intégré dans toute machine qui dispose d’un microprocesseur, et qui doit exécuter des programmes

## Son rôle
l'OS permet de gerer tous les éléménts matériels d'une machine afin de permettre aux programmes de s'executer dans de bonnes conditions.

## Comment ca marche
l’OS est constitué de plusieurs éléments indispensables :

- procedure d'initialisation:
	- initialisation de la mémoire
	- initialisation du matériel
	- initialisation des tables d’[interuptions](interruptions.md)
	- initialisation des [entrées-sorties](IO.md)
	- initialisation des listes de taches
	- lancement des taches système
	- …
- un [gestionnaire de memoire](GestMemoire.md)
- un gestionnaire d'[entrées sorties](IO.md)
- un [gestionnaire de taches](TaskManager.md)
- un [scheduler](scheduler.md) qui permet de gérer l'execution des taches
