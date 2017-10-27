#Emulateur de carte PC X86

Dans cette page nous vous proposons d'installer sur votre machine un
environnement permettant d'ecrire d'avoir une machine virtuelle correspondant a
une machine de type PC avec son BIOS (Basic Input Output System)


##QEMU

QEMU est un hyperviseur qui permet la simulation de matériel, en particulier il
peut émuler un PC x86\_64 : son processeur, BIOS, et différents périphériques.
Il se distingue de solutions plus connues (VirtualBox, Vmware) par sa capacité
à aussi émuler le processeur. Ce n'est pas très intéressant en terme de
performances, mais c'est très pratique pour le débug, et cela permet d'exécuter
du code pour un autre processeur que le processeur hôte.

##Chaîne de compilation

Pour produire le code machine à partir de sources C et assembleur, nous
utiliserons le compilateur et l'assembleur GNU : **gcc** et GNU **as**.


##Installation

suivant votre système d'eexploitation, voici les differentes procedures a suivre

- pour MAC :
	- brew install qemu
	- brew install gcc (s'il n'est pas déjà installé)

- pour Windows :
	- [Installateur QEMU](https://www.qemu.org/download/#windows)
	- [Chaîne de compilation GNU](https://sourceforge.net/projects/mingw/files/Installer/)

- pour Linux :
	- prendre gcc et qemu dans votre gestionnaire de paquet

##Test

- récupér le projet **[HelloWorld\_MBR](https://github.com/DevLannion/HelloWorld_MBR)**
- construire l'image boot.bin (`make`)
- démarrer un PC virtuel avec l'image dans le lecteur de disquette virtuel:

```
> qemu-system-x86_64 -fda boot.bin
```
