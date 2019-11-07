# _**Introduction**_
Git a été créé en 2005 par Linus Torvald, qui a créé le système d'exploitation Linux.
[GitHub](https://github.com) est un service de mise en ligne de projets "versionnés" via Git, créé en 2008. Il a été racheté par Microsoft en 2018 pour la modique somme de 7,5 milliards de dollars.

En gros, voici ce que font Git et GitHub :
* Git est un logiciel de gestion de versions. C'est à dire, un logiciel permettant de photographier à l'instant T les fichiers d'un dossier.
*	GitHub est un service en ligne qui utilise Git, et qui permet entre autres de :  Mettre en ligne ses dossiers Git (dans ce qu'on appelle "un repository") et de collaborer à plusieurs sur un même dossier Git.

# _**Plan**_ 

Nous allons maintenant voir :
* Comment installer Git sur ton ordinateur.
* Comment créer un dossier Git.
* Comment revenir à des versions précédentes.
*	Comment mettre en ligne sur GitHub.

# _**Installation**_

Pour installer Git, il faut aller sur le site du même nom dans la rubrique téléchargement, il faut choisir son OS, puis télécharger et installer le logiciel. Enfin redémarrer le terminal.

Le terminal devrait te renvoyer quelque chose comme : git version X.XX.X. S'il te renvoie un truc du genre command not found: git, c'est que tu n'as pas installé Git ou relancé ton terminal !

Pour se servir de Git, c'est simple : il suffit de rentrer dans le terminal les commandes **$ git ...**  ou **git ...** pour lui faire exécuter truc ou machin. Voyons maintenant la commande permettant d'initialiser un dossier git.

Il faut tout d’aboed initialiser git avant de créer un dossier: 

**git Init**

Pour cela mets-toi dans un dossier de travail (avec la commande cd) et exécute la commande suivante **git status**.
Cette commande permet de te donner en un rien de temps l'état de ton projet git. Pour cela tape : 

**git status**

Le logiciel git te dit actuellement qu'il n'y a rien dans ton dossier, et donc rien à photographier ("nothing to commit"). Voyons maintenant comment ajouter un fichier.


 **Ajouter un fichier avec git add**

Pour savoir quels fichiers git va prendre en photo, il faut les ajouter avec la commande git add :

**git add**

Tu peux voir avec git status que ton fichier est bien ajouté. 

# _**Revenir en arrière**_

Git permet non seulement de faire des sauvegardes propres de ses projets, mais aussi de revenir en arrière facilement. Pour remonter le temps, ça se passe en deux étapes :

_**Déterminer la sauvegarde où je veux revenir.**_

* Déterminer la raison du retour arrière :
          - Est-ce à titre purement indicatif, juste pour regarder ce qui a été fait avant ?
          - S'agit-il d'un retour en arrière définitif ?

_**Regarder l'historique des versions**_

La commande git log permet de connaitre les commits faits sur le projet. 
Tu peux voir la liste des commits contenant les informations importantes :

* Qui a fait le commit.
* Quand le commit a été fait.
* Pourquoi ? (avec le message)
* Qu'est-ce qui a été commité ? (grâce au code bizarre)
* Le code 100d6f07dbf4cfb9103b3819e64432186750a1a2 est le SHA du commit. C'est son identifiant unique. C'est ce qui te servira pour le retour en arrière.

_**Revenir en arrière**_

Il y a deux façons de revenir en arrière :
* La première est à titre purement indicatif, et te servira seulement à observer un état précédent
*	La seconde est un retour définitif en mode "je veux revenir à tel endroit pour retravailler à partir de là"

_**Retour en arrière à titre purement indicatif**_

Imaginons que tu veux juste jeter un oeil sur un fichier à un instant T. Pour ceci, tu rentrerais la commande :

**$ git checkout SHA**

(en remplaçant "SHA" par le code que tu as eu lors du git log)

Tu peux ainsi naviguer dans l'ancienne version pour consulter les fichiers à cet instant T. Pas plus compliqué ! Pour revenir à la version actuelle, tu n'as qu'à faire :

**$ git checkout master**

_**Revenir en arrière définitivement_**

Tu peux revenir en arrière définitivement avec la commande git reset qui s'utilise comme ceci :

**$ git reset --hard SHA**

(en remplaçant "SHA" par le code reçu lors du git log)

# _**Mise en ligne**_ 

Maintenant que tu es un champion du commit, nous allons voir comment mettre son code en ligne pour en faire profiter la terre entière, et pouvoir collaborer à plusieurs sur un projet.
Grâce à git et GitHub, tu peux "push" ton code en ligne en quelques lignes de commandes à peine. Dans cette partie, nous verrons :

* Qu'est-ce que GitHub, et comment créer un repository.
*	La notion de remote pour Git : comment lier ton repository local à un repository en ligne.
*les deux commandes maitresses : git pull et git push.

La commande git push va envoyer ton code stocké en local vers un remote de ton choix. Elle s'utilise en faisant : $ git push nom_du_remote nom_de_la_branche. Si tu veux push ta branche "master" vers la remote "origin", tu feras donc :

**$ git push origin master**

La commande git pull est le contraire de git push : elle remplace le code en local avec celui de la remote de ton choix. Elle s'utilise de la manière suivante : $ git pull nom_remote nom_branche. Ainsi, si tu veux pull ta branche "master" depuis la remote "origin" tu feras :

**$ git pull origin master**

