# Moniteur (Interpreteur de commandes)

exemple d'algorithme :

	Initialiser prompt="mon OS >"
	repeter indefiniment
		afficher prompt
		lire ligne de commande
		analyser ligne de commande
		si commande = commande interne
			executer commande interne
		sinon
			chercher commande dans le PATH d'execution des commandes
			appeler startTache(Nom de la tache, priorité, ...)
	fin repeter
	
	
exemple de commandes internes à prévoir :

- help : permet de liste les commandes internes disponibles
- meminfo : affiche les tables de gestion de la memoire
- memcompact : lance la procedure de nettoyage de la memoire (garbage collector)
- taskinfo : affiche les tables des taches 
- ...