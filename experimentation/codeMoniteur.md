# Moniteur (Interpreteur de commandes)

exemple d'algorithme :

	Initialiser prompt="mon OS >"
	repeter indefiniment
		afficher prompt
		lire ligne de commande
		analyser ligne de commande
		si commande OK
			executer commande
		sinon
			message d'erreur
	fin repeter
	