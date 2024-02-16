# Vim

## General
<details><summary>General</summary>

| Commande | Description | Racourci |
|-|-|-|
| `:q` | Quitter | ``
| `:w` | Sauvegarder |
| `:wq` | Sauvegarder et quitter |
| `:e [file]` | Ouvrir un fichier |
</details>
<details><summary>Fenêtres</summary>

| Commande | Description | Racourci |
|-|-|-|
| `:sp` | Split horizontal | `ctrl + w + s` |
| `:sp [file]` | Ouvrir un fichier dans un split |
| `:vsp [file]` | Ouvrir un fichier dans un split vertical |
</details>
<details><summary>Onglets</summary>

| Commande | Description | Racourci |
|-|-|-|
| `:tabe [file]` | Ouvrir un fichier dans un nouvel onglet |
| `:tabnew` | Ouvrir un nouvel onglet |
| `:tabclose` | Fermer l'onglet actuel |
| `:tabnext` | Aller à l'onglet suivant |
| `:tabprevious` | Aller à l'onglet précédent |
| `:tabfirst` | Aller au premier onglet |
| `:tablast` | Aller au dernier onglet |
</details>
<details><summary>Buffers</summary>

| Commande | Description |
|-|-|
| `:ls` | Liste les buffers |
| `:b [buffer]` | Aller à un buffer |
| `:bd` | Supprimer le buffer actuel |
| `:bd [buffer]` | Supprimer un buffer |
| `:bd [buffer]!` | Supprimer un buffer sans se soucier des modifications |
| `:bd[elete]` | Supprimer le buffer actuel |
| `:bd[elete] [buffer]` | Supprimer un buffer |
| `:bd[elete] [buffer] [buffer]` | Supprimer plusieurs buffers |
| `:bd[elete] [buffer]-[buffer]` | Supprimer une plage de buffers |
| `:bd[elete] [buffer]-[buffer] [buffer]` | Supprimer une plage de buffers |
</details>

- `:[any other]!`: Fait l'action sans se soucier des modifications 

### Visual mode
<details><summary>Insertion</summary>

| Commande | Description |
|-|-|
| `i` | Passer en mode insertion avant le curseur |
| `a` | Passer en mode insertion après le curseur |
| `I` | Passer en mode insertion au début de la ligne |
| `A` | Passer en mode insertion à la fin de la ligne |
</details>
<details><summary>Supression</summary>

| Commande | Description |
|-|-|
| `x` | Supprime le caractère sous le curseur |
</details>
