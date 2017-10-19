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

- A chacune des invocations du scheduler, on cherche la prochaine tache a executer et on prepare son environneemnt :
	- Restauration du contextes de la tache
	- Donner la main a la tache selectionnée dans la file d'attente d'execution, afin qu'elle puisse executer ce qu'elle a prevu de faire
	- Lorsque la taches rend la main au système, 2 cas se presentent :
		- Elle a fini ce qu'elle avait a faire, dans ce cas, le scheduler la replace dans la liste des taches actives
		- Elle n'a pas fini ce qu'elle avait a faire, elle est replacée en fin de la liste des taches actives
- Si plus aucune tache n'est en attente d'execution, le Scheduler utilise une tache spéciale (Idle) qui permet de ne pas arréter le système.
		
## Gestion des priorités
En général, tous les OS disposent d'un mécanisme de gestion des priorités de taches, cette priorité peux etre gérée de differentes manières :

- On execute toutes les taches située a un niveau de priorité avant d'éxécuter celles d'un niveau inférieur
- Des mécanismes compléméntaires peuvent etre mis en place afin d'afiner la gestion des priorités.
	- On peut executer des taches d'un niveau de priorité inferieur une fois sur n changement de taches
	- On peux augmenter le niveau de priorité des taches en attente d'execution
	- On peut reduire le niveau d'execution d'une tache qui vient de s'executer

On peut aussi prevoir un melange de toutes ces methodes

Il existe aussi des mécanismes plus complexes de gestion des priorités basés sur des seuils

- definir des seuil de priorités min et max ayant pour effet :
	- min : si le niveau de priorite d'une tache est en dessous de ce niveau elle ne s'executera que si plus aucune tache active n'est presente
	- max : si une tache est au dessus de ce niveau de priorite, elle s'executera sans rendre la main au scheduler jusqu'a ce qu'alle ai terminé ce qu'elle doit faire (utile pour des routines système qui ne doivent pas etre interrompues)