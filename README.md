# Résumé des commandes Git

Lorsque vous créer un nouveau projet, vous devez initialiser le dépôt Git avec la commande `git init`.

Vous devez créer également un dépôt sur Github (New Repository)

Ensuite, vous devez choisir quels fichiers ajouter sur votre dépôt. Pour cela, vous pouvez utiliser la commande `git add`.

* `git add NOM_DU_FICHIER` : Pour ajouter uniquement un fichier choisi
* `git add *` : Pour ajouter tous les fichiers du répertoire courant

Une fois les fichiers ajoutés, vous devez indiquer un message qui expliquera ce que vous avez fait. Pour cela, vous pouvez utiliser la commande `git commit -m "MESSAGE"`.

Vous devez ensuite choisir sur quelle branche vous allez travailler. Par défaut, vous devez travailler sur la branche `main`. Pour choisir la branch main vous devez utiliser la commande `git branch -m main` <-- Cette commande est a exécuter une seule fois, comme git init.

Vous devez également indiquer à Git sur quel dépôt distant vous souhaitez travailler avec la commande `git remote add origin URL_DU_REPO`. Cette commande est a exécuter une seule fois, comme git init et git branch -m main.

Pour finir, pour envoyer les modifications sur le dépôt distant, vous devez utiliser la commande `git push -u origin main`.

Ensuite, à chaque fois que vous voulez envoyer vos modifications sur le dépôt distant, vous allez devoir utiliser les commandes suivantes en boucle :
* `git add *`
* `git commit -m "MESSAGE"`
* `git push`

INFO : Après le premier `git push -u origin main`, vous pouvez utiliser seulement `git push`.

## En résumé
### À la création d'un nouveau projet :
* `git init`
* `git add *`
* `git commit -m "MESSAGE"`
* `git branch -m main`
* `git remote add origin URL_DU_REPO`
* `git push -u origin main`

### À chaque nouvelle modification :
* `git add *`
* `git commit -m "MESSAGE"`
* `git push`

Readme modifié sur la nouvelle branche