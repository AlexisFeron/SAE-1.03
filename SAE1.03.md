# Dossier d'étude et de choix des solutions / Notice d'utilisation


## Dossier d'étude et de choix des solutions :

Les logiciels sont triés par ordre de préférences.

| Besoins                                                               | Nombre d'outils différents demandés | Logiciels proposés                                            |
| --------------------------------------------------------------------- | ----------------------------------- | ------------------------------------------------------------- |
| Avoir des Gestionnaires de bureau/fenêtre (dont un qui vous plaise)   | 4                                   | 1) Gnome <br/> 2) Xfce <br/> 3) Unity <br/> 4) Plasma         |
| Avoir deux utilisateurs: vous et "stagiaire"                          |                                     | ✓                                                             |
| Compiler un programme C                                               | 2                                   | 1) GCC <br/> 2) Visual C++                                    |
| Regarder les pages de man de la libC                                  |                                     | ✓                                                             |
| Lancer un `make`                                                      |                                     | ✓                                                             |
| Éditer du code source                                                 | 4                                   | 1) VSCode <br/> 2) Sublime Text <br/> 3) Emacs <br/> 4) Vim   |
| Déboguer du code                                                      | 2                                   | 1) VSCode <br/> 2) GDB                                        |
| Naviguer sur le Web                                                   | 2                                   | 1) Chrome <br/> 2) Firefox                                    |
| Naviguer sur le Web avec la version de firefox dans backports         |                                     |                                                               |
| Éditer une image matricielle (png...)                                 | 2                                   | 1) Photopea <br/> 2) Gimp                                     |
| Éditer une image vectorielle (svg)                                    | 1                                   | 1) Inkscape                                                   |
| (Dé)Compresser les formats `targz`, `7z` et `rar`                     | 1                                   | 1) WinRAR                                                     |

### Pourquoi ces outils :

##### Gestionnaires de bureau :
Gnome : Gestionnaire de bureau déjà présent à l'IUT, simple graphiquement, simple d'utilisation et fluide. La personnalisation est plus compliquée. <br/> 
Xfce : Gestionnaire de bureau déjà présent à l'IUT, je le trouve plus compliqué d'utilisation que Gnome. Mais il est très économe en ressources. <br/>
Unity : Gestionnaire de bureau utilisé par défaut sur Ubuntu, simple d'utilisation, assez personnalisable. <br/>
Plasma : Gestionnaire de bureau que j'ai du installer par moi même, il a une interface agréable (ressemblante à Windows) et personnalisable, mais j'ai trouvé qu'il était pas assez fluide.

##### Compiler :
GCC : Compilateur que nous utilisons en algoritmique et structure de données. <br/>
Visual C++ : Environnement de développement intégré sur Windows qui permet la compilation.

##### Éditer du code :
VSCode : Editeur de code sympa visuellement et très pratique s'il on l'utilise avec de bonnes extensions. <br/>
Sublime text : Editeur de code sympa visuellement et pratique. <br/>
Emacs : Editeur de code que je trouve moins pratique. c'est celui que l'on utilise. <br/>
Vim : Editeur de code que je trouve peu pratique et pas simple d'utilisation. 

##### Déboguer :
VSCode : Editeur de code qui permet de déboguer du code soit nativement pour le java soit avec des extensions pour les autres langages. <br/>
GDB : Portable et fonctionne avec plusieurs langages. Fonctionne avec GCC.

##### Naviguer :
Chrome : Navigateur pratique que j'ai l'habitude d'utiliser chez moi, même s'il s'occupe peu de la vie privée. <br/>
Firefox : Navigateur pratique que j'ai l'habitude d'utiliser à l'IUT.

##### Éditer une image matricielle :
Photopea : Site internet ayant la plupart des fonctionnalités de Photoshop (donc très complet) gratuitement. <br/>
Gimp : Application plutôt simple d'utilisation et permet de faire la majorité de ce que l'on souhaite.

##### Éditer une image vectorielle :
Inkscape : Logiciel assez basique de dessin et édition d'image vectoriel libre. 

##### (Dé)Compresser :
WinRAR : Logiciel complet au niveau des formats supportés, et permet de faire ce que l'on demande.


## Notice d'utilisation :

### Tout d'abord, on doit configurer une machine virtuelle avec Debian :
On se rend sur le site de Debian afin de télécharger une image disque : https://www.debian.org/distrib/netinst.fr.html <br/>

On télécharge ensuite VirtualBox : https://www.virtualbox.org/wiki/Linux_Downloads

On va d'abord créer un machine virtuelle :
- On lance VirtualBox et on clique sur nouvelle.
- On donne un nom à notre machine virtuelle puis on choisit un dossier ou l'on dispose d'assez d'espace, on choisit ici le type Linux et on sélectionne une version de Debian. 
- On donne en suite, la taille de la mémoire que l'on souhaite attribuer à la machine virtuelle.
- On sélectionne Créer un disque dur virtuel maintenant.
- On sélectionne VDI.
- On sélectionne Dynamiquement alloué.
- On donne ici la taille du disque de la machine virtuelle. 

On vient de créer une machine virtuelle, on doit la lancer :
- On doit sélectionner l'image que l'on a télécharger puis procéder à un installation classique.
- Il faut juste dans notre cas, penser à configurer le proxy.
- Il faut sélectionner les gestionnaires de bureaux que l'on désire pour qu'ils soit installés.

### On doit pouvoir répondre à certains besoins et on va donc télécharger un outil pour chaques besoins que l'on retrouve dans le tableau ci dessus :

Pour l'installation d'un gestionnaire de bureau, en configurant la machine virtuelle vous aurez choisit l'un des gestionnaires de bureau. Il n'y as donc rien a changer. <br/>

Pour créer un deuxième utilisateur, il faut se rendre dans la partie utilisateur des paramètres, déverrouiller et ajouter un nouvel utilisateur. <br/>

Pour réaliser une compilation, vous pouvez utiliser la commande ci dessous dans un terminal en remplaçant par le nom des fichiers : `gcc -Wall -o nom_du_fichier_objet -c nom_du_fichier_source_C` <br/>

Pour regarder les pages man de la libC, il suffira de taper `man libc` dans un terminal. <br/>

Pour lancer un `make`, nous avons besoin de créer un fichier nommé Makefile qui contient plusieurs ligne de code, voici en un : https://github.com/AlexisFeron/Makefile/blob/main/Makefile, il faudra remplacer par le noms des fichiers, on pourra ensuite lancer un `make` et ensuite exécuter avec `./exe`.<br/>

Pour éditer du code, il suffit d'aller sur https://code.visualstudio.com/download et de télécharger la bonne version une fois installer, il est prêt à l'emploi, vous pourrez ensuite si vous le désirer trouver des extensions qui vous plaisent pour vous faciliter votre code. <br/>

Pour déboguer du code, vu que nous avons installé VSCode, nous pouvons l'utiliser pour faire du débogage, pour mieux comprendre comment cela fonctionne je vous conseille cette vidéo qui explique comment le faire : https://www.youtube.com/watch?v=7qZBwhSlfOo&ab <br/>

Je part du principe que vous savez naviguer sur internet si vous vous retrouver ici, donc je vous laisse simplement un lien pour installer google chrome : https://www.google.com/intl/fr_fr/chrome/ <br/>

Pour éditer une image matricielle, il vous suffit de vous rendre sur : https://www.photopea.com <br/>

Pour éditer une image vectorielle, l'outil que je vous recommande est Inkscape, pour l'installer il suffit de télécharger : https://inkscape.org/release/inkscape-1.1.1 <br/>

Pour compresser et décompresser les suivants formats `targz`, `7z` et `rar`, on va installer WinRAR, il suffit de le télécharger à l'adresse suivante : https://www.win-rar.com/download.html?&L=10 