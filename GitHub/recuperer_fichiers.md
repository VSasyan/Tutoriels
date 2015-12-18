Récupérer les fichiers d'un git
==============================

Pourquoi
--------

Il peut-être intéressant de récupérer uniquement les fichiers stockés sur le git et non pas l'historique, dans le `.git` (site web sur le serveur, ...).

Comment
-------

On est obligé de récupérer le dossier `.git`, l'option `--depth=1` permet de ne récupérer qu'un seul rang d'historique. 
Ensuite le dossier `.git` est supprimé (`rm -rf !$/.git`).

Voici donc la commande pour récupérer tous les fichiers d'un git, sans en conserver l'historique :

    git clone --depth=1 --branch=master git://someserver/somerepo dirformynewrepo && rm -rf !$/.git
    
