# PHP, Composer et Laravel - Mini-projet

L. Delafontaine, avec l'aide de
[GitHub Copilot](https://github.com/features/copilot).

Ce travail est sous licence [CC BY-SA 4.0][licence].

> [!TIP]
>
> Toutes les informations relatives à ce contenu sont décrites dans le
> [contenu principal](../README.md).

## Table des matières

- [Table des matières](#table-des-matières)
- [Objectifs](#objectifs)
- [Avertissements et alertes](#avertissements-et-alertes)
- [Mettre en place l'environnement de développement](#mettre-en-place-lenvironnement-de-développement)
  - [Installer et configurer votre éditeur de code](#installer-et-configurer-votre-éditeur-de-code)
  - [Installer et configurer Git et GitHub](#installer-et-configurer-git-et-github)
  - [Accéder au Classroom](#accéder-au-classroom)
  - [Cloner et ouvrir le projet localement](#cloner-et-ouvrir-le-projet-localement)
  - [Valider l'installation et la configuration de l'environnement de développement](#valider-linstallation-et-la-configuration-de-lenvironnement-de-développement)
- [Démarrer le mini-projet](#démarrer-le-mini-projet)
  - [Initialiser le projet Laravel](#initialiser-le-projet-laravel)
  - [Installer les dépendances PHP et JavaScript et finalisation de la configuration Laravel](#installer-les-dépendances-php-et-javascript-et-finalisation-de-la-configuration-laravel)
  - [Démarrer le serveur de développement Laravel](#démarrer-le-serveur-de-développement-laravel)
  - [Naviguer dans la structure du projet](#naviguer-dans-la-structure-du-projet)
  - [Effectuer des modifications simples](#effectuer-des-modifications-simples)
  - [Modifier une vue Laravel](#modifier-une-vue-laravel)
  - [Pousser les modifications sur GitHub](#pousser-les-modifications-sur-github)
  - [Commencer le développement depuis un dépôt GitHub](#commencer-le-développement-depuis-un-dépôt-github)
  - [Mettre à jour la documentation pour lancer le projet](#mettre-à-jour-la-documentation-pour-lancer-le-projet)
- [Conclusion](#conclusion)
- [Solution](#solution)
- [Aller plus loin](#aller-plus-loin)

## Objectifs

Bienvenue dans la première séance du mini-projet qui va vous accompagner durant
toute la durée du cours _"Programmation serveur 3 (ProgServ3)"_ !

Lors du cours
_"[Programmation serveur 1 (ProgServ1)](https://github.com/heig-vd-progserv-course/heig-vd-progserv1-course)"_,
vous avez appris les bases de PHP et de la programmation serveur à l'aide d'un
mini-projet pour créer un gestionnaire d'animaux de compagnie.

Lors du cours
_"[Programmation serveur 2 (ProgServ2)](https://github.com/heig-vd-progserv-course/heig-vd-progserv2-course)"_,
vous avez approfondi vos connaissances en programmation serveur à l'aide d'un
projet libre.

Dans ce cours _"Programmation serveur 3 (ProgServ3)"_, vous allez créer une
application web complète en utilisant le framework Laravel. Le mini-projet
reprendra les concepts étudiés en _"Programmation serveur 1 (ProgServ1)"_ et
_"Programmation serveur 2 (ProgServ2)"_, mais cette fois-ci en utilisant Laravel
pour structurer et simplifier le développement.

Le mini-projet du cours est un petit réseau social. Vous allez créer une
application web qui permettra aux personnes d'effectuer les actions suivantes
sur celle-ci :

- Se créer un compte sur la plateforme.
- Se connecter et se déconnecter.
- Modifier son profil utilisateur.
- Créer et partager des posts avec un titre et une description.
- Interagir avec les posts des autres personnes qui utilisent l'application
  (aimer un post).

Si le temps le permet, des fonctionnalités supplémentaires pourront être
ajoutées, comme la possibilité de rajouter une ou des images aux posts, de
commenter les posts ou de suivre d'autres utilisateur.trices.

L'objectif est de construire une application web complète pour remplir ces
fonctionnalités en utilisant Laravel.

Nous construirons cette application web ensemble durant la durée du cours en
plusieurs étapes. Dans cette séance, nous allons mettre en place l'environnement
de développement et initialiser le projet PHP pour le mini-projet.

De façon plus concise, à l'issue de cette séance, les personnes qui étudient
devraient avoir pu :

- Mettre en place un environnement de développement PHP pour Laravel.
- Initialiser un projet Laravel.
- Lancer le serveur de développement Laravel.
- Explorer la structure d'un projet Laravel.
- Partager le code source du projet sur GitHub.

## Avertissements et alertes

En lisant les contenus préparés pour les séances de mini-projet, vous trouverez
peut-être ce que l'on appelle des _"avertissements"_ ou des _"alertes"_.

Elles se présentent comme suit :

> [!NOTE]
>
> Hé ! Je suis une note ! Merci de m'avoir lue !

Elles sont là pour mettre en évidence des informations importantes dont vous
devez tenir compte.

Voici les différents types d'avertissements que vous pourriez trouver et leur
signification :

> [!NOTE]
>
> Met en évidence les informations que vous devriez prendre en compte.

> [!TIP]
>
> Informations facultatives pour vous aider à mieux réussir avec des conseils,
> des astuces, ou encore des suggestions.

> [!IMPORTANT]
>
> Informations cruciales nécessaires à la réussite des actions que vous devriez
> effectuer.

> [!WARNING]
>
> Contenu critique exigeant votre attention immédiate en raison des risques
> potentiels.

> [!CAUTION]
>
> Conséquences négatives potentielles d'une action que vous devriez éviter.

Nous pourrions vous rediriger vers de la documentation officielle ou des
ressources externes à suivre pour configurer votre environnement ou en savoir
plus sur un sujet spécifique.

Ces ressources externes sont là pour vous aider. Nous vous redirigeons vers
elles pour éviter de répéter ce qui est déjà bien maintenu et expliqué ailleurs.

Ces informations sont là pour vous aider à mieux comprendre et à réussir dans
votre apprentissage.

Ce que vous voyez et faites dans une séance actuelle peut être utilisé dans une
séance future.

C'est pourquoi il est important de suivre les étapes et de comprendre ce que
vous faites. Vous devez conserver le code que vous écrivez pour les séances
futures.

Cependant, si _quoi que ce soit_ n'est pas clair, ne fonctionne pas ou nécessite
une amélioration, n'hésitez pas à poser des questions ou nous le signaler.

C'est parti !

## Mettre en place l'environnement de développement

Laravel se reposant sur PHP, tout ce que vous avez appris dans les cours de
_"Programmation serveur 1 (ProgServ1)"_ et _"Programmation serveur 2
(ProgServ2)"_ reste valable.

Il est donc toujours nécessaire d'avoir un environnement de développement PHP
fonctionnel comportant, entre autres :

- Un serveur web (Apache, Nginx, ou le serveur de développement PHP intégré).
- Un interpréteur PHP (version 8.0 ou supérieure recommandée).
- Une base de données (MySQL, PostgreSQL, SQLite, etc.).

Heureusement pour nous, Laravel fournit un serveur de développement intégré qui
simplifie le processus de configuration de l'environnement de développement.

### Installer et configurer votre éditeur de code

Dans cette section, nous allons installer et configurer les outils nécessaires
pour développer avec Laravel.

Nous avons choisi d'utiliser Visual Studio Code comme éditeur de code pour ce
cours, mais vous êtes libre d'utiliser l'éditeur de votre choix.

Si vous n'avez pas encore installé Visual Studio Code, suivez les instructions
officielles pour l'installer sur votre système d'exploitation :
<https://code.visualstudio.com/docs/setup/setup-overview>.

[PHPStorm](https://www.jetbrains.com/phpstorm/) est une excellente alternative à
Visual Studio Code, mais il s'agit d'un logiciel payant. Au travers de la
HEIG-VD, vous avez accès à une licence gratuite pour tous les produits
JetBrains, que vous pouvez obtenir en suivant les instructions sur la page
suivante : <https://www.jetbrains.com/academy/student-pack/>.

### Installer et configurer Git et GitHub

Avant de continuer, assurez-vous que Git et GitHub sont correctement configurés
selon le contenu suivant :
[Git et GitHub](https://heig-vd-upinfo-course.github.io/heig-vd-upinfo-course/05-configurer-son-systeme-dexploitation-et-ses-applications/19-git-et-github/).

Assurez-vous d'avoir validé les points suivants :

- [x] Vous avez un compte GitHub.
- [x] Vous avez ajouté votre adresse e-mail académique à votre compte GitHub.
- [x] Vous avez configuré Git localement avec votre nom d'utilisateur et votre
      adresse e-mail principale de votre compte GitHub.
- [x] Vous avez ajouté votre clé SSH publique à votre compte GitHub.
- [x] Vous avez ajouté votre clé SSH privée à votre agent SSH local.

### Accéder au Classroom

Un "Classroom" est un espace de travail qui permet de gérer des dépôts GitHub
pour des cours.

Vous devriez avoir reçu un lien pour rejoindre le Classroom du cours sur votre
adresse e-mail académique. Ce lien vous permettra d'avoir accès à votre dépôt
GitHub privé pour le mini-projet et permettra aux enseignant.es de suivre votre
progression.

Il est nécessaire de rejoindre le Classroom pour accéder au dépôt du
mini-projet.

1. Acceptez l'invitation pour rejoindre le Classroom du cours en cliquant sur le
   lien que vous avez reçu par e-mail sur votre adresse e-mail académique.
2. Vous serez alors ajouté.e à l'organisation GitHub pour le classroom du cours,
   ce qui vous permettra d'accéder à votre dépôt GitHub privé pour le
   mini-projet.
3. Accédez à [Classroom 50](https://classroom50.org) et connectez-vous avec
   votre compte GitHub.
4. Accédez à la page du cours _"Programmation serveur 3 (ProgServ3)"_ puis aux
   devoirs ("View assignments").
5. Cliquez sur le bouton _"Accept this assignment"_ pour accepter le "devoir" du
   mini-projet.
6. Votre dépôt GitHub privé pour le mini-projet sera créé automatiquement pour
   vous. Vous devriez voir un message de confirmation indiquant que le dépôt a
   été créé avec succès et y accéder en cliquant sur le lien fourni. Il s'agira
   de votre espace de travail pour le mini-projet, où vous pourrez développer
   votre application web avec Laravel.

Vous devriez maintenant avoir accès à votre dépôt GitHub privé pour le
mini-projet sur une page similaire à celle-ci :

![GitHub Classroom - Mini-projet (1)](./images/github-classroom-mini-projet-01.png)

### Cloner et ouvrir le projet localement

Suivez les instructions du README du dépôt pour cloner le projet et l'ouvrir
dans Visual Studio Code dans le conteneur de développement.

### Valider l'installation et la configuration de l'environnement de développement

Une fois que vous avez cloné le projet et ouvert le conteneur de développement,
vous devriez valider que votre environnement de développement est correctement
configuré.

Pour cela, exécutez les commandes suivantes dans le terminal intégré de Visual
Studio Code :

```bash
# Vérifier la version de PHP
php --version

# Vérifier la version de Composer
composer --version

# Vérifier la version de npm
npm --version
```

Le résultat de ces commandes devrait afficher les versions installées de PHP,
Composer et npm, validant que les outils nécessaires pour le développement avec
Laravel sont correctement installés et configurés :

```text
$ php --version
PHP 8.5.11 (cli) (built: Oct  6 2026 01:23:10) (NTS)
Copyright (c) The PHP Group
Built by https://github.com/docker-library/php
Zend Engine v4.5.11, Copyright (c) Zend Technologies
    with Xdebug v3.5.3, Copyright (c) 2002-2026, by Derick Rethans
    with Zend OPcache v8.5.11, Copyright (c), by Zend Technologies

$ composer --version
Composer version 2.10.3 2026-08-27 13:34:23
PHP version 8.5.11 (/usr/local/bin/php)
Run the "diagnose" command to get more detailed diagnostics output.

$ npm --version
11.20.0
```

Validez également que votre conteneur de développement est correctement
configuré avec Git en exécutant la commande suivante :

```bash
# Vérifier la version de Git
git --version

# Vérifier que la clé SSH est correctement chargée dans l'agent SSH
ssh-add -l

# Tester la connexion SSH à GitHub
ssh -T git@github.com
```

Le résultat de ces commandes devrait afficher les versions installées de Git, la
liste des clés SSH chargées dans l'agent SSH et un message de bienvenue de
GitHub, validant que votre configuration Git et GitHub est correcte :

```text
$ git --version
git version 2.56.0

$ ssh-add -l
256 SHA256:naCCKCyb1yC41QaCHwlcy2KiHF6uYsphKSczwGbm/u0 ludovic.delafontaine@heig-vd.ch (ED25519)

$ ssh -T git@github.com
Hi ludelafo! You've successfully authenticated, but GitHub does not provide shell access.
```

## Démarrer le mini-projet

### Initialiser le projet Laravel

A présent que l'environnement de développement est prêt, nous allons initialiser
le mini-projet avec Laravel.

Ouvrez un terminal intégré dans Visual Studio Code (si ce n'est pas déjà fait)
en allant dans le menu _"Terminal"_ > _"New Terminal"_.

Ceci devrait automatiquement ouvrir l'emplacement du dossier racine de votre
projet dans le terminal intégré.

Comme notre dossier racine de votre projet contient déjà des fichiers de
configuration, nous allons créer le projet Laravel dans un dossier temporaire à
l'extérieur du dossier racine de votre projet, puis nous déplacerons les
fichiers nécessaires dans le dossier racine de votre projet.

> [!NOTE]
>
> Pourquoi faisons-nous cela ?
>
> Le modèle de base que nous vous avons fourni met à disposition différents
> fichiers de configuration et de documentation pour vous aider à démarrer le
> mini-projet.
>
> Si nous créons le projet Laravel directement dans le dossier racine de votre
> projet, un nouveau sous-dossier sera créé de la manière suivante (ici, le
> dossier de notre application Laravel s'appelle `example-app`) :
>
> ```text
> ./
> ├── .devcontainer/
> │   ├── devcontainer.json
> │   └── devcontainer-lock.json
> ├── example-app/
> │   ├── app/
> │   ├── bootstrap/
> │   ├── config/
> │   ├── database/
> │   ├── node_modules/
> │   ├── public/
> │   ├── resources/
> │   ├── routes/
> │   ├── storage/
> │   ├── tests/
> │   ├── vendor/
> │   ├── artisan*
> │   ├── composer.json
> │   ├── composer.lock
> │   ├── .editorconfig
> │   ├── .env
> │   ├── .env.example
> │   ├── .gitattributes
> │   ├── .gitignore
> │   ├── package.json
> │   ├── package-lock.json
> │   ├── phpunit.xml
> │   ├── README.md
> │   └── vite.config.js
> ├── .git/
> │   └── ...
> ├── .vscode/
> │   └── settings.json
> ├── compose.yaml
> ├── .gitignore
> └── README.md
> ```
>
> Nous remarquons que notre projet a maintenant plusieurs fichiers repétitifs,
> comme les fichiers `README.md` ou `.gitignore` (un à la racine du projet et
> l'autre dans le dossier `example-app`), ce qui peut créer de la confusion et
> des conflits lors du développement.
>
> Bien que cela ne pose pas de problème pour le fonctionnement de l'application
> Laravel, nous allons créer le projet Laravel dans un dossier temporaire puis
> déplacer les fichiers nécessaires dans le dossier racine de votre projet afin
> de garder une structure de projet propre et éviter les confusions.

Pour créer un nouveau projet Laravel, nous allons utiliser la commande
`composer create-project` qui permet de créer un nouveau projet Laravel avec
Composer.

```bash
# Crée un nouveau projet Laravel dans le dossier temporaire "/tmp/example-app"
composer create-project "laravel/laravel:^12.0" /tmp/example-app
```

> [!TIP]
>
> Il existe un utilitaire en ligne de commande appelé `laravel` qui permet de
> créer un nouveau projet Laravel avec la commande `laravel new`
> ([source](https://laravel.com/framework/docs/12.x/installation)).
>
> Cependant, cette commande installe automatiquement la dernière version de
> Laravel, sans pouvoir définir une version spécifique.
>
> Comme Laravel évolue continuellement, il est préférable d'utiliser la commande
> `composer create-project` pour créer un projet Laravel avec une version
> spécifique (ici, la version 12.x sur laquelle se base ce cours) afin d'éviter
> des problèmes de compatibilité avec les versions futures.
>
> Dans le futur, vous pourrez utiliser la commande `laravel new` pour créer un
> projet Laravel avec la dernière version disponible.

Cette commande va créer un nouveau projet Laravel contenant la structure de base
que nous allons explorer dans une prochaine section.

Déplaçons maintenant les fichiers nécessaires du projet Laravel vers le dossier
racine de votre projet.

```bash
# Déplace les fichiers nécessaires du projet Laravel vers le dossier racine de votre projet
cp -an /tmp/example-app/. /workspace/
```

Vous avez maintenant un projet Laravel fonctionnel dans le dossier racine de
votre projet avec la structure suivante :

```text
./
├── app/
│   ├── Http/
│   ├── Models/
│   └── Providers/
├── bootstrap/
│   ├── cache/
│   ├── app.php
│   └── providers.php
├── config/
│   ├── app.php
│   ├── auth.php
│   ├── cache.php
│   ├── database.php
│   ├── filesystems.php
│   ├── logging.php
│   ├── mail.php
│   ├── queue.php
│   ├── services.php
│   └── session.php
├── database/
│   ├── factories/
│   ├── migrations/
│   ├── seeders/
│   ├── database.sqlite
│   └── .gitignore
├── .devcontainer/
│   ├── devcontainer.json
│   └── devcontainer-lock.json
├── .git/
│   └── ...
├── public/
│   ├── favicon.ico
│   ├── .htaccess
│   ├── index.php
│   └── robots.txt
├── resources/
│   ├── css/
│   ├── js/
│   └── views/
├── routes/
│   ├── console.php
│   └── web.php
├── storage/
│   ├── app/
│   ├── framework/
│   └── logs/
├── tests/
│   ├── Feature/
│   ├── Unit/
│   └── TestCase.php
├── vendor/
│   ├── ...
│   └── autoload.php
├── .vscode/
│   └── settings.json
├── artisan*
├── composer.json
├── composer.lock
├── compose.yaml
├── .editorconfig
├── .env
├── .env.example
├── .gitattributes
├── .gitignore
├── package.json
├── phpunit.xml
├── README.md
└── vite.config.js
```

Vous pouvez supprimer le contenu du dossier temporaire `/tmp/example-app`
maintenant que nous avons déplacé les fichiers nécessaires vers le dossier
racine de votre projet.

```bash
# Supprime le contenu du dossier temporaire
rm -rf /tmp/example-app
```

### Installer les dépendances PHP et JavaScript et finalisation de la configuration Laravel

Installez les dépendances PHP et JavaScript nécessaires pour le projet Laravel
en exécutant les commandes suivantes :

```bash
# Installer les dépendances PHP avec Composer
composer install

# Installer les dépendances JavaScript avec npm
npm install

# Compiler les assets front-end avec Vite
npm run build
```

Finalement, modifiez le fichier `vite.config.js` pour que le serveur de
développement Vite écoute sur toutes les interfaces réseau, ce qui permettra
d'accéder à l'application Laravel depuis votre navigateur web:

```diff
diff --git a/vite.config.js b/vite.config.js
index 3c1c2a8..aad09dd 100644
--- a/vite.config.js
+++ b/vite.config.js
@@ -11,6 +11,11 @@ export default defineConfig({
         tailwindcss(),
     ],
     server: {
+        host: true,
+        origin: "http://localhost:5173",
+        hmr: {
+            host: "localhost",
+        },
         watch: {
             ignored: ["**/storage/framework/views/**"
],
         },
```

### Démarrer le serveur de développement Laravel

Laravel met à disposition un serveur de développement intégré qui permet de
lancer l'application web localement pour le développement et les tests.

Cela signifie qu'il n'est plus nécessaire d'avoir un serveur web comme Apache ou
Nginx installé sur votre machine pour exécuter l'application Laravel pour du
développement local : Laravel fournit son propre serveur de développement et
chaque changement que vous effectuez dans le code source de l'application sera
automatiquement pris en compte par le serveur de développement.

En production, il reste nécessaire d'utiliser un serveur web comme Apache ou
Nginx pour exécuter l'application Laravel. Nous y reviendrons à la fin du cours.

Exécutez la commande suivante pour démarrer le serveur de développement Laravel
:

```bash
composer run dev
```

Le serveur de développement Laravel devrait démarrer et être accessible à
l'adresse suivante : <http://localhost:8000>.

Ouvrez cette adresse dans votre navigateur web. Vous devriez voir la page
d'accueil par défaut de Laravel :

![Page d'accueil Laravel](./images/laravel-welcome-page.png)

Laravel est maintenant installé et fonctionne correctement !

### Naviguer dans la structure du projet

Un projet Laravel possède une structure de dossiers et de fichiers bien définie.
Voici un aperçu de la structure de base d'un projet Laravel fraîchement créé :

```text
./
├── app/
│   ├── Http/
│   ├── Models/
│   └── Providers/
├── bootstrap/
│   ├── cache/
│   ├── app.php
│   └── providers.php
├── config/
│   ├── app.php
│   ├── auth.php
│   ├── cache.php
│   ├── database.php
│   ├── filesystems.php
│   ├── logging.php
│   ├── mail.php
│   ├── queue.php
│   ├── services.php
│   └── session.php
├── database/
│   ├── factories/
│   ├── migrations/
│   ├── seeders/
│   └── database.sqlite
├── node_modules/
│   └── ...
├── public/
│   ├── build/
│   ├── favicon.ico
│   ├── hot
│   ├── index.php
│   └── robots.txt
├── resources/
│   ├── css/
│   ├── js/
│   └── views/
├── routes/
│   ├── console.php
│   └── web.php
├── storage/
│   └── ...
├── tests/
│   └── ...
├── vendor/
│   ├── ...
│   └── autoload.php
├── artisan*
├── composer.json
├── composer.lock
├── package.json
├── package-lock.json
├── phpunit.xml
├── README.md
└── vite.config.js
```

Bien que le nombre de fichiers et dossiers puisse sembler intimidant au premier
abord, il est important de comprendre que chaque dossier a un rôle spécifique
dans le fonctionnement de l'application Laravel.

Voici une brève description des dossiers et fichiers les plus importants :

- `app/` : Contient le code source principal de l'application, y compris les
  contrôleurs, les modèles, et les fournisseurs de services.
- `bootstrap/` : Contient les fichiers de démarrage de l'application.
- `config/` : Contient les fichiers de configuration de l'application.
- `database/` : Contient les fichiers liés à la base de données. Vous y
  retrouvez la base de données SQLite créée pour le projet.
- `public/` : Contient les fichiers accessibles publiquement, y compris le point
  d'entrée de l'application (`index.php`).
- `resources/` : Contient les ressources de l'application, telles que les
  fichiers CSS, JavaScript, et les vues Blade.
- `routes/` : Contient les fichiers de définition des routes de l'application.
- `storage/` : Contient les fichiers générés par l'application, tels que les
  logs et les fichiers de cache.
- `tests/` : Contient les tests automatisés de l'application.
- `vendor/` : Contient les dépendances installées via Composer. Le fichier
  `autoload.php` est particulièrement important car il permet le chargement
  automatique des classes PHP.
- `artisan` : Le script en ligne de commande de Laravel.
- `composer.json` : Le fichier de configuration de Composer pour gérer les
  dépendances PHP.
- `package.json` : Le fichier de configuration npm pour gérer les dépendances
  JavaScript.
- `README.md` : Le fichier de documentation du projet.

Nous prendrons le temps d'explorer cette structure de projet pour mieux
comprendre comment Laravel organise le code et les ressources tout au long du
cours.

### Effectuer des modifications simples

#### `routes/web.php` : le fichier d'entrée d'une application Laravel

Le fichier `routes/web.php` est le point d'entrée principal d'une application
Laravel.

C'est dans ce fichier que vous allez définir les "routes" de l'application web
Laravel. Il s'agit des différents points d'accès de l'application web, qui sont
associés à des actions spécifiques. Chaque route est définie par une URL et une
action à exécuter lorsque cette URL est visitée.

Nous y reviendrons plus en détails dans une future séance, mais pour le moment,
effectuons une modification simple pour valider que tout fonctionne
correctement.

Dans le fichier `routes/web.php`, ajoutez le code suivant :

```diff
diff --git a/routes/web.php b/routes/web.php
index 86a06c5..a9ab8bf 100644
--- a/routes/web.php
+++ b/routes/web.php
@@ -5,3 +5,7 @@
 Route::get('/', function () {
     return view('welcome');
 });
+
+Route::get('/hello-world', function () {
+    return 'Hello, World!';
+});
```

Sauvegardez le fichier après avoir effectué la modification.

Accédez à l'URL suivante dans votre navigateur web :
<http://localhost:8000/hello-world>. Vous devriez voir le texte "Hello, World!"
s'afficher dans votre navigateur web.

En définissant une nouvelle route dans le fichier `routes/web.php`, nous avons
pu créer un point d'accès supplémentaire à notre application Laravel.

En accédant à l'URL `/hello-world`, nous avons déclenché l'action associée à
cette route, qui est d'afficher le texte "Hello, World!" dans le navigateur web.

Nous reviendrons plus en détails sur la définition des routes et les actions
associées dans une future séance, mais rappelez-vous que le fichier
`routes/web.php` est le point d'entrée principal pour définir les routes de
votre application Laravel.

### Modifier une vue Laravel

Dans la première route définie dans le fichier `routes/web.php`, nous avons
indiqué que lorsque l'URL racine `/` est visitée, la vue `welcome` doit être
affichée.

A nouveau, nous y reviendrons plus en détails dans une future séance, mais pour
le moment, nous allons modifier cette vue pour valider que tout fonctionne
correctement.

Ouvrez le fichier `resources/views/welcome.blade.php` dans Visual Studio Code.

Modifiez le contenu de la balise `<h1>` pour qu'il affiche le texte suivant :

```html
<h1 class="mb-1 font-medium">Bienvenue dans le mini-projet ProgServ3 !</h1>
```

Enregistrez le fichier après avoir effectué la modification.

Votre navigateur web devrait automatiquement refléter la modification et
afficher le nouveau texte dans la page d'accueil de Laravel.

Essayez de changer le contenu de la balise `<p>` située sous le titre pour
valider que les modifications sont bien prises en compte avec, par exemple, le
texte suivant :

```html
<p class="mb-2 text-[#706f6c] dark:text-[#A1A09A]">
	C'est ici que commence votre nouvelle aventure avec Laravel.
</p>
```

Si tout fonctionne correctement, vous avez réussi à modifier une vue dans le
projet Laravel !

Nous étudierons plus en détail comment fonctionnent les vues avec Laravel dans
les prochaines séances. Pour le moment, il n'est pas nécessaire de revenir sur
cette modification.

### Pousser les modifications sur GitHub

Maintenant que les deux modifications ont été effectuées dans le projet Laravel,
nous allons les pousser sur le dépôt GitHub distant pour les sauvegarder et les
partager.

Commitez les modifications dans le dépôt Git local en exécutant les commandes
suivantes dans le terminal intégré de Visual Studio Code :

```bash
# Ajouter les fichiers modifiés au suivi de Git
git add routes/web.php resources/views/welcome.blade.php

# Créer un commit avec un message décrivant les modifications
git commit -m "Ajout d'une route /hello-world et modification de la vue welcome"
```

Poussez les modifications sur le dépôt GitHub distant en exécutant la commande
suivante :

```bash
# Pousser les modifications sur le dépôt GitHub distant
git push origin main
```

Validez que les nouveaux changements ont bien été poussés sur le dépôt GitHub en
accédant à votre dépôt GitHub privé pour le mini-projet. Vous devriez voir les
deux fichiers modifiés avec le message de commit correspondant.

Nous utiliserons Git et GitHub tout au long du mini-projet pour gérer le code
source et suivre les modifications.

### Commencer le développement depuis un dépôt GitHub

Maintenant que le code source du mini-projet est disponible sur GitHub, vous
pouvez cloner le dépôt sur n'importe quelle machine pour continuer le
développement.

Pour simuler cela, nous allons cloner le projet dans un nouveau dossier et le
configurer pour le développement.

Cela sera particulièrement utile dans le futur si vous souhaitez travailler sur
le projet depuis une autre machine, si vous souhaitez simplement repartir d'une
copie fraîche du projet ou encore si vous travaillez en équipe sur un projet
collaboratif.

#### Cloner votre dépôt GitHub du mini-projet

Dans GitHub, récupérez l'URL SSH du dépôt GitHub privé pour **votre**
mini-projet en cliquant sur le bouton _"Code"_ et en sélectionnant l'option
_"SSH"_, comme illustré ci-dessous :

> [!NOTE]
>
> L'illustration ci-dessous est un exemple et ne correspond pas à votre dépôt
> GitHub. Assurez-vous de copier l'URL SSH de **votre** dépôt GitHub privé pour
> le mini-projet et non celui de l'illustration qui correspond à la solution du
> mini-projet à la fin de chaque séance.

![GitHub Classroom - Mini-projet (2)](./images/github-classroom-mini-projet-02.png)

Une fois l'URL SSH copiée, retournez dans le terminal intégré de Visual Studio
Code.

> [!NOTE]
>
> L'URL SSH est recommandée pour cloner le dépôt car elle permet d'utiliser une
> authentification sécurisée avec des clés SSH, ce qui est plus pratique que
> d'utiliser l'URL HTTPS qui nécessite de saisir votre nom d'utilisateur et mot
> de passe à chaque fois que vous poussez des modifications vers GitHub.

Clonez le dépôt GitHub du mini-projet en exécutant la commande suivante :

> [!NOTE]
>
> Nous allons cloner le dépôt dans le projet courant pour simuler le fait de
> cloner le projet depuis GitHub sur une nouvelle machine. Cela permettra de
> valider que le projet fonctionne correctement et que toutes les dépendances
> sont installées correctement. A la fin de ces étapes, nous supprimerons le
> projet cloné pour éviter toute confusion avec le projet initialement créé.

```bash
git clone <url-ssh-du-depot-github>
```

Remplacez `<url-ssh-du-depot-github>` par l'URL SSH que vous avez copiée
précédemment.

Cette commande clone le dépôt GitHub dans un nouveau dossier nommé
`progserv3-2026-2027-mini-projet-<github-username>`.

Vous devriez retrouver un nouveau dossier nommé
`progserv3-2026-2027-mini-projet-<github-username>` contenant le code source du
mini-projet dans votre système de fichiers.

> [!NOTE]
>
> Vous aurez donc deux projets Laravel sur votre machine. C'est normal. Cela
> permet de simuler le fait de cloner le projet depuis GitHub sur une nouvelle
> machine. Plus tard dans ce contenu, vous serez invité.e à supprimer un des
> deux projets pour éviter toute confusion.

#### Installer les dépendances

Vous remarquerez peut-être que le code source du projet Laravel diffère
légèrement de celui que vous aviez initialement créé. Cela est dû au fait que
Git ignore certains fichiers et dossiers par défaut, comme le dossiers
`node_modules/`/`vendor/` contenant les dépendances installées via npm/Composer
(respectivement), ainsi que le fichier `.env` contenant les variables
d'environnement spécifiques à chaque machine.

Lorsque vous clonez un dépôt Git, vous devez réinstaller les dépendances et
configurer les variables d'environnement pour que le projet fonctionne
correctement.

Pour cela, il est nécessaire d'installer les dépendances PHP avec Composer et
les dépendances JavaScript avec npm.

Naviguez dans l'emplacement du dossier précédemment cloné
`progserv3-2026-2027-mini-projet-<github-username>` :

```bash
# Naviguer dans le dossier cloné du projet Laravel
cd progserv3-2026-2027-mini-projet-<github-username>
```

Exécuter les commandes suivantes pour installer toutes les dépendances
nécessaires au projet Laravel:

```bash
# Installer les dépendances PHP avec Composer
composer install

# Installer les dépendances JavaScript avec npm
npm install

# Compiler les assets front-end avec Vite
npm run build
```

Les dépendances JavaScript et PHP devraient maintenant être installées
correctement et les dossiers `node_modules/` et `vendor/` devraient être
présents dans le dossier du projet.

#### Configurer les variables d'environnement

Une fois les dépendances installées, copiez le fichier `.env.example` pour créer
le fichier `.env` en exécutant la commande suivante :

```bash
cp .env.example .env
```

Ouvrez le fichier `.env` dans Visual Studio Code. Ce fichier contient les
variables d'environnement spécifiques à votre machine.

Ce fichier ne doit jamais être partagé publiquement car il peut contenir des
informations sensibles comme des mots de passe ou des clés d'API.

> [!CAUTION]
>
> Ce fichier `.env` ne doit jamais être partagé publiquement car il peut
> contenir des informations sensibles comme des mots de passe ou des clés d'API.
> Vous devez toujours garder ce fichier privé et sécurisé.

C'est la raison pour laquelle il est ignoré par Git via le fichier `.gitignore`
et qu'il est nécessaire de le créer manuellement à partir du fichier
`.env.example`. Une fois le fichier d'exemple copié, vous pouvez modifier les
variables d'environnement selon vos besoins.

Générez une clé d'application Laravel en exécutant la commande suivante dans le
terminal intégré :

```bash
php artisan key:generate
```

Cette commande génère une clé unique pour l'application Laravel et la met à jour
dans le fichier `.env` dans la variable `APP_KEY`.

Cette clé est utilisée par Laravel pour sécuriser les sessions et autres données
sensibles. La documentation officielle de Laravel explique plus en détail le
rôle de cette clé : <https://laravel.com/docs/12.x/encryption#configuration>.

Nous reviendrons sur ces notions plus tard dans le cours mais pour le moment, il
suffit de savoir qu'il est nécessaire d'effectuer ces étapes pour que
l'application Laravel fonctionne correctement.

#### Créer la base de données SQLite

Finalement, il est nécessaire de créer la base de données SQLite pour le projet
avec la commande suivante :

```bash
php artisan migrate
```

Cette commande crée automatiquement pour nous la base de données et ses tables
associées.

Un menu interactif vous demande de choisir certaines options. Choisissez les
options suivantes à l'aide des flèches du clavier et appuyez sur la touche
_Entrée_ pour valider vos choix :

```text
   WARN  The SQLite database configured for this application does not exist: database/database.sqlite.

 ┌ Would you like to create it? ────────────────────────────────┐
 │ ● Yes / ○ No                                                 │
 └──────────────────────────────────────────────────────────────┘
```

Différentes migrations devraient s'exécuter et créer les tables nécessaires dans
la base de données SQLite :

```text

   INFO  Preparing database.

  Creating migration table ......................... 7.46ms DONE

   INFO  Running migrations.

  0001_01_01_000000_create_users_table ............. 17.87ms DONE
  0001_01_01_000001_create_cache_table ............. 11.70ms DONE
  0001_01_01_000002_create_jobs_table .............. 15.33ms DONE
```

Nous reviendrons sur ces notions plus tard dans le cours mais pour le moment, il
suffit de savoir qu'il est nécessaire d'effectuer ces étapes pour que
l'application Laravel fonctionne correctement et crée la base de données.

#### Vérifier que tout fonctionne correctement

Démarrez le serveur de développement Laravel en exécutant la commande suivante
dans le terminal intégré :

```bash
composer run dev
```

Ouvrez l'adresse <http://localhost:8000> dans votre navigateur web. Vous

Vous devriez retrouver le même résultat que précédemment, avec la page d'accueil
de Laravel affichant le texte modifié.

Bravo ! Vous avez réussi à cloner le dépôt GitHub du mini-projet, installer les
dépendances, configurer les variables d'environnement, et créer la base de
données.

N'importe utilisant Git et GitHub peut désormais cloner le projet et le
configurer pour le développement en suivant les mêmes étapes.

#### Supprimer le projet cloné

Maintenant que nous avons validé que le projet cloné fonctionne correctement,
nous allons supprimer le projet cloné pour éviter toute confusion avec le projet
initialement créé.

```bash
# Naviguer dans le dossier parent du projet cloné
cd ..

# Supprimer le projet cloné
rm -rf progserv3-2026-2027-mini-projet-<github-username>
```

Vous devriez maintenant retrouver uniquement le projet initialement créé dans
votre espace de travail pour le mini-projet.

### Mettre à jour la documentation pour lancer le projet

Afin de garder une trace des étapes nécessaires pour cloner et configurer le
projet Laravel, nous allons mettre à jour le fichier `README.md` du dépôt GitHub
avec les instructions que nous venons de suivre.

Pour cela, nous allons utiliser diverses fonctionnalité de Git et GitHub pour
gérer cette tâche de développement.

#### Créer une issue GitHub pour cette tâche

Afin de prendre en main un workflow Git et GitHub adapté au développement
professionnel, nous allons commencer par créer une _issue_ GitHub dans le dépôt
du mini-projet.

Bien que son nom puisse prêter à confusion, une issue peut aussi être utilisée
pour décrire une nouvelle fonctionnalité à implémenter ou encore une tâche à
réaliser :

1. Accédez à votre dépôt GitHub privé pour le mini-projet.
2. Cliquez sur l'onglet _"Issues"_.
3. Cliquez sur le bouton _"New issue"_.
4. Donnez le titre suivant à l'issue : _"Ajouter les instructions de
   développement"_. Nous vous recommandons de toujours commencer le titre d'une
   issue par un verbe d'action à l'infinitif. Cela permet de décrire
   explicitement ce qui doit être fait.
5. Une description peut être ajoutée pour donner plus de contexte, mais ce n'est
   pas obligatoire ici car l'issue est assez explicite.
6. Cliquez sur le bouton _"Submit new issue"_ pour créer l'issue.

Ceci crée une nouvelle issue dans le dépôt GitHub du mini-projet. Elle permettra
de suivre l'avancement de cette tâche de développement.

Pensez aux issues comme à des tickets de travail. Utilisez-les pour suivre les
tâches, les fonctionnalités, les bugs, et vous vider la tête pour ne pas avoir à
tout retenir.

#### Créer une branche Git depuis l'issue

Une branche permet de travailler sur une fonctionnalité ou une correction de bug
sans affecter le code principal du projet.

GitHub permet de créer une branche directement depuis une issue dans le menu à
droite de l'issue :

1. Dans l'issue que vous venez de créer, cliquez sur le bouton _"Create
   branch"_.

   <details>
   <summary>Cliquer ici pour voir une capture d'écran illustrant l'étape</summary>

   ![GitHub Classroom - Mini-projet (3)](./images/github-classroom-mini-projet-03.png)

   </details>

2. Une modal s'ouvre pour confirmer la création de la branche. Laissez les
   options par défaut et cliquez sur le bouton _"Create branch"_ pour confirmer.
   Ceci crée automatiquement une nouvelle branche nommée comme le titre de
   l'issue. Cette branche est créée à partir de la branche `main`.

   <details>
   <summary>Cliquer ici pour voir une capture d'écran illustrant l'étape</summary>

   ![GitHub Classroom - Mini-projet (4)](./images/github-classroom-mini-projet-04.png)

   </details>

3. Une nouvelle modal s'ouvre pour vous proposer les commandes Git à exécuter
   pour basculer sur la nouvelle branche. Copiez les commandes proposées pour
   les utiliser dans le terminal intégré de Visual Studio Code.

   <details>
   <summary>Cliquer ici pour voir une capture d'écran illustrant l'étape</summary>

   ![GitHub Classroom - Mini-projet (5)](./images/github-classroom-mini-projet-05.png)

   </details>

4. Retournez dans le terminal intégré de Visual Studio Code.
5. Exécutez les commandes copiées précédemment pour basculer sur la nouvelle
   branche :

   ```bash
   git fetch origin
   git checkout 1-ajouter-les-instructions-de-développement
   ```

   La première commande récupère les dernières modifications du dépôt distant.
   La seconde commande crée une nouvelle branche locale nommée
   `1-ajouter-les-instructions-de-développement` et bascule dessus. La branche
   locale est liée à la branche distante du même nom.

6. Vérifiez que vous êtes bien sur la nouvelle branche en exécutant la commande
   suivante :

   ```bash
   git branch
   ```

   Le résultat devrait ressembler à ceci :

   ```text
   * 1-ajouter-les-instructions-de-développement
     main
   ```

   L'étoile (`*`) indique la branche courante. Vous êtes maintenant prêt.e à
   travailler sur cette branche.

#### Mettre à jour le fichier README.md

Mettons à jour le fichier `README.md` avec les instructions pour cloner et
configurer le projet Laravel.

Ce README contient actuellement une description générique du projet Laravel.
Nous allons remplacer ce contenu par les instructions que nous avons suivies
pour cloner et configurer le projet.

Cela permettra à toute personne qui clone le dépôt de savoir comment configurer
correctement le projet pour le développement (vous y compris dans le futur).

Ouvrez le fichier `README.md` dans Visual Studio Code.

Remplacez le contenu actuel du fichier par les instructions suivantes :

> [!NOTE]
>
> Vous êtes évidemment libre de reformuler ces instructions comme vous le
> souhaitez. L'important est que les étapes nécessaires pour cloner et
> configurer le projet soient clairement expliquées.
>
> Cela permettra à toute personne qui clone le dépôt de savoir comment
> configurer correctement le projet pour le développement (vous y compris dans
> le futur).

````markdown
# HEIG-VD ProgServ3 Course PHP Template

Ce modèle de projet est conçu pour les étudiant.es du cours
[_"Programmation Serveur 3 (ProgServ3)"_](https://github.com/heig-vd-progserv-course/heig-vd-progserv3-course)
à la [HEIG-VD](https://heig-vd.ch).

Il fournit une structure de base pour les projets PHP avec les éléments suivants
:

- Un interpréteur PHP 8.5 avec les extensions nécessaires pour le développement
  web et la connexion à une base de données SQLite.
- Des configurations recommandées pour l'éditeur de code
  [Visual Studio Code](https://code.visualstudio.com/), y compris des extensions
  utiles pour le développement PHP avec Laravel
  ([PHP Intelephense](https://marketplace.visualstudio.com/items?itemName=bmewburn.vscode-intelephense-client),
  [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode),
  [SQLite Viewer](https://marketplace.visualstudio.com/items?itemName=qwtel.sqlite-viewer),
  [Laravel](https://marketplace.visualstudio.com/items?itemName=laravel.vscode-laravel)
  et
  [Laravel Pint](https://marketplace.visualstudio.com/items?itemName=open-southeners.laravel-pint)).

Tous ses éléments sont configurés pour fonctionner avec
[Docker Compose](https://docs.docker.com/compose/), ce qui permet de créer un
environnement de développement isolé et reproductible.

N'hésitez pas à personnaliser ce modèle et ce document pour ajouter des
instructions spécifiques à votre projet ou des détails supplémentaires sur la
configuration et l'utilisation du projet.

## Utiliser ce modèle pour votre projet

1. Cliquez sur le bouton "Use this template" (Utiliser ce modèle) sur la page
   GitHub de ce dépôt.
2. Donnez un nom à votre nouveau dépôt et configurez les options selon vos
   préférences.
3. Invitez les membres de votre équipe à collaborer sur le projet en leur
   donnant accès au dépôt (si applicable).
4. Chaque membre de l'équipe doit cloner le nouveau dépôt sur sa machine locale
   pour commencer à travailler sur le projet (si applicable).
5. Utilisez le workflow GitHub étudié en cours pour gérer les branches, les
   commits et les pull requests afin de travailler efficacement sur le projet.

## Structure du projet

- `.devcontainer/`: Contient la configuration pour le développement dans un
  conteneur Debian (Trixie) avec Visual Studio Code.
- `.vscode/`: Contient les paramètres recommandés pour Visual Studio Code.
- `.gitignore`: Fichier de configuration pour Git, spécifiant les fichiers et
  dossiers à ignorer.
- `README.md`: Ce fichier de documentation.

## Ouvrir le projet localement

> [!NOTE]
>
> Il est important d'ouvrir le dossier du projet directement et non un dossier
> parent.
>
> Pensez à bien ouvrir le dossier du projet lui-même (celui qui contient ce
> fichier README.md) et non un dossier parent. Ouvrir un dossier parent peut
> entraîner des problèmes de configuration et de fonctionnement de Visual Studio
> Code.

1. Clonez ce dépôt sur votre machine locale.
2. Ouvrez ce dossier dans Visual Studio Code.

## Ouvrir le projet dans un conteneur de développement

Vous devez avoir l'extension
[Dev Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)
installée dans Visual Studio Code pour pouvoir ouvrir le projet dans un
conteneur Docker.

Une fois le projet ouvert dans Visual Studio Code, vous devriez voir une
notification vous proposant d'ouvrir le projet dans un conteneur de
développement. Cette notification peut apparaître sous forme de bannière en bas
à droite de l'éditeur ou dans la barre d'état en bas à gauche de la fenêtre.

Acceptez cette proposition pour bénéficier d'un environnement de développement
préconfiguré.

Si aucune notification n'apparaît, vous pouvez ouvrir manuellement le conteneur
en utilisant la commande _"Dev Containers: Reopen in Container"_ dans la palette
de commandes (<kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>P</kbd> sur Windows/Linux ou
<kbd>Cmd</kbd>+<kbd>Shift</kbd>+<kbd>P</kbd> sur macOS).

## Développement local

Pour développer et tester le mini-projet en local, voici les étapes à suivre
dans un terminal intégré de Visual Studio Code :

1. Installer les dépendances avec npm et Composer :

   ```bash
   # Installer les dépendances PHP avec Composer
   composer install

   # Installer les dépendances JavaScript avec npm
   npm install

   # Compiler les assets front-end avec Vite
   npm run build
   ```

2. Copier le fichier `.env.example` en `.env` et configurer les variables
   d'environnement.
3. Générer la clé d'application Laravel :

   ```bash
   php artisan key:generate
   ```

4. Créer la base de données et exécuter les migrations :

   ```bash
   php artisan migrate
   ```

5. Démarrer le serveur de développement Laravel :

   ```bash
   composer run dev
   ```

L'application sera accessible à l'adresse <http://localhost:8000>.

## Visualiser les e-mails envoyés par votre application PHP

Le serveur SMTP Mailpit est inclus dans la configuration Docker Compose pour
vous permettre de tester l'envoi d'e-mails depuis votre application PHP.

Pour accéder à l'interface web de Mailpit, lancez le conteneur Docker à l'aide
de la commande `docker compose up`, ouvrez votre navigateur et rendez-vous à
l'adresse suivante : <http://localhost:8025>.

Vous y verrez la liste des e-mails envoyés par votre application PHP, ainsi que
leur contenu et les détails de l'envoi.

Si vous fermez/redémarrez Mailpit, les e-mails précédemment envoyés seront
perdus, car ils ne sont pas stockés de manière persistante.

Pour arrêter le serveur Mailpit, vous pouvez utiliser le raccourci clavier
<kbd>Ctrl</kbd>+<kbd>C</kbd> dans le terminal où la commande `docker compose up`
a été exécutée, ou exécuter la commande `docker compose down` dans un terminal
intégré de Visual Studio Code.

Lorsque vous fermez Visual Studio Code, les conteneurs Docker seront
automatiquement arrêtés. Dès que vous rouvrez Visual Studio Code et que vous
exécutez à nouveau la commande `docker compose up`, les services Docker seront
redémarrés.
````

Sauvez le fichier après avoir effectué la modification.

#### Commiter et pousser les modifications

Une fois les modifications apportées au fichier `README.md`, il est temps de
commiter et pousser ces modifications vers le dépôt GitHub.

Dans le terminal intégré de Visual Studio Code, exécutez les commandes suivantes
pour ajouter le fichier modifié au suivi de Git, créer un commit, et pousser les
modifications vers le dépôt distant :

```bash
git add README.md

git commit -m "Ajouter les instructions de développement"

git push
```

Vous pouvez toujours vérifier le détail de votre dépôt Git avec la commande
suivante :

```bash
git status
```

#### Créer une pull request GitHub

Dans la terminologie GitHub, une pull request (PR) est une demande de fusion de
modifications d'une branche vers une autre branche. Dans notre cas, nous allons
créer une PR pour fusionner la branche
`1-ajouter-les-instructions-de-développement` dans la branche `main`.

GitHub propose une interface conviviale pour visualiser et gérer les pull
requests.

Lorsque vous avez poussé vos modifications, GitHub affiche généralement une
notification proposant de créer une pull request comme suit :

![GitHub Classroom - Mini-projet (6)](./images/github-classroom-mini-projet-06.png)

Vous pouvez également créer une pull request manuellement en suivant ces étapes
:

1. Accédez à votre dépôt GitHub privé pour le mini-projet.
2. Cliquez sur l'onglet _"Pull requests"_.
3. Cliquez sur le bouton _"New pull request"_.
4. Sélectionnez la branche source (_compare_)
   `1-ajouter-les-instructions-de-développement` et la branche de destination
   `main` (_base_).

   <details>
   <summary>Cliquer ici pour voir une capture d'écran illustrant l'étape</summary>

   ![GitHub Classroom - Mini-projet (7)](./images/github-classroom-mini-projet-07.png)

   </details>

5. Cliquez sur le bouton _"Create pull request"_.
6. Donnez un titre à la pull request. Par défaut, elle prend le message du
   dernier commit, qui peut ne pas représenter la totalité des modifications
   apportées. Je (Ludovic) recommande d'utiliser le titre de l'issue associée
   créée précédemment : _"Ajouter les instructions de développement"_.
7. Ajoutez une description si nécessaire. Ici, comme le titre de la pull request
   est explicite, ce n'est pas obligatoire.
8. Cliquez sur le bouton _"Create pull request"_ pour créer la pull request.

La pull request est maintenant créée et visible dans l'onglet _"Pull requests"_
du dépôt GitHub :

![GitHub Classroom - Mini-projet (8)](./images/github-classroom-mini-projet-08.png)

> [!NOTE]
>
> Vous pouvez ignorer le message d'avertissement concernant les caractères
> cachés (_The head ref may contain hidden characters:
> `"1-ajouter-les-instructions-de-d\u00E9veloppement"`_) si vous le voyez. Cela
> est dû aux caractères accentués dans le nom de la branche et n'affecte pas le
> fonctionnement de la pull request.

#### Valider la pull request

La très grande force des pull requests réside dans le fait qu'elles permettent
de revoir les modifications avant de les fusionner dans la branche principale du
projet.

Pour cela, rendez-vous dans l'onglet _"Files changed"_ de la pull request :

![GitHub Classroom - Mini-projet (9)](./images/github-classroom-mini-projet-09.png)

Vous pouvez y voir toutes les modifications apportées dans la branche source par
rapport à la branche de destination, y ajouter des commentaires, et même laisser
des suggestions de modifications si nécessaire.

Cela vous permettra de valider que les modifications sont correctes avant de les
fusionner.

Si des erreurs se sont glissées dans les modifications, vous pouvez toujours
retourner dans votre environnement de développement, corriger les erreurs, et
pousser les modifications vers la branche source. La pull request sera
automatiquement mise à jour avec les nouvelles modifications.

Itérez sur ce processus jusqu'à ce que vous soyez satisfait.e des modifications.

#### Faire valider la pull request

Une fois que vous êtes satisfait.e des modifications, il est temps de faire
valider la pull request envers quelqu'un d'autre.

Dans un projet professionnel, il est courant de demander à un.e collègue de
revoir et valider les modifications avant de les fusionner dans la branche
principale.

Cela permet de s'assurer que le code est de qualité et respecte les standards du
projet. De plus, cela permet de partager la connaissance du code entre les
membres de l'équipe.

Pour faire valider la pull request, vous pouvez retourner dans l'onglet
_"Conversation"_ et ajouter un.e relecteur.trice en cliquant sur le bouton
_"Reviewers"_ dans le menu à droite de la pull request.

La personne mise en relecteur.trice pourra ainsi revoir les modifications,
laisser des commentaires si nécessaire, et approuver la pull request si tout est
correct.

Comme il s'agit de votre propre dépôt, vous pouvez également fusionner la pull
request vous-même une fois que vous êtes satisfait.e des modifications.

#### Fusionner la pull request

Une fois la pull request validée par vos soins (et optionnellement par Ludovic
dans le contexte de ce cours), il est temps de fusionner les modifications dans
la branche principale `main`.

Pour cela, cliquez sur le bouton vert _"Merge pull request"_ dans l'onglet
_"Conversation"_ de la pull request.

La fusion des modifications est maintenant effectuée et les modifications sont
intégrées dans la branche `main`.

Vous pouvez maintenant supprimer la branche source de la pull request en
cliquant sur le bouton _"Delete branch"_, car elle n'est plus nécessaire.

Félicitations ! Vous avez réussi à fusionner un changement dans la branche
principale du projet en utilisant une pull request.

![GitHub Classroom - Mini-projet (10)](./images/github-classroom-mini-projet-10.png)

#### Valider que l'issue a bien été fermée

Une fois la pull request fusionnée, l'issue associée est automatiquement fermée
par GitHub.

Vous pouvez vérifier cela en retournant dans l'onglet _"Issues"_ du dépôt
GitHub.

Vous devriez voir que l'issue _"Ajouter les instructions de développement"_ est
marquée comme fermée. Si

#### Récupérer les modifications fusionnées localement

Après avoir fusionné la pull request sur GitHub, il est important de récupérer
les modifications fusionnées dans votre dépôt Git local.

Pour cela, retournez dans le terminal intégré de Visual Studio Code et exécutez
la commande suivante pour basculer sur la branche `main` :

```bash
git checkout main
```

Ensuite, exécutez la commande suivante pour récupérer les dernières
modifications de la branche `main` depuis le dépôt distant :

```bash
git pull
```

Cette commande met à jour votre branche `main` locale avec les modifications
fusionnées depuis GitHub.

Normalement, il ne devrait pas y avoir de conflits, car vous êtes seul.e à
travailler sur ce projet. Cependant, dans un contexte professionnel avec
plusieurs développeur.se.s, des conflits peuvent survenir si plusieurs personnes
modifient le même fichier en même temps.

Résolvez les conflits si nécessaire, puis vous serez prêt.e à continuer le
développement.

#### Recommencer la boucle de développement

Pour chacune des prochaines tâches de développement, il est recommandé de suivre
le même workflow Git et GitHub en créant une issue, une branche, une pull
request, et en faisant valider les modifications avant de les fusionner.

Cela permet de garder un historique clair des modifications apportées au projet
et de s'assurer que le code est de qualité.

Il existe de nombreuses manières de gérer un workflow Git et GitHub. Celui-ci
est simple et efficace pour un projet de cette taille et vous prépare à des
environnements de développement professionnels.

## Conclusion

Félicitations ! Vous avez mis en place votre environnement de développement et
initialisé votre projet Laravel pour le mini-projet.

De plus, vous avez appris à utiliser Git et GitHub pour gérer le code source et
suivre les modifications de manière professionnelle. Il s'agit d'une compétence
essentielle pour toute personne qui programme.

Vous êtes maintenant prêt.e à commencer à développer votre propre réseau social
en utilisant Laravel.

## Solution

La solution du mini-projet est accessible dans un dépôt GitHub dédié à l'adresse
suivante :
<https://github.com/heig-vd-progserv-course/heig-vd-progserv3-course-mini-project-solution/tree/mini-projet-1>.

> [!NOTE]
>
> La solution est fournie à titre indicatif uniquement. Il est fortement
> recommandé de développer votre propre version du mini-projet avant de
> consulter la solution.
>
> De plus, cette solution référence un commit spécifique. Des modifications
> peuvent avoir été apportées au dépôt depuis ce commit.
>
> Pour accéder à la version exacte de la solution correspondant à ce commit/tag,
> vous pouvez cloner le dépôt et utiliser la commande Git suivante pour basculer
> sur le commit/tag spécifique :
>
> ```bash
> git checkout <commit-hash> # ou git checkout <tag>
> ```
>
> Remplacez `<commit-hash>` ou `<tag>` par l'identifiant du commit ou du tag
> correspondant à la solution.

## Aller plus loin

> [!TIP]
>
> Cette section est optionnelle.
>
> Vous pouvez y revenir si vous avez du temps ou si vous souhaitez approfondir
> vos connaissances après avoir terminé les exercices et le mini-projet.

- Seriez-vous capable de protéger votre branche `main` pour éviter de pousser
  directement des modifications sans passer par une pull request ? Référez-vous
  à la documentation officielle de GitHub pour les règles de protection de
  branche :
  <https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches/about-protected-branches>
  et
  <https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/about-rulesets>.
- Seriez-vous capable de configurer GitHub pour supprimer automatiquement les
  branches source des pull requests une fois qu'elles sont fusionnées ?
  Référez-vous à la documentation officielle de GitHub pour la suppression
  automatique des branches :
  <https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/configuring-pull-request-merges/managing-the-automatic-deletion-of-branches>.

<!-- URLs -->

[licence]:
	https://github.com/heig-vd-progserv-course/heig-vd-progserv3-course/blob/main/LICENSE.md
