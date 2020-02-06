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
