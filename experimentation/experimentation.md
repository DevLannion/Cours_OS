#Experimentation

Cette page va vous permettre de mettre en place un environnement et des outils qui devrait vous permettre de réaliser un petit OS 

- [Emulateur de carte PC x86](emulateurX86.md)
- Debuggeur


##Liste des actions à réaliser

- La premiere des choses a faire, c'est de definir comment sera utilisé 'espace mémoire disponible pour votre "machine"
- vous devrez ensuite, ecrire les routines d'initialisations
	- [interruptions](initInterruptions.md)
	- [memoire](initMemoire.md)
	- ...
- ecriture des routines système :
	- [scheduler](codeScheduler.md)
	- [gestionnaire de taches](codeGestTaches.md)
	- [gestionnaire de la memoire](codeGestMemoire.md)
	- [moniteur](codeMoniteur.md)
	- ...
- écriture des premiers drivers 
	- [écran](driverEcran.md)
	- [clavier](driverClavier.md)
- ecriture des descripteurs correspondants
	- [écran](descripteurEcran.md)
	- [clavier](descripteurClavier.md)
- ...