# Comment cloner le projet sur son ordinateur

## Se connecter à Github

Tout d'abord, il faut vous connecter à Github sur votre ordinateur.

Pour ce faire, faites les commandes suivantes :
```bash
git config --global user.name "John Doe"
```
```bash
git config --global user.email johndoe@example.com
```

## Créer une clé SSH

Ensuite, pour récupérer un dépôt Github, il vous faut connecter votre compte à votre ordinateur via une clé SSH.

Pour ce faire, générer une clé SSH avec la commande suivante :

```bash
ssh-keygen -t ed25519 -C "votre.email@exemple.com"
```

Puis copier la clé SSH Publique via cette commande :
```bash
pbcopy < <emplacement declare votre clé>/id_ed25519.pub
```

Ensuite, aller sur GitHub dans :
Menu Settings -> SSH and GPG keys -> New SSH key

Donnez-y un titre, choisissez 'Authentication Key' et insérez-y la clé SSH que vous venez de copier dans la zone 'Key'.

Ensuite, tester la connexion avec la commande :
```bash
ssh -T git@github.com
```

Si vous obtenez un message comme : 'Hi John! You've successfully authenticated, but GitHub does not provide shell access.' c'est que tout est bon !

## Installer le projet

Clonez le dépôt sur votre machine locale via la commande :
```bash 
git clone git@github.com:LaureEverwyn/Partiels_MDS.git
```

Et normalement, tout est bon !

## Envoyer des modifications sur le dépôt

### ⚠️ IMPORTANT ⚠️
Avant toute chose, assurez-vous d'avoir bien récupéré toutes les modifications du dépôt avec la commande :
```bash
git pull
```

Cela vous évitera de devoir résolver des conflits git relou à corriger :)

Après avoir fait de multiples modifications, vous pouvez envoyer vos modifications sur le dépôt en suivant ces étapes :

Ajoutez vos modifications avec la commande 
```bash 
git add .
```

Le point ici signifie que vous ajoutez tous les fichiers modifiés.

Committez vos modifications avec la commande
```bash
git commit -m "votre_message_de_commit"
```

Comme message de commit, expliquer brièvement ce que vous avez fait.

Poussez vos modifications sur le dépôt distant avec la commande 
```bash
git push
```

Et normalement, tout est bon !