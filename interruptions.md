# Les Interruptions

Ce mecanisme correspond a des actions qui sont déclenchées par des évènements externes (I/O, Timers, ...)

Suivant les machines le processeur dispose de differents types d'interruptions :

- matérielles
- logicielles

Les interruptions matérielles sont déclenchées par un signal électrique arrivant sur une broche du processeur

Les interruptions logicelles sont déclenchées par des insctructions (cela permet souvent de donner la main a des routines systemes depuis un programme)

Il existe different types d'interruptions :

- non masquable : ce sont des interruptions qui declencheront une routine quel que soit l'etat du systeme.
- masquables : les interruptions ne sont traitées que si le processeur le permet