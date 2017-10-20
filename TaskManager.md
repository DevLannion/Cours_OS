# Le Gestionnaire de taches

Ce module a pour mission de gerer les taches dans le systeme, sans se soucier de leur execution.

Il gere les files d'attente des taches :

- lorsque une nouvelle tache est lancée, il la place dans la file d'attente d'execution
- il gère les taches en sommeil, et les reveillent lorsqu'un evenement qu'elle attend est arrivé ; a ce moment la, il deplace cette tache de la file d'attente sommeil vers la file d'attente d'execution.

Une [tache](Tache.md) est definie par une structure de donnée plus ou moins complexe en fonction des besoins.

Le gestionnaire de tache doit également initialiser les files d'attente, avant de donner la main au [scheduler](scheduler.md)