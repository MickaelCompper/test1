# TP Git

## Création du compte Github et du dépôt distant

1. Créer un compte sur la plateforme github
2. Créer un jeton d'accès personnel (aller dans settings > developer settings > personal access token > generate new token)
3. Donner un nom au jeton et sélectionner le contexte (cliquer sur "repo")
4. Générer le jeton et l'enregistrer quelque part (il n'est pas récupérable)
5. Créer un nouveau dépôt (aller dans your repositories > new)
6. Donner un nom au dépôt (par exemple "projet") puis valider

## Création du dépôt local et envoi vers le dépôt distant (sur github)

1. Depuis le terminal, se déplacer dans le dossier "sites/git/projet"
2. Initialiser un dépôt vide à l'aide de la commande *git init*
3. Créer un fichier *index.php* avec un peu de code php
4. Taper la commande *git add -A* pour ajouter le fichier au suivi (lorsque vous faites la commande *git status* le fichier doit apparaître en vert)
5. Taper la commande *git commit -m "écrire le nom de votre commit ici (par exemple first commit)"*
6. Si le commit n'est pas passé, il faudra peut-être renseigner votre nom et email de cette manière:
  * git config --global user.email "votre email utilisé lors de la création du compte github"
  * git config --global user.name "Votre nom d'utilisateur github"
7. Taper la commande *git branch -m main*
8. Lier votre dépôt local à votre dépôt distant à l'aide de la commande *git remote add origin https://github.com/{nom utilisateur}/{nom de votre dépôt}.git*
9. Envoyer les données vers github avec la commande *git push -u origin main*
10. Le mot de passe à utiliser est le jeton d'accès personnel
11. Vérifier sur github que ça a fonctionné

## Apporter des modifications

1. Modifier le fichier *index.php*
2. Ajouter les modifications au suivi avec *git add -A*
3. Créer un nouveau commit avec *git commit -m "message du commit"*
4. Envoyer vers github avec *git push -u origin main*

## Travail collaboratif

Vous allez par groupe de 2 ou 3, apporter des modifications aux fichiers du dépôt.

### Mise en place

Personne A (propriétaire du dépôt github) :
* Donner les droits sur le dépôt aux membres du groupe
* Cloner le projet dans un nouveau dossier avec la commande *git clone url du dépôt*

Personne B-C :
* Accepter les droits
* Cloner le projet dans un nouveau dossier avec la commande *git clone url du dépôt du propriétaire*

### Modifications de fichiers

Personne A :
* Ajouter un nouveau fichier *readme.md*
* Faire un nouveau commit et envoyer sur github

Personne B-C :
* Récupérer les modifications apportées par la personne A à l'aide de la commande *git pull origin main*
* Modifier le fichier *index.php*
* Faire un nouveau commit et envoyer sur github

Personne A :
* Récupérer les modifications apportées par les autres membres du groupe

### Modifications de fichiers avec conflits

Personne A :
* Créer le fichier *index.html* avec le contenu du fichier *index1.html* de ce dossier
* Faire un nouveau commit et envoyer sur github

Personne B-C :
* Récupérer les modifications apportées
* Modifier le fichier *index.html* avec le contenu du fichier *index2.html* de ce dossier
* Faire un nouveau commit (attention ne pas encore envoyer sur github !)

Personne A :
* Modifier le fichier *index.html* avec le contenu du fichier *index3.html* de ce dossier
* Faire un nouveau commit (attention ne pas encore envoyer sur github !)

Tout le monde :
* Envoyer sur github
* Que se passe t-il ?