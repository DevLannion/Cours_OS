# Entrées / Sorties


## Gestionaire d'entrées / sorties
Le gestionnaire d'entrées / sorties s'occupe de l'interface entre les programmes et les périphériques, il gère une table décrivant l'ensemble des périphériques disponibes. Les programmes peuvent ainsi accéder à ces périphériques de façon simple, par l'intermédiaire de [drivers](#Drivers)
La table de gestionnaire de périphériquess sera donc une combinaison ([drivers](#Drivers), [descripteur](#Descripteurs)) qui décrira de façon complète et unique le périphérique concerné

les principales entrées / sorties que l'on trouve sur un système sont :

- écran
- clavier
- son
- disque
- mémoire
- réseau
- ....


## Drivers
Le Driver est un programme qui gère les intéractions entre un périphérique et le système ; par exemple la gestion d'un clavier.
Le driver offre de façon générique un certain nombre de fonctions pour accéder à ce périphérique : 

- init
- open
- close
- read
- write

Le driver sera spécifique pour chaque type de périphérique (composant). Par contre s'il y à plusieurs composants identiques dans le système, ce sera le même driver qui gèrera ce périphérique, la différence se fera par la sélection d'un [descripteur](#Descripteurs) différent.

Le nom du driver correspond généralement à la fonction générale fournie par le type de composant.

## Descripteurs
Le descripteur de périphérique contient les informations matérielles d'un périphérique donné, on peut avoir plusieurs descripteurs identiques, mais avec des données differentes, dans le cas ou on a plusieurs périphériques de même type dans un système.
exemple d'informations contenues dans un descripteur

- adresse physique du composant
- adresse mémoire de base
- taille du buffer de données
- interruption utilisée
- ...


Le nom du descripteur sera généralement lié au nom du composant associé, avec un eventuel numéro d'ordre s'il y en a plusisurs dans le système.