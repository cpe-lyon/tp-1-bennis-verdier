# TP1 par Kamil BENNIS et Fabien VERDIER

## Exercice 1. Installation du serveur 

## Exercice 2. Prise en main de l'interpréteur de commandes

### Manuel

#### 1. Comment obtenir le manuel de la commande which et à quoi sert-elle ?

`$ man which`

which retourne le chemin des fichiers qui seraient exécutés dans l'environnement courant si ses arguments avaient été donnés comme commandes dans un interpréteur de commandes strictement conforme à POSIX. Pour ce faire, which cherche dans la variable PATH les fichiers exécutables correspondants aux noms des arguments.

#### 2. Comment rechercher un terme dans le manuel ?

`/option` à l'intérieur du manuel nous permet de surligner toutes les occurences de "option" dans le manuel.

#### 3. Comment quitte-t-on le manuel ?

Il suffit d'appuyer sur q pour quitter `q`.

#### 4. Un manuel peut a avoir plusieurs sections. Mais comment accéder à une section en particulier ?

Pour accéder à une section précise du manuel de **intro** par exemple, au moins 2 commandes sont possibles :
* `$ man intro.6`
* `$ man 6 intro`

### Navigation dans l’arborescence des fichiers

Pour se déplacer dans les répertoires, on utilise la commande **cd**. Pour aller dans `/var/log`, on tape la commande :  
`$ cd /var/log`.
Lorsque l'on se trouve dans un répertoire, pour remonter au répertoire parent en utilisant un chemin relatif, on utilise la commande `$ cd ..`. Dans ce cas, cette commande nous place dans le répertoire `/var`.  
Pour retourner au dossier personnel, on utilise la commande `$ cd`.  
  
Pour executer une commande en tant qu'administrateur, on fait préceder la commande du mot-clef `sudo` qui veut dire super-utilisateur do.
Cependant, `sudo` permet de lancer des programmes, et on ne peut pas le mettre devant des commandes intégrées. Par exemple, cette écriture donne une erreur : ~~`$ sudo cd /root`~~.  

On peut créer une arborescence de répertoire et fichier en ligne de commande. Pour créer un répertoire, la commande est `$ mkdir NomDeDossier`. Pour créer un fichier, on utilise `$ touch NomDeFichier`. On combinant ces commandes et les variantes de `cd`, on peut donc créer une arborescence.

Si l'on veut supprimer un fichier, on utilise la commande `$ rm NomDuFichier`. Pour supprimer un dossier **vide**, on peut utiliser `$ rmdir NomDuDossier` ou `$ rm -d NomDuDossier`. Pour supprimer un répertoire contenant d'autres répertoires et des fichiers, il faut utiliser la commande `$ rm -r NomDuDossier` qui va supprimer récursivement tous les éléments.

### Commandes importantes

Pour afficher la date et l'heure, la commande est `$ date`, à ne pas confondre avec la commande `$ time` qui permet de déterminer le temps que met un processus à s'executer.  
La commande `$ ls` permet d'afficher la liste de tous les répertoires et fichiers qui se trouvent dans le répertoire courant. Pour afficher les répertoires cachés (qui commencent par un **.**), il faut utiliser la commande `$ la` (la est l'alias de ls -A).

L'executable de la commande **ls** se trouve dans le répertoire /bin, comme d'autres commandes comme **kill**, **mkdir**, et toutes les commandes natives.  

:sparkles: Astuce : pour afficher les répertoires situés dans le répertoire parent au répertoire actuel, nous pouvons utiliser la commande `$ ls ..`.  

Nous pouvons utiliser des alias pour définir une commande avec une option par exemple. Pour lister les alias, il suffit de faire la commande `$ alias`. Nous avons dans notre système un alias ll='ls -alF'.

#### Commande sur les fichiers :
Nous pouvons écrire dans un fichier la sortie d'une commande avec > et >>. En utilisant >, on écrit dans le fichier et on l'écrase s'il existe déjà. Avec >>, on ajoute la sortie de la commande à la fin du fichier s'il existe déjà. Par exemple, si on effectue la commande suivante :  
`$ echo 'yo' > plop`  
On place la sortie de la commande `echo 'yo'` dans le fichier plop (qui est créé s'il n'existe pas et qui est écrasé sinon). La sortie de `echo 'yo'` étant `yo`, on a simplement écrit `yo` dans le fichier **plop**.
Le comportement est quasiment le même avec la commande suivante :  
`$ echo 'yo' >> plop `  
On écrit `yo` à la fin du fichier **plop** et on ne l'écrase pas, ainsi si on tape deux fois cette commande, on écrit deux fois `yo` contrairement à la commande précédente qui aurait écrasé le fichier à chaque appel.

:sparkles: Astuce : pour déterminer le type d'un fichier, on peut utiliser la commmande `$ file NomDuFichier`.  

Lorsqu'on modifie le contenu d'un fichier toto qu'on a lié à un fichier titi grace à la commande `ln toto titi`,  on s'apercoit que cela modifie les deux fichiers mais la supression de toto n'influe pas sur l'existence de titi.
Mais dans le cas où un autre fichier tutu est liée symboliquement avec titi `ln -s titi tutu`, une modification de titi influe sur tutu et inversement et la supression de titi provoque la supression de tutu aussi.

Les raccourcis claviers `CTRL S` et `CTRL Q` permettent respectivement d'interrompre et de reprendre le défilement à l'écran.
A noté que la touche `Arrêtdef` presentes dans la plupart des claviers permet aussi d'avoir le même résultat.

Pour afficher les 5 permieres lignes d'un fichers(syslog) il faut taper la commande : `$ head -n 5 syslog`.
Pour afficher les 15 dernieres lignes d'un fichers il faut taper la commande : `$ tail -n 15 syslog`.
Pour afficher les lignes 10 à 20 d'un fichers il faut taper la commande : `$ sed -n '10 20p'syslog`.

La commande `dmesg | less` permet d'afficher la mémoire tampon du noyau `dmesg` page par page `less`.

Le fichier `/etc/passwd` permet d'afficher la liste de tous les utilisateurs du système, pour afficher sa page de manuel il suffit de taper `$ man passwd`.

Pour afficher seulement la première colonne triées par ordre alphabétique inverse il peut utiliser la commande : `$ cut -d ':' -f1 passwd | sort -r ` le caractère entre guillements permet de délimiter les colonnes, `-f1` correspond à la première colonnes et `sort -r ` sert à trier par ordre alphabétique inverse.

 Le nombre d’utilisateurs ayant un compte sur cette machine est défini par la commande `wc -l`.
 
 Pour chercher le nombre de pages de manuel comportant le mot-clé conversion dans leur description il faut écrire `$ man -k conversion | wc -l`.

A l’aide de la commande find on peut aussi recherchez tous les fichiers se nommant passwd présents sur la machine :`$ find / -name 'passwd' |  less`, pour enregistrer cette liste dans un nouveau fichier list_passwd_files, il faudrait rajouter `> list_passwd-files.txt` en sortie de la commande file et pour redigerer ses erreurs vers le fichier spécial dev/null on peut utiliser : ` `.

Dans un dossier personnel, pour chercher où est défini un alias on peut taper la commande `$ grep -rl -null`.
¨Par contre pour trouver un fichier, il vaudrait mieux taper la commande `locate`.
Mais dans le cas où un fichier vient d'être créer, il faudrait mettre à jour le locate (avec anacron).

## Exercice 3 Découverte de l’éditeur de texte nano

Pour ouvrir un fichier avec l'éditeur de texte nano, il faut se placer dans le dossier du fichier en question et taper : `nano log.txt`.
Pour mofifier un mot en un autre il suffit de taper `ALT R` et se laisser guider par nano. Pour manipuler le fichier les raccourcis `CTRL K ` pour couper et `CTRL U` pour coller sont indispensables. Pour annuler la dernière action il faut taper `ALT U`.

## Exercice 4 Personnalisation du shell

Décommenter la ligne `force_color_prompt=yes` et recharger le fichier .bashrc avec la commande ` source .bashrc` permet de faire passer l'invite de commande en couleurs. On obtient user@host en vert et chemin_courant en bleu.

La séquence \[\e[01;35m\]\A permet d'afficher l'heure (\A) en violet, dont le code couleur est 35.  
Les séquences \[\e[00m\] - , \[\e[00m\]: et \[\e[00m\]\$ permettent d'afficher respectivement le tiret, les deux points et le $ en blanc, dont le code couleur est 0.  
La séquence \[\e[01;32m]\u@\h permet d'afficher les noms de l'utilisateur et de la machine en vert, dont le code couleur est 32.  
La séquence \[\e[01;36m\]\w permet d'afficher le chemin courant en cyan, dont le code couleur est 36.

