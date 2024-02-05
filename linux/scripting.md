# Scripting

<details><summary>Variables</summary>

| Variable | Description | Exemple |
|-|-|-|
| `$#` | Nombre d'arguments | `echo $#` |d
| `$@` | Argument**s** | `echo $@` |
| `$[1-9]` | Argument | `echo $2` |
| `$0` | Nom du script | `echo $0` |
| `$$` | PID du script | `echo $$` |
| `$?` | Code de retour de la dernière commande | `echo $?` |
| `$!` | PID du dernier processus en arrière-plan | `echo $!` |
| `$var` | Variable | `echo $var` |
| `${var}` | Variable | `echo ${var}iable` |
</details>
<details><summary>Tableaux</summary>

#### Déclaration
```sh
array1=(value1 value2 value3)
array2=(
    value1
    value2
    value3
)
```
#### Accès
```sh
echo ${array1[0]}
echo ${array1[@]}
```
```sh
for value in ${array1[@]}; do
    echo $value
done
```
</details>
<details><summary>Arithmétique</summary>

| Opérateur | Description | Exemple |
|-|-|-|
| `+` | Addition | `echo $(( 1 + 1 ))` |
| `-` | Soustraction | `echo $(( 1 - 1 ))` |
| `*` | Multiplication | `echo $(( 1 * 1 ))` |
| `/` | Division | `echo $(( 1 / 1 ))` |
| `%` | Modulo | `echo $(( 1 % 1 ))` |
| `**` | Exposant | `echo $(( 1 ** 1 ))` |
| `++` | Incrémentation | `echo $(( i++ )) && echo $i` |
| `--` | Décrémentation | `echo $(( i-- )) && echo $i` |
</details>
<details><summary>Fonctions</summary>

#### Déclaration
```sh
exemple() {
    # code
}
```
#### Appel
```sh
exemple arg1 arg2
```
</details>


## Structures de contrôle

<details><summary>Boucles</summary>

- `for`: Boucle pour chaque élément.
```sh
for x in y; do
    # code
done
```
- `while`: Boucle tant que la condition est vraie.
```sh
while condition; do
    # code
done
```
- `until`: Boucle jusqu'à ce que la condition soit vraie.
```sh
until condition; do
    # code
done
```
- `break`: Sortir de la boucle.
- `continue`: Passer à l'itération suivante.
</details>
<details><summary>Conditionnel</summary>

```sh
if conditionnel; then
    # code
elif conditionnel; then
    # code
else
    # code
fi
```
<details><summary>Conditionnel basique</summary>

```sh
if [ condition ]; then
```
```sh
if test condition; then
```
- Opérateurs logiques:
    * `-a`: AND
    ```sh
    if [ condition1 -a condition2 ]; then
    ```
    * `-o`: OR
    ```sh
    if [ condition1 -o condition2 ]; then
    ```
    * `!`: NOT
    ```sh
    if [ ! condition ]; then
    ```
</details>
<details><summary>Conditionnel avancé</summary>

```sh
if [[ condition ]]; then
```
- Opérateurs logiques **supplémentaires**:
    * `&&`: AND
    ```sh
    if [[ condition1 && condition2 ]]; then
    ```
    * `||`: OR
    ```sh
    if [[ condition1 || condition2 ]]; then
    ```
    * `!`: NOT
    ```sh
    if [[ ! condition ]]; then
    ```
</details>
<details><summary>Conditionnel arithmétique</summary>

```sh
if (( condition )); then
```
- Fonctionne uniquement avec des nombres.
- Ne supporte pas les opérateurs logiques.
- Supporte uniquement les opérateurs de comparaison arithmétiques suivants:
    * `==` Égal
    * `!=` Différent
    * `>` Supérieur
    * `<` Inférieur
    * `>=` Supérieur ou égal
    * `<=` Inférieur ou égal
</details>

#### select & case
- `select`: Menu interactif.
- `case`: Pareil que `if`.
```sh
select var in a b c; do
    case $var in
        a)
            # code
            ;;
        b)
            # code
            ;;
        c)
            # code
            ;;
        *)
            # code
            ;;
    esac
done
```
</details>
</details>


## Opérateurs de comparaison

<details><summary>Chaînes de caractères</summary>

| Opérateur | Description | Exemple |
|-|-|-|
| `-z` | Chaîne vide | `if [ -z "$var" ]; then` |
| `-n` | Chaîne non vide | `if [ -n "$var" ]; then` |
| `=` | Égal | `if [ "a" = "a" ]; then` |
| `!=` | Différent | `if [ "a" != "b" ]; then` |
| `>` | Supérieur ASCII | `if [ "a" > "b" ]; then` |
| `<` | Inférieur ASCII | `if [ "a" < "b" ]; then` |
| `>=` | Supérieur ou égal ASCII | `if [ "a" >= "b" ]; then` |
| `<=` | Inférieur ou égal ASCII | `if [ "a" <= "b" ]; then` |
</details>
<details><summary>Nombres</summary>

| Opérateur | Description | Exemple |
|-|-|-|
| `-eq` | Égal | `if [ 1 -eq 1 ]; then` |
| `-ne` | Différent | `if [ 1 -ne 2 ]; then` |
| `-gt` | Supérieur | `if [ 2 -gt 1 ]; then` |
| `-lt` | Inférieur | `if [ 1 -lt 2 ]; then` |
| `-ge` | Supérieur ou égal | `if [ 2 -ge 1 ]; then` |
| `-le` | Inférieur ou égal | `if [ 1 -le 2 ]; then` |
</details>
<details><summary>Fichiers</summary>

| Opérateur | Description | Exemple |
|-|-|-|
| `-e` | Existe | `if [ -e /path/to/file ]; then` |
| `-f` | Est un fichier | `if [ -f /path/to/file ]; then` |
| `-d` | Est un répertoire | `if [ -d /path/to/file ]; then` |
| `-L` | Est un lien symbolique | `if [ -L /path/to/file ]; then` |
| `-s` | Est de taille supérieure à 0 | `if [ -s /path/to/file ]; then` |
| `-r` | Read access | `if [ -r /path/to/file ]; then` |
| `-w` | Write access | `if [ -w /path/to/file ]; then` |
| `-x` | Execute access | `if [ -x /path/to/file ]; then` |
| `-O` | Appartient à l'utilisateur en cours | `if [ -O /path/to/file ]; then` |
| `-G` | Appartient au groupe de l'utilisateur en cours | `if [ -G /path/to/file ]; then` |
| `-nt` | Est plus récent que | `if [ /path/to/file1 -nt /path/to/file2 ]; then` |
| `-ot` | Est plus vieux que | `if [ /path/to/file1 -ot /path/to/file2 ]; then` |
</details>
