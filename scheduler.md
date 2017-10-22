#Le Scheduler

## Qu'est ce que c'est
Le scheduler est un process qui permet de donner successivement la main aux différentes tâches à exécuter en fonction d’un certain nombre de paramètres :

- priorité
- besoin d’exécution ou non

## Son rôle
Il assure l'exécution des tâches chacune leur tour, pour cela, 
il gère plusieurs listes :

- process en attente d’exécution (tâches actives)
- process en sommeil (tâches en attentes d’événements externes ; I/O, timer, …)

On peut concevoir d'avoir d'autres listes d'attentes

## Comment ca marche
Le passage d’un process à l’autre se fait selon différentes méthodes.

Deux modes de fonctionnements :

- Mode préemptif : la répartition du temps alloué a chaque tâche est fait en fonctions de critères ci dessous.
- Mode temps partagé : dans ce cas, un quota de temps est alloué a chaque tâche, une horloge gère le passage d'une tâche à l'autre.

A chacune des invocations du scheduler, on cherche la prochaine tâche à exécuter et on prépare son environneemnt :

- Restauration du contexte de la tâche
- Donner la main à la tâche suivante selectionnée dans la file d'attente d'exécution, afin qu'elle puisse exécuter ce qu'elle à prevu de faire
- Lorsque la tâche rend la main au système, 2 cas se présentent :
	- Elle a fini ce qu'elle avait à faire, dans ce cas, le scheduler l'enlève de la liste des tâches.
	- Elle n'a pas fini ce qu'elle avait à faire, elle est replacée en fin de la liste des taches actives.
	- Elle n'a pas fini ce qu'elle a à faire, mais elle est en attente d'un évènement extèrieur ; dans ce cas, elle est remise en fin de la liste des tâches en sommeil.
- S'il n'y à plus aucune tâche en attente d'exécution, le Scheduler utilise une tache spéciale (Idle) qui permet de ne pas arréter le système.
		
## Gestion des priorités
En général, tous les OS disposent d'un mécanisme de gestion des priorités de tâches, cette priorité peux être gérée de différentes manières :

- On exécute toutes les tâches située à un niveau de priorité avant d'éxécuter celles d'un niveau inférieur
- Des mécanismes compléméntaires peuvent être mis en place afin d'afiner la gestion des priorités.
	- On peut exécuter des tâches d'un niveau de priorité inferieur une fois sur N changements de tâches.
	- On peux augmenter le niveau de priorité des tâches en attente d'exécution
	- On peut réduire le niveau d'exécution d'une tâche qui vient de s'executer, cela va permettre de donner la main à des tâches de priorité plus faible lorsque le niveau de priorité de cette tâche descend en dessous de la priorité des tâches de priorité inférieure.

On peut aussi prevoir un melange de toutes ces methodes.

Il existe aussi des mécanismes plus complexes de gestion des priorités basés sur des seuils

- definir des seuils de priorités min et max ayant pour effet :
	- min : si le niveau de priorité d'une tâche est en dessous de ce niveau elle ne s'exécutera que s'il n'y a plus aucune tâche actives sur un niveau supérieur à ce seuil.
	- max : si une tâche est au dessus de ce niveau de priorité, elle s'exécutera sans rendre la main au scheduler jusqu'à ce qu'alle ai terminé ce qu'elle doit faire (utile pour des routines système qui ne doivent pas etre interrompues). Attention : il faut s'assurer que les tâches qui se retrouvent dans cet état disposent de mécanismes pour rendre la main, sinon, le système serait bloqué !

## Autres fonctions généralement traitées par le scheduler

- Gestion du temps d'exécution d'une [tache](Tache.md).
- Gestion des contextes.