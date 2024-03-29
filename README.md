# Configuration buildroot
Cette configuration buildroot est destinée à supporter le système [Jukidbox](https://github.com/symac/jukidbox) dans sa version de 2020.

Fonctionne avec un raspberry pi 1. Pour un RPi2 voir [cet autre dépôt](https://github.com/symac/buildroot_jukidbox_pi2).

La configuration de base est largement inspirée du [tutoriel de C. Blaess](https://www.blaess.fr/christophe/buildroot-lab/index.html) (*Copie [internet archive](https://web.archive.org/web/20201214052606/https://www.blaess.fr/christophe/buildroot-lab/index.html)*).

## Image de démarrage
L'image de démarrage est affichée à l'aide de l'utilitaire ```fbv``` appelé depuis le script [custom-rootfs/etc/init.d/S21splashscreen](custom-rootfs/etc/init.d/S21splashscreen). La solution utilisée par défaut est d'afficher un fichier qui a été enregistré selon la méthode décrite dans l'article [Super fast Linux splashscreen](https://bootlin.com/blog/super-fast-linux-splashscreen/) (*[copie Internet Archive](https://web.archive.org/web/20201214053126/https://bootlin.com/blog/super-fast-linux-splashscreen/)*). Si l'on souhaite changer ce logo, le plus simple est de modifier le fichier ``S21splashscreen```` pour commenter l'appel actuel à fbv et utiliser l'autre option. 

# Notes pour la gération de l'image en 2023
- installation ubuntu 20.04 dans virtualbox
- installation de git / gcc / g++ / make / mercurial
- génération d'une image à partir de la configuration de ce dépôt
  
