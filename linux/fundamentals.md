# Fundamentals
> work in progress

## Structure
<details><summary>Composants</summary>

| Composant | Description | Exemple |
|-|-|-|
| Bootloader | Programme qui charge le noyau du système. | GRUB |
| Kernel | Noyau du système. | Linux |
| Daemons | Processus en arrière-plan. | `sshd`, `httpd` |
| Shell | Interface en ligne de commande. | `bash`, `zsh` |
| Graphics Server | Serveur graphique. | Xorg, Wayland |
| Desktop Environment | Environnement graphique. | GNOME, xfce |
| Utilities | Applications et outils. | `ls`, `ps` |
</details>
<details><summary>Système de fichier</summary>

| Répertoire | Description |
|-|-|
| `/` | Contient tous les autres répertoires. |
| `/boot` | Fichiers nécessaires au démarrage du système. |
| `/dev` | Fichiers représentant les périphériques. |
| `/sys` | Informations sur le système. |
| `/proc` | Informations sur les processus en cours. |
| `/etc` | Fichiers de configuration. |
| `/var` | Fichiers de données variables. |
| `/run` | Fichiers relatifs à l'exécution du système. |
| `/usr` | Applications et les fichiers partagés. |
| `/lib` | Bibliothèques partagées. |
| `/bin` | Binaires essentielles. |
| `/sbin` | Binaires essentielles à l'administration du système. |
| `/opt` | Logiciels optionnels. |
| `/home` | Répertoires personnels des utilisateurs. |
| `/root` | Répertoire personnel de l'utilisateur root. |
| `/srv` | Données des services fournis par le système. |
| `/tmp` | Fichiers temporaires. |
| `/mnt` | Points de montage temporaires. |
| `/media` | Points de montage pour les supports amovibles. |
</details>
<details><summary>Fichiers important</summary>

| Chemin | Description |
|-|-|
| `/etc/passwd` | Informations sur les utilisateurs. |
| `/etc/shadow` | Mots de passe des utilisateurs. |
| `/etc/group` | Informations sur les groupes. |
| `/etc/sudoers` | Configuration de sudo. |
| `/etc/hosts` | Fichier de résolution de noms. |
| `/etc/resolv.conf` | Configuration des serveurs DNS. |
| `/etc/fstab` | Configuration des points de montage. |
| `/etc/crontab` | Configuration des tâches planifiées. |
| `/etc/ssh/sshd_config` | Configuration du serveur SSH. |
| `/etc/host.allow` | Configuration des accès autorisés. |
| `/etc/host.deny` | Configuration des accès refusés. |
</details>

## Commandes basiques

### Système
<details><summary>Énumération</summary>

| Commande | Description | Exemple |
|-|-|-|
| `env` | Informations sur l'environnement. | `env` |
| `uname` | Informations sur le système. | `uname -a` |
| `hostname` | Nom d'hôte du système. | `hostname` |
| `service` | Informations sur les services. | `service --status-all` |
| `systemctl` | Informations sur les services. | `systemctl` |
| `cron` | Informations sur les tâches planifiées. | `crontab -l` |
| `mount` | Informations sur les points de montage. | `mount` |
| `fdisk` | Informations sur les partitions. | `fdisk -l` |
| `lsof` | Informations sur les fichiers ouverts. | `lsof` |
| `lsblk` | Informations sur les périphériques de stockage. | `lsblk` |
| `lsusb` | Informations sur les périphériques USB. | `lsusb` |
| `lspci` | Informations sur les périphériques PCI. | `lspci` |
| `journalctl` | Informations sur les logs. | `journalctl` |
</details>
<details><summary>Management</summary>

| Commande | Description | Exemple |
|-|-|-|
| `export` | Définit une variable d'environnement. | `export VAR=value` |
| `unset` | Supprime une variable d'environnement. | `unset VAR` |
| `service` | Gestion des services. | `man service` |
| `systemctl` | Gestion des services. | `man systemctl` |
| `cron` | Gestion des tâches planifiées. | `crontab -h` |
| `mount` | Montage de périphériques. | `mount /dev/sda1 /mnt` |
| `fdisk` | Gestion des partitions. | `fdisk -h` |
| `reboot` | Redémarre le système. | `reboot` |
| `shutdown` | Éteint le système. | `shutdown -h now` |
| `rsync` | File backup | `rsync -h` |
</details>

### Réseau
<details><summary>Énumération</summary>

| Commande | Description | Exemple |
|-|-|-|
| `ip` | Informations sur les interfaces réseau. | `ip a` |
| `ifconfig` | Informations sur les interfaces réseau. | `ifconfig` |
| `iptables` | Informations sur les règles de pare-feu. | `iptables -L` |
| `ufw` | Informations sur les règles de pare-feu. | `ufw status` |
| `route` | informations sur les routes. | `route` |
| `netstat` | Informations sur les connexions réseau. | `netstat -tulpen` |
| `ss` | Informations sur les connexions réseau. | `ss -tulpen` |
</details>
<details><summary>Management</summary>

| Commande | Description | Exemple |
|-|-|-|
| `ip` | Gestion des interfaces réseau. | `ip -h` |
| `ifconfig` | Gestion des interfaces réseau. | `ifconfig -h` |
| `iptables` | Gestion des règles de pare-feu. | `iptables -h` |
| `ufw` | Gestion des règles de pare-feu. | `ufw -h` |
| `route` | Gestion des routes. | `route -h` |
</details>

### Système de fichier
<details><summary>Énumération</summary>

| Commande | Description | Exemple |
|-|-|-|
| `pwd` | Affiche le répertoire courant. | `pwd` |
| `ls` | Liste les fichiers et répertoires. | `ls -la` |
| `tree` | Affiche l'arborescence des fichiers. | `tree` |
| `locate` | Recherche des fichiers. | `locate file` |
| `find` | Recherche des fichiers. | `find / -name exemple` |
| `whereis` | Affiche le chemin d'accès d'une commande. | `whereis ls` |
| `cat` | Affiche le contenu d'un fichier. | `cat file` |
| `diff` | Compare deux fichiers. | `diff file1 file2` |
</details>
<details><summary>Managment</summary>

| Commande | Description | Exemple |
|-|-|-|
| `cd` | Change le répertoire courant. | `cd /path` |
| `mkdir` | Crée un répertoire. | `mkdir dir` |
| `touch` | Crée un fichier. | `touch file` |
| `rm` | Supprime des fichiers ou répertoires. | `rm -rf /` |
| `mv` | Déplace ou renomme des fichiers ou répertoires. | `mv file1 file2` |
| `cp` | Copie des fichiers ou répertoires. | `cp file1 file2` |
| `ln` | Crée des liens symboliques ou physiques. | `ln -s file link` |
| `chmod` | Modifie les permissions d'un fichier. | `chmod 777 file` |
| `chown` | Modifie le propriétaire d'un fichier. | `chown -R user:group dir` |
</details>

### Utilisateurs et Groupes
<details><summary>Énumération</summary>

| Commande | Description | Exemple |
|-|-|-|
| `id` | Identité de l'utilisateur. | `id` |
| `groups` | Groupes de l'utilisateur. | `groups` |
| `sudo -l` | Droits sudo de l'utilisateur. | `sudo -l` |
| `who` | Informations sur les utilisateurs connectés. | `who` |
</details>
<details><summary>Management</summary>

| Commande | Description | Exemple |
|-|-|-|
| `useradd` | Crée un utilisateur. | `useradd -m -s /bin/bash user` |
| `userdel` | Supprime un utilisateur. | `userdel user` |
| `usermod` | Modifie un utilisateur. | `usermod -aG sudo user` |
| `passwd` | Modifie le mot de passe d'un utilisateur. | `passwd user` |
| `addgroup` | Crée un groupe. | `addgroup group` |
| `delgroup` | Supprime un groupe. | `delgroup group` |
</details>

### Processus
<details><summary>Énumération</summary>

| Commande | Description | Exemple |
|-|-|-|
| `ps` | Informations sur les processus en cours. | `ps aux` |
| `strace` | Trace les appels systèmes faits par un processus. | `strace -p 1` |
| `ltrace` | Trace les appels de bibliothèques faits par un processus. | `ltrace -p 1` |
</details>
<details><summary>Management</summary>

| Commande | Description | Exemple |
|-|-|-|
| `kill` | Envoie un signal à un processus. | `kill -9 1234` |
| `fg` | Met un processus en avant-plan. | `fg` |
| `bg` | Met un processus en arrière-plan. | `bg` |
| `jobs` | Liste les processus en arrière-plan. | `jobs` |
</details>

### Chaînes de caractères
<details><summary>Afficher</summary>

| Commande | Description | Exemple |
|-|-|-|
| `less` | Affiche une chaîne de caractères dans une interface interactive. | `less file` |
| `more` | Affiche une chaîne de caractères petit à petit. | `more file` |
| `head` | Affiche les premières lignes d'une chaîne de caractères. | `head file` |
| `tail` | Affiche les dernières lignes d'une chaîne de caractères. | `tail file` |
| `wc` | Compte les mots, lignes et caractères d'une chaîne de caractères. | `wc file` |
</details>
<details><summary>Modifier</summary>

| Commande | Description | Exemple |
|-|-|-|
| `grep` | Recherche un motif dans une chaîne de caractères. | `grep pattern file` |
| `awk` | Manipule une chaîne de caractères. | `awk '{print $1}' file` |
| `sed` | Manipule une chaîne de caractères. | `sed 's/pattern/replacement/g' file` |
| `tr` | Remplace des caractères dans une chaîne de caractères.. | `tr 'a' 'b'` |
| `cut` | Coupe certaines parties d'une chaîne de caractères. | `cut -d: -f1 file` |
| `uniq` | Supprime les lignes en double d'une chaîne de caractères. | `uniq file` |
| `sort` | Trie une chaîne de caractères. | `sort file` |
</details>

### MISC
<details><summary>Interactions réseau</summary>

| Commande | Description | Exemple |
|-|-|-|
| `ping` | Test de connectivité. | `ping google.com` |
| `traceroute` | Affiche le chemin pris par les paquets. | `traceroute google.com` |
| `curl` | Affiche une ressource web. | `curl google.com` |
| `wget` | Télécharge une ressource web. | `wget google.com` |
| `nc` | Outil de communication réseau. | `nc -vlnp 4242` |
| `ssh` | Connexion SSH. | `ssh user@host` |
| `scp` | Transfert de fichiers SSH. | `scp user@host:/path dst` |
</details>
