# Connexion SSH via clé

### Générer une clef

    ssh-keygen
    
### Copier la clef publique sur les machines

    cat ~/.ssh/id_rsa.pub | ssh pi@piensg006 "cat >> ~/.ssh/authorized_keys"

### Ajouter l'option dans `~/.ssh/config`

    Host piensg003
        HostName     piensg003
        User         pi
        IdentityFile ~/.ssh/id_rsa IdentityFile ~/.ssh/id_rsa

## Pour MPI :

### Forcer OpenMPI à n'utiliser que eth0

Créer le fichier `~/.openmpi/mca_parameters.conf` et écrire `btl_tcp_if_include=eth0` :

    mkdir ~/.openmpi
    echo "btl_tcp_if_include=eth0" >> ~/.openmpi/mca_parameters.conf

### Lister les machines

Créer un fichier `hosts_names` :

    piensg003 slots=4 max-slots=4
    piensg004 slots=4 max-slots=4
    piensg005 slots=4 max-slots=4
    piensg006 slots=4 max-slots=4
    piensg007 slots=4 max-slots=4
    #piensg011 slots=4 max-slots=4

### Variable d'environnement (optionnel)

Définir `export MPI_HOSTS=/home/pi/vsasyan/hosts_name` :

### Copier l'exécutable

Il faut copier l'exécutable par exemple en ssh :

    ssh pi@piensg011 'mkdir -p /home/pi/vsasyan' && scp /home/pi/vsasyan/multi_mandel pi@piensg011:/home/pi/vsasyan/
