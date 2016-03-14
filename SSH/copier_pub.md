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

Créer le ficheir `~/.openmpi/mca_paramters.conf` et écrire `btl_tcp_if_include=eth0`.

### Lister la machine

Créer un fichier `hosts_names` :

    172.31.57.62
    172.31.57.63
    172.31.57.64
    172.31.57.65
    172.31.57.66
    172.31.57.70
