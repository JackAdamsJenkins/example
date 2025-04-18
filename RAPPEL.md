# Rappel du cours

## Git 
C'est l'outil de gestion de version.

## GitHub
C'est un service de gestion de version en ligne.
Similaire à BitBucket, GitLab, etc.

## Démarrer un projet

* On commence par créer un nouveau dépôt sur Github
   * On renseigne au minimum le titre du projet
   * On peut ajouter une description
   * On peut choisir une licence
   * On peut choisir un README
   * ...


Ensuite, dans votre dossier de travail (sur votre ordinateur) :
* On initialise le dépôt avec la commande `git init`
* On ajoute tous les fichiers du projet avec la commande `git add *` ou `git add nom_du_fichier` ou `git add .`
* On ajoute un message de commit avec la commande `git commit -m "MESSAGE"`
* On crée une branche principale avec la commande `git branch -m main`
* On fait la liaison avec le dépôt distant avec la commande `git remote add origin URL_DU_REPO`
* On envoie les modifications sur le dépôt distant avec la commande `git push -u origin main`

Ensuite, à chaque fois que vous souhaitez envoyer vos modifications sur le dépôt distant, vous allez devoir utiliser les commandes suivantes en boucle :
* `git add *`
* `git commit -m "MESSAGE"`
* `git push`

## Pull Request
En gros : une PR est une demande de fusion de code. Elle permet de faire des modifications sur une branche, de vérifier que le code est correct, de soumettre les modifications, etc. C'est ce qui est utilisé pour collaborer sur un projet open source (ou entre collègues).

### Faire une PR
* Trouver un repository (sur github) sur lequel vous souhaitez contribuer
* En haut à droite, cliquer sur le bouton "Fork"
   * Donner un nom au projet (ou laissez le nom par défaut)
   * Cliquer sur "Create fork"

Ensuite, sur votre machine :
* Cloner le fork : `git clone url_de_VOTRE_depot` (pas celui du projet original)
* Ouvrir le projet dans votre IDE
* Créer une nouvelle branche : `git checkout -b nom_de_la_branche`
* Faites les modifications que vous souhaitez
* Ajoutez les fichiers modifiés : `git add *`
* Ajoutez un message de commit : `git commit -m "MESSAGE"`
* Envoyez les modifications sur le dépôt distant : `git push -u origin nom_de_la_branche`

Ensuite, c'est sur le dépôt Github que ça se passe :
* Aller sur la page du projet
* Cliquer sur le bouton "Compare & pull request"
* Choisir la branche sur laquelle vous souhaitez fusionner les modifications (Depuis votre branche vers la branche du repo distant)
* Vous valiez les modifications que vous souhaitez fusionner en cliquant sur "Create pull request"

La personne qui a créé le projet peut maintenant voir votre PR et vous donner des commentaires ou valider les modifications.

