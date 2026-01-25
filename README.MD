- [Sujet : Faire Burger Quizz !](#sujet---faire-burger-quizz--)
- [Notation](#notation)
- [Environnement](#environnement)
- [Déroulement](#d-roulement)
- [Creation des comptes](#creation-des-comptes)
  * [GitHub](#github)
  * [Gitpod](#gitpod)
    + [Creation compte](#creation-compte)
    + [Configuration du compte](#configuration-du-compte)
- [Fork du projet](#fork-du-projet)
- [TP1 - Stack Back-End](#tp1---stack-back-end)
- [Utiliser gitpod](#utiliser-gitpod)
  * [Test de commit](#test-de-commit)
- [API Springboot](#api-springboot)
  * [Developpement](#developpement)
  * [Packaging de l'app, execution et mesures](#packaging-de-l-app--execution-et-mesures)
- [API Quarkus](#api-quarkus)
  * [Developpement](#developpement-1)
  * [Packaging de l'app, execution et mesures](#packaging-de-l-app--execution-et-mesures-1)
- [Pull Request](#pull-request)
- [Commandes Utiles](#commandes-utiles)



# Sujet : Faire Burger Quizz !

Vous avez 4 séances de TD/TP pour  produire un site web qui permettent de répondre à des questions et  donne le score.

# Notation
 - 2pt  de rendu par séance
 - 12 pt de Questions ouvertes lors du dernier tp  (1H dernière seance)

> [!WARNING]
> Noubliez pas de faire votre pullRequest en fin de td/tp

> [!TIP]
> Il y a des commandes utiles en bas de page.

# Environnement
L'ensemble des  4 TD/TP sont à réaliser sur **_GitHub Codespaces_**.

**_GitHub Codespaces_** est un IDE complet basé sur VS Code accessible directement dans votre navigateur. Aucun besoin d'installer Java, Node.js ou Maven sur votre machine : l'environnement est pré-configuré avec toutes les dépendances nécessaires. Elle automatise la préparation des environnements (dépendances, configurations, etc.), réduisant ainsi le temps d’installation et les problèmes de compatibilité.
  

# Déroulement
Dans le monde de l'*Open Source*, lorsque l'on veut contribuer à un projet, on propose des évolutions à une base de code (un **repo**) qui  seront approuvées ou non par un validateur (**reviewer**). C'est ce que l'on appel  **faire une PR**.

Vous allez reproduire le processus d'une PR pour chacun des TD/TP.

Ainsi pour chacun des TD/TPS, il faudra:
1. Dupliquer (**Forker**) le projet github
1. Modifier / compléter des fichier du repo. forké
1. Commiter vos modifs sur votre repo.
1. Proposer vos modifications sur le repo. parent (**PullRequest**)

# Creation du compte
Vous allez créer 1 compte  sur GitHub (à moins que vous n'en ayez déjà un et que vous n'ayez pas consommé tout votre quotas d'utilisation de Codespaces). Ce compte sera utilisé lors des 4TD/TP.

## GitHub
Dans cette section nous créons un compte sur Github. Si vous en avez déjà vous pouvez passer à l'étape suivante.
1. Se rendre sur https://github.com
1. Bouton Sign up
![Github1](assets/GitHub1.png)
1. Remplissez  le formulaire d'inscription
![Github1](assets/GitHub2.png)
1. Connecter vous au site github avec le nouveau compte créé
1. Remplissez le formulaire
![Github1](assets/GitHub3.png)


# Fork du projet
L'objectif est de créer une copie du projet 'miage-numres-step1' sur votre compte github.

1. Se rendre sur le projet github [miage-numres-step1] (https://github.com/aepsilon-tek/miage-numres-step1)
1. Fork du projet grâce au bouton

![Capture d'écran](assets/Fork1.png)
![Capture d'écran](assets/Fork2.png)


# TP1 - Stack Back-End
L'architecture   générale de  l'application  Burger Quizz est la suivante :
![Capture d'écran](assets/Archi.png)

Une application web consomme une API Rest  qui s'appuie sur une base de données relationnelles en  mémoire **H2**.

Ce TP1 doit permettre de  choisir la  stack d'implementation de l'api. Le choix est à faire entre **Springboot** et **Quarkus**.


# Utiliser GitHub codespaces

1. Rendez-vous sur la page principale de votre projet forké
![Capture d'écran](assets/GitHubFork.png)
1. En haut de cette page, cliquez sur le bouton vert <> Code
1. Sélectionnez l'onglet Codespaces
1. Cliquez sur Create codespace on main
![Capture d'écran](assets/GitHubCodeSpaceSettup.png)
1. Attendez environ 1 à 2 minutes que l'environnement se construise (le système installe Java, Node.js et les extensions nécessaires automatiquement).

Sinon vous pouvez clicquer ici  [![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=${github.repository_id})

> [!TIP]
> Fermez la fenêtre de Copilot, vous n'en avez pas besoin.

> [!WARNING]
> Assurez-vous d'avoir forké ce projet sur votre compte personnel avant de cliquer sur le bouton ci-dessus, sinon vous ne pourrez pas enregistrer (pusher) vos modifications.

> [!WARNING]
> Vous disposez de 60 heures gratuites par mois. Quand vous avez terminé votre travail, cliquez sur le nom du Codespace en bas à gauche et choisissez Stop Current Codespace.
![Capture d'écran](assets/GitHubStop.png)


Vous êtes désormais connecté à votre environnement de developpement.

## Test de commit
1. Répondez aux questions Q1 et Q2 dans le fichier **_Questions.md_**
2. Commiter & Pusher
3. Vérifier sur le site github que dans votre repo le fichier  **_Questions.md_** contient bien vos modifications


# API Springboot

## Developpement
1. Lancer application `springboot` en mode développement dans un Terminal
1. Tester dans un second Terminal que l'api répond : ```curl -w "\n" http://localhost:8080/api/hello ```
1. Modifier le contenu du message renvoyé
1. Tester que la modification fonctionne
1. Commiter & Pusher la modification du fichier


## Packaging de l'app, execution et mesures
1. Dans le terminal, construire l'application springboot
1. Lancer la commande `java -jar api-springboot/target/api-springboot-0.0.1-SNAPSHOT.jar`
1. Tester que l'Api répond
1. Mesurer la mémoire consommer par l'api SpringBoot `ps -e -o pid,rss,args | grep api-springboot`
Répondre aux questions Q3,Q4,Q5 et Q6 du fichier **_Questions.md_**
1. Commiter  & Pusher le fichier **_Questions.md_**


# API Quarkus
## Developpement
1. Lancer application `quarkus` en mode développement dans un Terminal
1. Tester dans un second Terminal que l'api répond : ```curl -w "\n" http://localhost:8080/hello ```
1. Modifier le contenu du message renvoyé
1. Tester que la modification fonctionne
1. Commiter & Pusher la modification du fichier


## Packaging de l'app, execution et mesures
1. Dans le terminal, construire l'application quarkus en mode JVM
1. Lancer la commande `java -jar api-quarkus/target/quarkus-app/quarkus-run.jar`
1. Mesurer la mémoire consommer par l'api quarkus `ps -e -o pid,rss,args | grep quarkus-run`
Répondre aux questions Q7,Q8 et Q9 du fichier **_Questions.md_**

1. Installer GraalVM dans un terminal : `sdk install java 21.0.2-graalce`
1. Dans le terminal, construire l'application quarkus en mode Natif
1. Lancer la commande `./api-quarkus/target/api-quarkus-1.0.0-SNAPSHOT-runner`
1. Mesurer la mémoire consommer par l'api quarkus `ps -e -o pid,rss,args | grep runner`
Répondre aux questions Q10,Q11  du fichier **_Questions.md_**


1. Commiter  & Pusher le fichier **_Questions.md_**

# Pull Request
Une fois tous vos commits & Push réalisés sur votre repo, il est nécessaire de faire la **Pull Request** sur le repo **parent**.
Pour cela, il suffit de :
1. Se rendre sur votre compte personnel sur `GitHub`.
1. Sur la page principale, se rendre sur `Contribute` > `Open pull Request`
![Capture d'écran](assets/PullRequest1.png)
1. Remplir le titre de la pull request en précisant votre nom (vos noms) et `Create pull request`
![Capture d'écran](assets/PullRequest2.png)

# Commandes Utiles
* ```./mvnw clean compile ``` : Compilation des 2 modules (`api-quarkus` et `api-springboot` ) du projet
* ```./mvnw spring-boot:run  -pl api-springboot ``` : Lancement du projet `api-springboot` en mode developpement
* ```./mvnw clean package  -pl api-springboot ``` : Construction du projet `api-springboot`
* ```./mvnw quarkus:dev -pl api-quarkus ``` : Lancement du projet `api-quarkus` en mode developpement
* ```./mvnw clean package  -pl api-quarkus ``` : Construction du projet `api-quarkus` en mode JVM
* ```./mvnw clean package -P native  -pl api-quarkus ``` : Construction du projet `api-quarkus` en mode Natif
