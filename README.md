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

# Exercice 0
* Créer un nouveau dépôt Github
* Sur votre ordinateur, créer un nouveau dossier et collez dedans un projet que vous avez déjà réalisé en HTML/CSS (HomeKey, Vividly, etc.)
* Créer un fichier README.md avec un contenu minimal (au moins un titre, une description)
* Faire en sorte d'envoyer votre projet sur Github

# Pull Request
C'est une fonctionnalité clé des système de gestion de version basées sur git comme Github, Gitlab, BitBucket. Elle représente une demande de fusion des modifications (commits) d'une branche vers une autre, généalement de la branche d'une fonctionnalité vers la branche principale d'un projet.

## Concept de la Pull Request (PR)
**Collaboration et revue de code** : La PR n'est pas seulement un mécanisme de fusion de code. C'est aussi un outil de collaboration. Lorsqu'un développeur soummet une PR, d'autres membres de l'équipe peuvent la consulter, laisser des commentaires, suggérer des modifications et même proposer des commits pour améliorer la PR avant qu'elle ne soit fusionnée.

**Point de contrôle** : Avant la fusion, la PR fournit un point de contrôle pour s'assurer que le code respecte les qualités, passe tous les tests et n'introduit pas de régressions.

**Intégration avec CI/CD** : Les PR sont souvent intégrées avec des outils d'Intégration Continue (CI) et de Livraison Continue (CD). Lorsqu'une PR est soumise, des tests automatis"s peuvent être déclenchés, et le résultat de ces tests est souvent signalé directement dans l'interface de la PR.

## Faire une PR
**Fork du repository**
Avant de pouvoir soumettre une PR, vous devez avoir une copie du repository sur votre compte Github. Si ce n'est pas déjà fait :
1. Aller sur la page Github du projet auquel vous souhaitez contribuer
2. Cliquer sur le bouton "Fork" situié en haut à droite de la page. Cela créera une copie du projet sur votre compte Github personnel.

**Cloner le fork**
Après avoir fait un fork, vous allez pouvoir travailler dessus. pour cela, vous allez devoir le cloner sur votre propre machine

```bash
git clone URL_DU_DEPOT (Attention, c'est VOTRE repo que vous devez cloner, pas celui du projet original)
git clone https://github.com/JackAdamsJenkins/repo-olivia.git
```

**Créer une nouvelle branche**
Il est conseillé de créer une nouvelle branche pour chaque fonctionnalité ou correction. Cela vous permet de garder le travail organisé et séparé.
Pour créer une nouvelle branche, vous devez utiliser la commande `git checkout -b NomDeLaNouvelleBranche`

**Exemples :**
```
git checkout -b nom_de_la_branche
git checkout -b interfaceGUI
git checkout -b correctionBug
git checkout -b search
```