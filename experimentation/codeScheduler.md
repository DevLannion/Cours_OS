# Scheduler (ordonnanceur de taches)


exemple d'algorithme :

	currentTache = null
	repeter indefiniment
		newTache = getNextActiveTache()
		si (currentTache != null)
			si currentTache non terminée
				pushActiveTache(currentTache)
			else
				pushSleepingTache(currentTache)
			finsi
		finsi
		currentTache=newTache
	fin repeter
	
	fonction getNextActiveTache()
		nextTache = tblActiveTache[0]
		boucle index sur nbval(tblActiveTache) - 1
			tblActiveTache[index+1] = tblActiveTache[index]
		fin boucle
		ptrLastActiveTache = index
		return nextTache
	fin fonction
	
	fonction pushActiveTache(tache)
		ptrLastActiveTache ++
		tblActiveTache[ptrLastActiveTache] = tache
	fin fonction
	
	fonction pushSleeplingTache(tache)
		ptrLastSleepingTache ++
		tblSleepingTache[ptrLastSleepingTache] = tache
	fin fonction
	
	