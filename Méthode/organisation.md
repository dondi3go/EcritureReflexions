# Organisation

Cette partie traite de la partie formelle du projet.
L'arborescence sur le disque, les outils utilisés.


## Organisation des chapitres

Pour *La Revue*, le formalisme était "article009_blablabla.md"

Plusieurs problèmes :

* le préfixe "article", trop long
* le nombre de digits, trois c'est trop

Possibilité : "01_blablabla.md"


## Editeur de texte (VSCodium)

Continuer à utiliser *VSCodium*, mais avoir une meilleure coloration syntaxique.

Ce qui manque :

* Faire apparaitre les commentaires en vert foncé


## Gestion de version (Git)

Un peu d'ordre dans les messages de commit sinon tout sera confus.

Première question : en francais ou en anglais ?

Standardisation des messages de commit :
- "Add note on brainwashing" : ok
- "Update" : bof, "cleanup, rewording", plus de précision
- "First ok version"
- "Suite article XX"
- "Ajout article YY"
- Relecture de XX


## Compilateur (doc)

J'aimerais pouvoir faire les choses suivantes :
* Avoir une production en pdf directement.
* Directement convertir un .md en .pdf
* Distinguer deux types de commentaires : ceux destinés à être imprimés, les autres
* Avoir des statistiques


## Alias

Ajouter des alias pour se simplifier la vie.

###
Dans c:/users/<username>/.bashrc

alias cdiff='git diff HEAD@{1} --word-diff=color'
alias cgrep='grep --color -n'

* Commande *git*
* Commande *doc* + *typst*
* Commande *grep*, *fgrep*, etc