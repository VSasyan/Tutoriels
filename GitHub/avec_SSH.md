Utiliser GitHub en SSH
======================

Création de la clé
------------------

Le SSH permet de créer une clef pour certifier votre machine.
Plus besoin de rentrer le mdp à chaque fois quand vous commitez.

Créer la clef ssh pour la machine :
https://help.github.com/articles/generating-ssh-keys/


Utilisation de GitHub
---------------------

La suite est pareille, seule change la création du lien (on fait un lien en ssh pas https).

Créer un nouveau dossier et se mettre dedans avec un terminal :
mkdir Tutoriel

Initier Git :
git init

Ajouter un lien entre le git Local et GitHub :
git remote add origin [](git@github.com:VSasyan/Tutoriels.git)

Récupérer le contenu du GitHub :
git pull origin master

Ces trois lignes peuvent être remplacées par un clonage :
git clone [](git@github.com:VSasyan/Tutoriels.git)

Penser à ajouter vos nouveaux fichiers :
git add *
git commit -m "Message"

Envoyer le contenu sur GitHub :
git push -u origin master
Vous devez donner vos login GitHub.

C'est terminé !
