# Entrées / Sorties


## Gestionaire d'entrées / sorties
Le gestionnaire d'entrées / sorties s'occupe de l'interface entre les programmes et les périphériques, il gère une table décrivant l'ensemble des périphériques disponibes. Les programmes peuvent ainsi accéder a ces périphériques de façon simple, par l'intermediaire de drivers
La table de gestionnaire de fichier sera donc une combinaison (driver, descripteur) qui decrira de facon complete le périphérique concerné

les principales entrées / sorties que l'on trouve sur un systèmes sont :

- écran
- clavier
- son
- disque
- memoire
- reseau
- ....


## Drivers
Le Driver est un programme qui gère les intéractions entre un périphérique et le système ; par exemple la gestion d'un clavier.
Le driver offre un certain nombre de fonctions standard pour accéder a ce périphérique : 

- init
- open
- close
- read
- write

On trouvera un driver par type de périphérique. Le driver sera spécifique pour chaque type de périphérique. 

Le driver utilise les informations du descripteur pour différentier les différents périphériques de même type

## Descripteurs de périphériques
Le descripteur de périphérique contient les informations matérielles d'un périphérique donné, on peut avoir plusieurs descripteurs identiques, mais avec des données differentes, dans le cas ou on a plusieurs périphériques de même type dans un système.
exemple d'informations contenues dans un descripteur

- adresse physique du composant
- adresse mémoire de base
- taille du buffer de données
- interruption utilisée
- ...