# Le terminal

## Définition

Un terminal, plus communément appelé _interpréteur de commande_ (ou _command-line interpreter_ - CLI - en anglais) est un **outil qui interprète les commandes tapées au clavier dans l'interface de ligne de commande**.
Il permet d'ouvrir des dossiers, créer des fichiers, les lancer, les renommer, installer des programmes et plus encore. Il correspond à la version texte de l'explorateur de fichier.

### - Comment le lancer ?

Le terminal n'est pas le même selon les différents systèmes d'exploitation graphiques :
* Sur macOS : CMD + SPACE, puis écrire Terminal (ou iTerm), Enter.
* Sur Linux : CTRL + ALT + T 
 * astuce : sur Linux, il est préférable de passer le terminal en anglais, ce qui va vraiment aider lorsque le terminal renverra des erreurs. Cette dernière étant la langue d'internet, la majorité des (apprentis) _developers_ posteront leur problème en anglais.
* Sur Windows : invite de commande type DOS
 * alors que macOS et Linux utilisent un terminal de type Shell Unix, universellement reconnu, Windows dispose d'un autre terminal appelé DOS.
 * Pour les débutants, il sera préférable d'utiliser _Cygwin_ ou encore _Windows subsystem for Linux_.
 
#### Différences entre GUI et CLI

_L'interface utilisateur graphique_ (GUI) permet à l'utilisateur d'intéragir avec le système à l'aide d'éléments graphiques tels que des fenêtres, des icônes, des menus, tandis que _l'interface de ligne de commande_ (CLI) permet à l'utilisateur d'interagir avec le système à l'aide de commandes, donc via le terminal.
 
### Premières fonctions

Pour faire marcher le terminal, rien de plus simple : il suffit de rentrer le texte correspondant à une fonction pour que celle-ci s'exécute.

* Pour ouvrir un fichier, il faut taper **open mon_fichier.txt** (sur macOS) ou **xdg-open mon_fichier.txt** (sur Linux)
* Pour afficher le dossier dans lequel on se trouve actuellement, on tape **pwd**.
* **ls**, qui est le diminutif de _list_, affiche les fichiers et dossiers situés dans le dossier actuel. Il est possible d'ajouter des options à la plupart des fonctions : pour celle-ci, **ls -a** (a pour "all") affiche tous les dossiers, même ceux commençant par **.**.
* On peux lancer un programme permettant de lire le manuel d'une fonction précise avec la fonction **man fonction**.
* **cd** est l'acronyme de _change directory_ et permet de naviguer entre dossiers.

### Fonctions importantes à retenir

* **touch** : créer un fichier
* **cp** : copier un fichier
* **mv** : déplacer un fichier ou un dossier
* **rm** : supprimer un fichier 
* **rm-r** : supprimer un dossier et son contenu

### Aller plus loin

Voici un excellent [cours express](https://www.vikingcodeschool.com/web-development-basics/a-command-line-crash-course) pour avoir quelques bases concernant l'utilisation du terminal, qui aborde d'autres sujets intéressants tels que le [PATH]().
[Learn Enough Command Line To Be Dangerous](https://www.learnenough.com/command-line-tutorial/basics) est un cours d'introduction au terminal de Michael Hartl permettant d'aller assez loin dans son utilisation.
[Ici](https://medium.com/actualize-network/how-to-learn-vim-a-four-week-plan-cd8b376a9b85), une marche à suivre pour découvrir Vim.