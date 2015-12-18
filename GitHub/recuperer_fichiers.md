Récuperer les fichier d'un git
==============================


Pour récuperer automatiquement les fichiers d'un git, sans en récupérer l'historique :

    git clone --depth=1 --branch=master git://someserver/somerepo dirformynewrepo && rm -rf !$/.git

On est obligé de récupérer le dossier `.git`, l'option `--depth=1` permet de ne récupérer qu'un seul rang d'historique. 
Ensuite le dossier `.git` est supprimé (`rm -rf !$/.git`).
