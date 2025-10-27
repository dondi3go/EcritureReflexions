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

{
    "editor.renderWhitespace": "none",
    "editor.wordWrap": "on",
    "editor.rulers": [80,120],
    "workbench.editor.enablePreview": false,
    "python.linting.enabled": true,
    "python.linting.flake8Enabled": false,
    "python.linting.pylintEnabled": true,
    "editor.unicodeHighlight.nonBasicASCII": false,
    "todohighlight.include": [
        "**/*.md"
    ],
    "todohighlight.keywords": [
        {
            "text": "DOUBLE_SPACE: OK",
            "regex": {
                "pattern": "[ ]{2,}"
            },
            "backgroundColor": "red",
            "overviewRulerColor": "none"
        },
        {
            "text": "DOUBLE_STAR_STRONG: OK",
            "regex": {
                "pattern": "(\\*\\*)(.*?)(\\*\\*)"
            },
            "color": "black",
            "backgroundColor": "khaki",
            "overviewRulerLane": 1,
            "overviewRulerColor": "orange",
            "outlineColor": "red",
            "fontStyle": "normal"
        },
        {
            "text": "SINGLE_STAR_ITALIC: OK",
            "regex": {
                "pattern": "[*](.*?)[*]"
            },
            "color": "lightcoral",
            "backgroundColor": "none",
            "overviewRulerColor": "none",
            "fontStyle": "normal"
        },
        {
            "text": "DOUBLE_QUOTES: OK",
            "regex": {
                "pattern": "[\"](.*?)[\"]"
            },
            "color": "gold",
            "backgroundColor": "none",
            "overviewRulerColor": "none"
        },
        {
            "text": "DIALOG_LINE: NOT OK, SHOULD ALWAYS MATCH LINE START",
            "regex": {
                "pattern": "([-]{2,2}(.*))"
            },
            "color": "gold",
            "backgroundColor": "none",
            "overviewRulerColor": "none"
        },
        {
            "text": "COMMENTS: OK BUT BETTER IF MATCH LINE START",
            "regex": {
                "pattern": "(\/\/(?<text>.+))"
            },
            "color": "green",
            "backgroundColor": "none",
            "overviewRulerColor": "none"
        }
    ],
    "git.enabled": false
}

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