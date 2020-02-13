# TP1: Admin Système

## Exo 2:

1. Manuel

    1.1 man which --> Afficher le manuel intégré -> fourni une aide sur une commande.
         Which --> permet de donner le chemin d'une commande.
    
    1.2 /option permet de trouver tous les mots "option" dans le man.

    1.3 Pour quitter le man, on doit appuer sur "q" et "entrer".

    1.4 man 6 intro --> section 6 --> donne des info sur les jeux et programmes sympas sur le système
    
2. Navigation

    2.1 cd /var/log --> permet d'aller dans le dossier /var/log
    
    2.2 cd .. --> permet de retourner dans le /var
    
    2.3 cd ~ --> permet de retourner dans le dossier personnel ou cd /home/linux --> propre à mon dossier personnel.
    
    2.4 cd - --> retourne dans le chemin précédent.
    
    2.5 cd /root --> Nous n'avons pas les droits, l'accès est donc rejeté.
    
    2.6 sudo cd /root --> On a accès car on passe par sudo qui correspond au droit "super utilisateur" (root).
    
    2.7 mkdir -p Dossier1/fichier1 Dossier2/Dossier2.1 Dossier2/Dossier2.2
        touch Dossier1/fichier1
        touch Dossier2/Dossier2.2/fichier2 
        touch Dossier2/Dossier2.2/fichier3
    
    2.8 rm Dossier1/fichier1 --> fonctionne car fichier
         rm Dossier1 --> non car c'est un dossier.
         
    2.9 rmdir ou rm -d permet de supprimer un dossier vide.
    
    2.10 Sur Dossier2, ne fonctionne pas car non vide.
    
    2.11 rm -r Dossier2 --> Supprime de manière récursive.
    
3. Commandes importantes

    3.1 date --> affiche la date et l'heure. 
        Time +cmd --> permet d'afficher l'usage de ressource et temps nécéssaire à           l'éxécution d'une commande.
    
    3.2 ls --> affiche les dossiers et fichiers visibles.
         la --> affiche les dossiers et fichiers cachés.
         
    3.3 which ls --> chemin accès /usr/bin/ls
    
    3.4 ll --> équivalent de ls -alF. Permet d'afficher les droits sur les fichiers et dossiers cachés ou non.
         Alias ll --> ls -alF.
    
    3.5 ls /bin permet d'afficher le contenu de /bin.
    
    3.6 ls --> permet de lister l'ensemble des fichiers et dossiers.
    
    3.7 pwd --> donne le chemin absolu du dossier courant.
    
    3.8 echo 'yo' > plop --> va écrire yo dans un fichier en remplacant son sontenu. 
    
    3.9 echo 'yo' >> plop --> Va ajouter à la suite le contenu du echo dans le fichier plop sans en supprimer le contenu.
    
    3.10 file permet de déterminer le type d'un fichier.

    3.11 echo 'Hello toto !' > toto
          ln toto titi --> créer un lien titi vers toto
          echo 'Modif' > toto
          cat titi --> on remarque que le changement a été effectué.
          rm toto --> titi affiche toujours le contenu de toto car titi copie le dernier contenu de toto
    
    3.12 ln -s titi tutu --> lien symbolique de titi vers tutu
          Si on modifie tutu, titi est aussi modifié car titi pointe sur tutu.
          Si on supprime tutu, titi existe mais ne peut être lu donc n'affiche plus rien car le lien est cassé.
    
    3.13 more /var/log/syslog. Avec la touche "Entré", on fait défilé ou non le contenu. "Espace" --> par page.
    
    3.14 head -5 /var/log/syslog --> affiche les 5 premières lignes.
        tail -15 /var/log/syslog --> affiche les 15 dernières lignes.
        head -20 | tail -10 /var/log/syslog --> Les lignes entre 10 et 20 .
        
    3.15 dmesg | less
        dmesg --> affiche contenu du buffer du kernel
        less permet un affichage page par page.
    
    3.16 more /etc/passwd --> contient l'ensemble des comptes. Le groupe d'appartenance sont présent ainsi que le numéro associé.


    3.17 sort -d -r --> permet de trier par ordre alphabétique inverse. de Z & A

    3.18 wc /etc/passwd --> affiche le nombre d'utilisateur.

    3.19 man -k conversion | wc -l -> affiche le nombre de page contenant "conversion".


    3.20 sudo find / -name "passwd" | wc --> on cherche combien de fichier s'appelle passwd.
    
    3.21 find / -name passwd >liste_users 2>/dev/null.
         On va donc séparer les résultats et les erreurs.
         dans liste_user --> les users et dans /dev/null --> les erreurs
    
    3.22 Dans votre dossier personnel, utilisez la commande grep pour chercher où est défini 
    l’alias ll vu précédemment.

    ->  cat .bashrc | grep ll                                                                                     
   
    3.23 Utilisez la commande locate pour trouver le fichier history.log.

    -> locate -A history.log                                                                                       
   
    3.24 Si l'on créer un fichier et que l'on utilise locate:

    -> touch testDeFichier

    -> locate -a testDeFichier (aucun résultats) 
    Locate utilise une **base de donnée** pour rechercher des fichiers... Il faut mettre à jours cette base de données
    manuellmenent pour que *locate* puisse trouver notre fichier. Il faut faire : **updatedb**.
    
## Exo 3:

4. 

    4.1 more /var/log/syslog > log.txt --> Cela permet de copier le contenu de syslog dans log.txt
    
    4.2 _Sous VIM - :%s/kernel/noyau --> permet de remplacer le mot kernel par le mot noyau dans l'ensemble du fichier en une fois.
    
    4.3 _Sous VIM - 10dd --> coupe 10 lignes suivant le placement du curseur - p --> Colle le presse papier APRES le curseur (P pour coller avant le curseur).
    
    4.4 u ou CRTL+R --> permet d'annuler la dernière commande.
    
    4.4 ZZ ou :qw --> permet d'enregistrer le fichier avant de quitter.
 

## Exo 4:
    
