# Installation de QGLViewer

Téléchargez la librairie depuis le site : libqglviewer.com (système d'exploitation linux) et décompréssez le.  
Ouvrez le avec Qt creator et compilez juste le projet "QGLViewer".  
Dans le répertoire où se trouve votre projet, vous allez trouver un dossier intitulé "build-libQGLViewer-2.6.3-Desktop-Debug", mettez-vous dans ce répertoire et exécutez :

    cd QGLViewer/
    udo make install
    cd /etc/ld.so.conf.d/
    sudo touch QGLViewer.conf
    sudo echo /etc/local/lib/ > QGLViewer.conf
	
Exécutez la commande : `sudo ldconfig`
