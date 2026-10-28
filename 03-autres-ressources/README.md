# Autres ressources

Ce dossier contient des ressources pour le cours _"Programmation serveur 3
(ProgServ3)"_.

## Utilisation de Classroom 50

[Classroom 50](https://github.com/foundation50/classroom50/wiki) est une
alternative à [GitHub Classroom](https://classroom.github.com/) qui permet de
gérer les dépôts de cours et les devoirs pour les étudiant.es.

Sa mise en place peut être réalisée en suivant les étapes suivantes :

1. Avoir un compte GitHub et un accès à
   [GitHub Education](https://education.github.com/).
2. Créer une organisation GitHub pour la classroom (par exemple,
   `heig-vd-progserv-classroom`).
   - Si un dépôt GitHub pour le cours existe déjà, je (Ludovic) préfère créer
     une nouvelle organisation pour l'espace classroom afin de séparer les
     dépôts de cours des dépôts de devoirs. En effet, les dépôts de code de
     chaque étudiant.e seront créés dans l'organisation classroom, et non dans
     l'organisation de cours, ce qui évite de "polluer" l'organisation de cours
     avec des dépôts privés d'étudiant.es.
3. Se connecter à [Classroom 50](https://classroom50.org) avec le compte GitHub.
   - Cela peut nécessiter de donner des autorisations à Classroom 50 pour
     accéder à l'organisation GitHub.
   - Si les modèles ("templates") de départ pour les devoirs sont stockés dans
     une autre organisation que celle de la classroom, il faudra également
     donner des autorisations à Classroom 50 pour accéder à cette organisation.
4. Dans Classroom 50, configurer une nouvelle organisation en utilisant
   l'organisation GitHub créée à l'étape 2.
   - Il faudra également mettre à niveau ("upgrade") l'organisation GitHub vers
     un plan payant (GitHub Team) pour permettre la création de dépôts privés
     pour chaque étudiant.e. En utilisant GitHub Education, l'organisation peut
     bénéficier d'un plan gratuit pour les dépôts privés.
   - Lancer l'assistant de configuration pour créer un espace classroom pour le
     cours.
5. Une fois l'organisation classroom configurée, accéder aux paramètres pour
   finaliser la configuration.
   - Cela permet de sécuriser l'organisation et de définir les paramètres de
     confidentialité pour les dépôts d'étudiant.es.
6. Créer une nouvelle "classroom" pour le cours, en définissant les détails du
   cours et les paramètres de devoirs.
   - L'organisation classroom peut être utilisée pour créer de nouvelles
     "classrooms" pour chaque cours/année académique, en utilisant des préfixes
     pour les noms de dépôts. Par exemple, pour le cours ProgServ3, on peut
     utiliser le nom "ProgServ3 2026-2027" avec le préfixe ("slug")
     `progserv3-2026-2027` associé.
   - Au sein d'une classroom, il est ensuite possible de créer des devoirs pour
     les étudiant.es, en définissant les paramètres de dépôt et les instructions
     pour chaque devoir.
7. Inviter les étudiant.es à rejoindre la classroom :
   - Dans les paramètres de la classroom, définir la liste de classe ("roster")
     avec les adresses e-mail des étudiant.es. En cliquant sur le bouton "Upload
     roster", il est possible de télécharger un modèle CSV ou d'importer un
     fichier CSV contenant les adresses e-mail des étudiant.es.
   - Lors de l'importation du roster, il est possible de définir les rôles de
     chaque personnes à importer (pratique pour définir un.e autre
     enseignant.e).
   - Chaque personne recevra un e-mail d'invitation pour rejoindre la classroom.
8. Créer un nouveau devoir, en définissant les paramètres de dépôt et les
   instructions pour les étudiant.es.
   - Un devoir est un dépôt GitHub qui sera créé pour chaque étudiant.e dans
     lequel il/elle pourra travailler.
   - Un devoir peut être utilisé pour un mini-projet, un exercice pratique ou
     une évaluation.
   - Par exemple, pour le mini-projet de ProgServ3, on peut créer un devoir avec
     les paramètres suivants :
     - Nom du devoir : "Mini-projet".
     - Préfixe de dépôt : `mini-projet`.
     - Description : "Le dépôt de code initial pour le mini-projet du cours
       ProgServ3."
     - Type de devoir : individuel (chaque étudiant.e aura son propre dépôt
       privé).
     - Modèle ("template") de départ : un dépôt GitHub contenant le code de base
       pour le mini-projet, avec les fichiers et dossiers nécessaires pour
       démarrer le développement, par exemple
       `heig-vd-progserv-course/heig-vd-progserv3-course-php-template`.
     - Dans les options avancées, il est possible de définir les droits sur le
       dépôt. Pour un mini-projet, je (Ludovic) recommande de définir les droits
       sur privé ("private") avec des droits d'administration. Ceci permettra à
       chaque étudiant.e de pouvoir transférer le dépôt sur son compte personnel
       dans le futur. Pour une évaluation, je laisserais uniquement les droits
       en écriture ("write"), ce qui les empêchera de pouvoir accéder aux
       paramètres du dépôt, de le transférer sur leur compte personnel ou encore
       changer la visibilité du dépôt.
     - Les autres options sont à configurer selon les besoins du cours et les
       préférences de l'enseignant.e.
   - Une fois le devoir créé, il est nécessaire de partager le lien du devoir
     avec les étudiant.es pour qu'ils/elles puissent le cloner et commencer à
     travailler dessus.
9. Les étudiant.es doivent accéder au lien du devoir pour accepter l'invitation
   et rejoindre la classroom.
   - Une fois qu'ils/elles ont accepté l'invitation, ils/elles peuvent accéder
     au dépôt du devoir et commencer à travailler dessus.
   - Chaque étudiant.e aura son propre dépôt privé pour le devoir, ce qui permet
     de travailler de manière indépendante et de soumettre les modifications via
     des pull requests.
   - Le dépôt privé suit la structure
     `<préfixe de l'organisation classroom>/<préfixe du devoir>-<nom d'utilisateur GitHub>`.
     Par exemple, pour le mini-projet, le dépôt privé d'un étudiant.e nommé.e
     `johndoe` serait accessible à l'adresse
     `heig-vd-progserv-classroom/progserv3-2026-2027-mini-projet-johndoe`.
10. Les étudiant.es peuvent ensuite cloner le dépôt du devoir sur leur machine
    locale et commencer à travailler dessus.
    - Chaque étudiant.e aura son propre dépôt privé pour le devoir, ce qui
      permet de travailler de manière indépendante et de soumettre les
      modifications via des pull requests.
