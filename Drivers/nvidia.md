# Installer les drivers NVidia propriétaires

## Source

https://wiki.debian.org/fr/NvidiaGraphicsDrivers#Debian_7_.22Wheezy.22

## Ce qui revient à faire

Descendre à Version 304.125 :

    sudo gedit /etc/apt/sources.list

Ajouter : Debian 7 "Wheezy"

    deb http://http.debian.net/debian/ wheezy main contrib non-free

Puis :

    sudo aptitude update
    sudo aptitude -r install linux-headers-$(uname -r|sed 's,[^-]*-[^-]*-,,') nvidia-kernel-dkms


Il faut ensuite faire : https://wiki.debian.org/fr/NvidiaGraphicsDrivers#configure

Soit :

    sudo mkdir /etc/X11/xorg.conf.d
    sudo gedit /etc/X11/xorg.conf.d/20-nvidia.conf

Et copier-coller :

    Section "Device"
            Identifier "My GPU"
            Driver "nvidia"
    EndSection
