1- Téléchargez la librairie depuis le site: libqglviewer.com (système d'exploitation linux) et décompréssez le.
2- Ouvrez le avec Qt creator et compiler juste le projet QGLViewer
3- Dans le répertoire où se trouve votre projet, vous allez trouver un dossier intitulé "build-libQGLViewer-2.6.3-Desktop-Debug"
	* Mettez-vous dans ce répertoire
	* cd QGLViewer/
	* sudo make install
	* cd /etc/ld.so.conf.d/
	* sudo touch QGLViewer.conf
	* sudo vi QGLViewer.conf
	* Ecrivez dedans: "/etc/local/lib/"
4- Exécuter la commande: sudo ldconfig
