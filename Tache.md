# Tache

Une tache est un process definie dans le système, elle peut etre de diferents types :

- *utilisateur* : cela correspond a des programmes lancés par les utilisateurs de la machine
- *système* : ces taches sont utilisées par le système afin de faire fonctionner l'ordinateur.

Le système gère les taches grace a une structure de donnée la definissant

Le nombre de champ de cette base de donnée est variable d'un OS a l'autre, mais on retouvera le plus souvent les informations suivantes :

- Nom de la tache
- Niveau de priorité
- User
- Etat
- Contexte (emplacement en memoire, taille memoire, pointeur d'execution, ...)
- Durée d'execution
- ....

