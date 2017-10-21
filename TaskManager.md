# Le Gestionnaire de taches

Ce module a pour mission de gerer les taches dans le systeme, sans se soucier de leur execution.

Il gere les files d'attente des taches :

- lorsque une nouvelle tache est lancée, il la place dans la file d'attente d'execution.
- Il gère aussi la reservation de la memoire via le [gestionnaire de memoire](GestMemoire.md)
- Il gère les taches en sommeil, et les reveillent lorsqu'un evenement qu'elle attend est arrivé ; a ce moment la, il deplace cette tache de la file d'attente sommeil vers la file d'attente d'execution.

Une [tache](Tache.md) est definie par une structure de donnée plus ou moins complexe en fonction des besoins.

## Son role
- Le gestionnaire de tache doit initialiser les files d'attente.
- Le gestionnaire de tache ne s'occupe pas de l'execution des taches, il gere uniquement l'initialisation des taches et la gestion des files d'attentes. 