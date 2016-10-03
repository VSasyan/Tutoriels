# Création de partition sur une clef USB

## Instructions

### Démarrage de `fdisk`

* Passer root : `su -`
* Démonter la clef si besoin : `umount /dev/sdb*`
* Lancer fdisk sur la clef : `fdisk /dev/sdb`

### Utilisation de `fidsk`

* Lister toutes les partitions en tapant `p`
* Supprimer les partitions en tapant `d` puis le numéro de la partition (1, 2, 3 ou 4)
* Créer une nouvelle partion en tapant `n` puis 
  * `p` pour une nouvelle partition primaire
  * `1` pour créer la première partition
  * ne rien rentrer deux fois pour créer une partition du premier au dernier cylindre
* Modifier la type de la partition en FAT32 : taper `t`, puis `1` et enfin `c`
* Ecrire toutes ses modifications en tapapnt `w`

### Finalisation

* Reformater la clef : `mkfs.vfat -F32 -v /dev/sdb1`

C'est terminé !

## Sources

https://openclassrooms.com/forum/sujet/formater-une-clef-usb-sous-linux-84377?page=2#message-4445845
https://openclassrooms.com/forum/sujet/formater-une-clef-usb-sous-linux-84377#message-4444889
