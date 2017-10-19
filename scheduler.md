#Le Scheduler

## Qu'est ce que c'est
le scheduler est un process qui permet de donner la main aux différentes taches a exécuter en fonction d’un certain nombre de paramètres :

- priorité
- besoin d’execution ou non

## Son role
Il assure l'execution des process chacun leur tour, pour cela, 
il gère plusieurs listes :

- process en attente d’execution (taches actives)
- process actifs (taches en attentes d’événements externes ; I/O, timer, …)

## Comment ca marche
Le passage d’un process a l’autre se fait selon différentes méthode :

- un timer se déclenche régulièrement afin de forcer le changement de process.
- les taches rendent la main au système a la fin de chaque instruction et se remettent dans la liste d’attente
- il gere les contextes de chaque process