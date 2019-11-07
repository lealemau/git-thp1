# ****1. Introduction****

Accroche-toi à tes chaussettes, car nous allons maintenant découvrir les bases du terminal ! Il s'agit d'un outil très puissant permettant de "parler" à son ordinateur. Nous allons voir : comment interagir avec le terminal, comment jouer avec ses premiers fichiers, et bien d'autres choses utiles. C'est plutôt fun, tu vas voir !

# ****1.1. Ce que tu vas apprendre dans cette ressource****

Voici la liste des questions auxquelles tu vas pouvoir répondre avec cette ressource :

- Qu'est-ce que le terminal ?
- Que veulent dire GUI et CLI ?
- Comment lancer un terminal ?
- Comment exécuter ses premières fonctions avec un terminal ?
- Pourquoi la notion de géographie est très importante dans un terminal ?
- Qu'est-ce que VIM et comment s'en servir ?

# ****Historique****

Le terminal -- ce que l'on appelle plus communément un interpréteur de commande (ou command-line interpreter - CLI - en anglais) -- est un outil qui interprète les commandes tapées au clavier dans l'interface de ligne de commande.

À la base, les ordinateurs tournaient sans interface graphique. Les utilisateurs n'avaient donc pas d'autre choix que de passer par les CLI pour effectuer une action. L'arrivée des systèmes d'exploitation graphiques (Windows, Apple, Linux) n'a pourtant pas tué la popularité de la CLI car il permet de faire des tâches extrêmement précises.

En gros, c'est une version texte de l'explorateur de fichiers : on peut ouvrir des dossiers, créer des fichiers, les lancer, les renommer, installer des programmes, et bien d'autres choses. On dit que c'est une **CLI** (Command Line Interface), comparée à la GUI (Graphical User Interface) de l'explorateur normal. Tout est fait via le clavier, donc pas besoin de souris pour l'utiliser.

# ****Le terminal****

## ***Qu'est-ce que le terminal ?***

Le terminal est un outil intimidant aux premiers abords, mais pas si compliqué au final. J'ai réalisé une vidéo pour l'expliquer :
"https://www.youtube.com/embed/myz_6xrDwR4"

# ****3.2. Comment le lancer ?****

## ****3.2.1. Sur macOS****

CMD + SPACE, puis écrire Terminal (ou iTerm), Enter.

## ****3.2.2. Sur linux****

CTRL + ALT + T.

# ***🚀 ALERTE BONNE ASTUCE***
Si tu utilises Linux, passe ton terminal en anglais. Ça va vraiment t'aider lorsqu'il te renverra des erreurs. En effet, comme l'anglais est la langue d'internet, la majorité des gens ayant eu ton problème vont le poster en anglais. Tu auras ainsi 100 fois plus de résultats sur Google qu'avec une erreur postée en français.

## ***3.2.3. Sur Windows***

Sur Windows, le terminal sera géré de manière un chouilla différente. Pendant toute la formation, nous allons utiliser un terminal de type Shell Unix, car c'est le plus utilisé au monde et qu'il sera donc plus aisé pour toi de trouver des réponses en cas de problème. Le terminal Shell Unix est celui qui est installé de base pour Linux et macOS. Celui de Windows est l'invite de commandes, qui est de type DOS. Bon je sais, ça commence à faire beaucoup d'infos... Mais essaie au moins de retenir ces points :

- macOS et Linux utilisent le même "noyau" de système d'exploitation : Unix ; tandis que Windows utilise DOS.
- Le terminal de macOS et Linux est de type Shell Unix, tandis que celui de Windows est de type DOS. Ce qui fait que l'invite de commandes de Windows aura une utilisation différente de celui de type Unix Shell.
- Dans le milieu de la programmation, le terminal de type Shell Unix est universellement utilisé.
- Si tu es utilisateur de Windows, nous te demanderons de trouver une alternative à l'invite de commandes.

Pas de panique, nous avons pensé à toi si tu es sur Windows ! Voici quelques alternatives qui feront le travail :

- La solution de facilité pour les grands débutants du terminal est Cygwin. Pour t'aider, j'ai même réalisé une vidéo tutorielle pour son installation.
- C'est en constatant le rejet universel de Windows chez les développeurs qu'un certain Satya Nadella a travaillé dur pour proposer une alternative décente. Ainsi, ***si tu es sur Windows 10***, il existe un terminal Shell Unix qui s'appelle Windows Subsystem for Linux et qui installe une version de Linux sur Windows dont tu peux te servir

# ***3.3. Premières fonctions ?***

Pour faire marcher le terminal, rien de plus simple : il suffit de rentrer le texte correspondant à une fonction pour que celle-ci s'exécute. Par exemple, si dans l'explorateur en GUI il suffit de double cliquer sur mon_fichier.txt pour l'ouvrir, il faudra taper open mon_fichier.txt (sur macOS) ou xdg-open mon_fichier.txt (sur Linux) dans le terminal pour faire de même. On va tester ça avec notre première fonction :

$ echo "Hello world !"

(je commence toutes les commandes de terminal avec un $. C'est une convention qui aide à reconnaître les commandes de CLI, mais qui ne fait pas partie de la commande. Enlève donc bien le $ au moment de tester !)

Si tu exécutes cette commande, le terminal devrait te renvoyer Hello world ! (cette phrase est un grand classique de la programmation). Et là, BOUM ! Tu viens d'exécuter ta première commande de terminal 🎉.

Maintenant nous allons voir quelques commandes basiques.

## ***3.3.1. PWD***

pwd est l'acronyme de Print Working Directory, une commande affichant le dossier dans lequel tu es actuellement.

$ pwd

Pour moi, pwd me renvoie :

/Users/felix

C'est comme dans l'explorateur en GUI, quand tu double-cliques sur felix, il te déplace dans le dossier felix qui est dans le dossier Users.

# ***🚀 ALERTE BONNE ASTUCE***
pwd est généralement la première commande que l'on tape quand on arrive dans le terminal de quelqu'un car c'est idéal pour s'y retrouver ✌️

## ***3.3.2. LS***

ls est le diminutif de list. Cette fonction affiche les fichiers et dossiers situés dans mon dossier actuel.

$ ls

Pour moi, ls me renvoie :

Applications/   Dropbox/     Music/       Desktop/
Pictures/     Documents/    Library/     Public/
Downloads/    Movies/

Dans le terminal, nous pouvons ajouter des options à la plupart des fonctions en utilisant la syntaxe $ fonction -option. Par exemple, je peux faire ls -a (a pour "all"), ce qui a pour effet d'afficher aussi les fichiers commençant par un . (fichiers de devs en général). Je peux faire ls -l pour afficher la liste au format long. Et je peux même combiner les deux en faisant ls -al.
