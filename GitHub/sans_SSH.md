Utiliser GitHub en SSH
======================

Compte GitHub
-------------

Il faut un compte GitHub pour commiter sur les projets ou accéder aux projets privés (si autorisé par le propriétaire).
Vous pouver récupérer les projets sans compte (git clone, git pull).

Utilisation de GitHub
---------------------

Modifier le proxy pour le terminal :
export http_proxy='http://10.0.4.2:3128'
export https_proxy='https://10.0.4.2:3128'

Créer un nouveau dossier et se mettre dedans avec un terminal :
mkdir Tutoriel

Initier Git :
git init

Ajouter un lien entre le git Local et GitHub :
git remote add origin https://github.com/VSasyan/Tutoriels.git

Récupérer le contenu du GitHub :
git pull origin master

Ces trois lignes peuvent être remplacées par un clonage :
git clone https://github.com/VSasyan/Tutoriels.git

Penser à ajouter vos nouveaux fichiers :
git add *
git commit -m "Message"

Envoyer le contenu sur GitHub :
git push -u origin master
Vous devez donner vos login GitHub.

C'est terminé !
