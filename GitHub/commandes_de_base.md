Message GitHub de base
======================

A la création d'un projet vide, GitHub rapelle les commandes des bases, les voici :

HTTPS
-----

    HTTPS : https://github.com/VSasyan/test.git

…or create a new repository on the command line

    echo "# test" >> README.md
    git init
    git add README.md
    git commit -m "first commit"
    git remote add origin https://github.com/VSasyan/test.git
    git push -u origin master

…or push an existing repository from the command line

    git remote add origin https://github.com/VSasyan/test.git
    git push -u origin master


SSH
---

    SSH : git@github.com:VSasyan/test.git

…or create a new repository on the command line

    echo "# test" >> README.md
    git init
    git add README.md
    git commit -m "first commit"
    git remote add origin git@github.com:VSasyan/test.git
    git push -u origin master

…or push an existing repository from the command line

    git remote add origin git@github.com:VSasyan/test.git
    git push -u origin master
