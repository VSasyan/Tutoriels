Installation de ArgoUML sous Debian
===================================

Téléchargement
--------------

Dernière version (sous license Éclipse) sur [http://argouml-downloads.tigris.org/nonav/argouml-0.34/ArgoUML-0.34.tar.gz]
Le mettre dans un dossier local ou temporaire, par exemple ~/Téléchargements

Extraction
----------

    ~/Téléchargements $ tar -xf ArgoUML-0.34.tar.gz

Installation
------------

(source : README et commentaires)

Requérez les privilèges administrateur (ou du moins de staff). On va l'installer proprement dans /usr/local/lib/.

    /home/<>/Téléchargements/ # cp -r ArgoUML-0.34 /usr/local/lib/           # ou mv, hein !

On fait un lien pour que ce soit plus utilisable

    /home/<>/Téléchargements/ # ln -s /usr/local/lib/argouml-0.34/argouml.sh /usr/local/bin/argouml

Lancement
---------

    $ argouml <project-file>

KDE
---

Ouvrir le Lanceur, et clic droit sur l'onglet Applications, Modifier les applications.
Clic droit sur Développement, Nouvel élément.

Nom :	        ArgoUML
Icône :		/usr/local/lib/ArgoUML-0.34/icon/argouml2.svg
Description :
Commentaire :
Commande :	/usr/local/bin/argouml

Enregistrer