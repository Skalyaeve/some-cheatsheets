# Vim


## Modes
<details><summary>Normal</summary>

| Commande | Description |
|-|-|
| `ESC` | Passer en mode normal |
| `:` | Exécuter une commande vim |
| `:!` | Exécuter une commande shell |
| `:h[elp] [exemple]` | Affiche l'aide |
| `:ter[minal]` | Ouvrir un terminal |
</details>
<details><summary>Sélection (visual mode)</summary>

| Commande | Description |
|-|-|
| `v` | Passer en mode sélection |
| `V` | Passer en mode sélection ligne |
| `ctrl + v` | Passer en mode sélection bloc |
</details>
<details><summary>Insertion (insert mode)</summary>

| Commande | Description |
|-|-|
| `i` | Passer en mode insertion |
| `a` | Passer en mode insertion après le curseur |
| `I` | Passer en mode insertion au début de la ligne |
| `A` | Passer en mode insertion à la fin de la ligne |
| `o` | Passer en mode insertion sur une nouvelle ligne en dessous |
| `O` | Passer en mode insertion sur une nouvelle ligne au dessus |
| `cc` | Supprimer la ligne et passer en mode insertion |
| `C` | Supprimer jusqu'à la fin de la ligne et passer en mode insertion |
| `cw` | Supprimer le mot suivant et passer en mode insertion |
| `ci` | Supprimer le texte encadré et passer en mode insertion |
| `R` | Passer en mode remplacement |
</details>


## Fichiers et répertoires
<details><summary>Ouvrir / Fermer</summary>

| Commande | Description |
|-|-|
| `:cd [path]` | Changer de répertoire |
| `:e[dit] <exemple>` | Ouvrir un fichier / répertoire |
| `:e#` | Swap entre les deux derniers fichiers ouverts |
| `:w [fichier]` | Enregistrer un fichier |
| `:wa` | Enregistrer tous les fichiers ouverts |
| `:x` | Enregistrer et fermer la fenêtre |
</details>
<details><summary>Gestion multiple</summary>

| Commande | Description |
|-|-|
| `:args` | Liste les fichiers ouverts |
| `:args fichier1 ...` | Ouvrir plusieurs fichiers |
| `:n` | Aller au fichier suivant |
| `:N` | Aller au fichier précédent |
| `:first` | Aller au premier fichier |
| `:last` | Aller au dernier fichier |
</details>
<details><summary>Buffers</summary>

| Commande | Description |
|-|-|
| `:ls` | Liste les buffers |
| `:bn[ext]` | Aller au buffer suivant |
| `:bp[revious]` | Aller au buffer précédent |
| `:b [numéro]` | Changer de buffer |
| `:bd[elete] [numéro]` | Supprimer un buffer |
</details>


## Navigation
<details><summary>Curseur</summary>

| Commande | Description |
|-|-|
| `gg` | Aller au début du fichier |
| `G` | Aller à la fin du fichier |
| `H` | Aller en haut de l'écran |
| `M` | Aller au milieu de l'écran |
| `L` | Aller en bas de l'écran |
| `0` | Aller au début de la ligne |
| `$` | Aller à la fin de la ligne |
| `:<numéro>` | Aller à la ligne `<numéro>` |
| `W` | Aller au début du mot suivant |
| `B` | Aller au début du mot précédent |
| `E` | Aller à la fin du mot |
| `*` | Aller au prochain mot identique |
| `#` | Aller au mot précédent identique |
| `%` | Aller au caractère fermant / ouvrant |
| `f<c>` | Aller au prochain caractère `<c>` |
| `F<c>` | Aller au caractère précédent `<c>` |
| `/<motif>` | Rechercher `<motif>` vers l'avant |
| `?<motif>` | Rechercher `<motif>` vers l'arrière |
| `n` | Aller au prochain résultat de recherche |
| `N` | Aller au résultat précédent de recherche |
| `zt` | Faire de la ligne actuelle la première ligne de l'écran |
| `zz` | Centrer la ligne actuelle dans l'écran |
| `zb` | Faire de la ligne actuelle la dernière ligne de l'écran |
| `maj + <flèche>` | Faire défiler l'écran |
</details>
<details><summary>Fenêtres</summary>

| Commande | Description |
|-|-|
| `:sp[lit] [fichier]` | Ouvrir une nouvelle fenêtre |
| `:vsp[lit] [fichier]` | Ouvrir une nouvelle fenêtre verticale |
| `:on[ly]` | Fermer toutes les fenêtres sauf celle active |
| `(ctrl + w) + <flèche>` | Passer à une autre fenêtre |
| `(ctrl + w) + <numéro> + w` | Passer à la fenêtre `<numéro>` |
| `(ctrl + w) + H` | Déplacer la fenêtre à gauche |
| `(ctrl + w) + J` | Déplacer la fenêtre en bas |
| `(ctrl + w) + K` | Déplacer la fenêtre en haut |
| `(ctrl + w) + L` | Déplacer la fenêtre à droite |
</details>
<details><summary>Onglets</summary>

| Commande | Description |
|-|-|
| `:tabe [fichier]` | Ouvrir un nouvel onglet |
| `:tabc[lose] [numéro]` | Fermer un onglet |
| `:tabn[ext]` | Aller à l'onglet suivant |
| `:tabp[revious]` | Aller à l'onglet précédent |
| `:tabfir[st]` | Aller au premier onglet |
| `:tabl[ast]` | Aller au dernier onglet |
| `:tabm[ove] <numéro>` | Déplacer l'onglet actuel à la position `<numéro>` |
</details>


## Modification
<details><summary>Remplacer</summary>

| Commande | Description |
|-|-|
| `r<c>` | Remplacer le caractère sous le curseur par `<c>` |
| `:s/<motif>/<remplacement>/` | Remplacer le premier `<motif>` par `<remplacement>` sur la ligne |
| `:s/<motif>/<remplacement>/g` | Remplacer tous les `<motif>` par `<remplacement>` sur la ligne |
| `:%s/<motif>/<remplacement>/` | Remplacer le premier `<motif>` par `<remplacement>` dans le fichier |
| `:%s/<motif>/<remplacement>/g` | Remplacer tous les `<motif>` par `<remplacement>` dans le fichier |
| `:%s/<motif>/<remplacement>/gc` | Remplacer tous les `<motif>` par `<remplacement>` dans le fichier avec confirmation |
| `u` | Annuler |
| `ctrl + r` | Rétablir |
| `J` | Fusionner la ligne suivante avec la ligne actuelle |
| `:'<,'>norm I<motif>` | Prefixer chaque ligne de la sélection avec `<motif>` |
| `:'<,'>norm A<motif>` | Suffixer chaque ligne de la sélection avec `<motif>` |
| `>` / `<` | Indenter / Désindenter la sélection |
</details>
<details><summary>Supprimer (Couper)</summary>

| Commande | Description |
|-|-|
| `x` | Supprimer le caractère sous le curseur |
| `X` | Supprimer le caractère précédent |
| `d` | Supprimer la sélection |
| `dd` | Supprimer la ligne |
| `D` | Supprimer jusqu'à la fin de la ligne |
| `d0` | Supprimer jusqu'au début de la ligne |
| `dw` | Supprimer le mot suivant |
| `db` | Supprimer le mot précédent |
| `d<numéro>w` | Supprimer les `<numéro>` mots suivants |
</details>
<details><summary>Copier / Coller</summary>

| Commande | Description |
|-|-|
| `y` | Copier la sélection |
| `yy` | Copier la ligne |
| `Y` | Copier la ligne |
| `yw` | Copier le mot sous le curseur |
| `y0` | Copier jusqu'au début de la ligne |
| `y$` | Copier jusqu'à la fin de la ligne |
| `p` | Coller après le curseur |
| `P` | Coller avant le curseur |
</details>
