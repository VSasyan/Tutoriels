#Installer QT5

Ajouter au fichier `/etc/apt/sources.list` les lignes :

    deb http://mirrors.ircam.fr/pub/debian/ wheezy-backports main
    deb-src http://mirrors.ircam.fr/pub/debian/ wheezy-backports main

Puis executer :

    sudo apt-get update
    sudo apt-get install qtbase5-dev qtchooser qt5-default
    sudo apt-get install -t wheezy-backports qtcreator
    sudo apt-get autoremove
