# Les Interruptions

Ce mécanisme correspond à des actions qui sont déclenchées par des évènements externes (I/O, Timers, ...)

## Différents types d'interruptions 
Suivant les machines le processeur dispose de differents types d'interruptions :

- matérielles
- logicielles

Les interruptions matérielles sont déclenchées par un signal électrique arrivant sur une broche du processeur.

Les interruptions logicelles sont déclenchées par des insctructions (cela permet souvent de donner la main à des routines systèmes depuis un programme).

## Différents mode de fonctionnement
Il existe différent mode de fonctionnement des interruptions :

- non masquable : ce sont des interruptions qui déclenchent une routine quel que soit l'état du système.
- masquables : les interruptions ne sont traitées que si le processeur le permet.