# Système de Quiz en Laravel

## Description du Projet
Le système de quiz est une application de quiz à choix multiples simple conçue pour permettre aux enseignants de tester leurs étudiants et d'évaluer leurs performances. Ce système comprend plusieurs fonctionnalités pour rendre le processus de quiz efficace et pratique.

### Fonctionnalités

1. **Limite de temps du quiz**
    - Le quiz a une limite de temps prédéfinie de 20 minutes. Une fois ce délai écoulé, la session de l'étudiant pour l'examen expirera automatiquement.
    (Il n'est pas encore disponible de choisir la durée du quiz .)

2. **Une seule tentative**
    - Chaque étudiant peut tenter le quiz une seule fois pour maintenir l'équité et prévenir la tricherie.

4. **Examen et communication de l'administrateur**
    - L'administrateur reçoit une notification par e-mail lorsqu'un étudiant termine un quiz. L'administrateur peut ensuite renvoyer un e-mail à l'étudiant avec sa note et son résultat (Accepté ou Rejeté).

5. **Accès privé**
    - Le système de quiz est privé, et tous les utilisateurs, y compris les administrateurs, doivent se connecter pour y accéder.

6. **Fonctionnalités des utilisateurs**
    - Les utilisateurs réguliers (étudiants) peuvent :
        - Se connecter
        - Passer un test
        - Répondre à des questions à choix multiples
        - Examiner un rapport de leurs réponses, y compris les bonnes réponses et leur note.

7. **Fonctionnalités de l'administrateur**
    - Les administrateurs peuvent :
        - Créer des quiz avec des questions à choix multiples
        - Recevoir des notifications par e-mail lorsque les étudiants terminent des quiz
        - Renvoyer des notifications par e-mail aux étudiants avec leurs notes et résultats.

### Questions du Quiz
- Les questions du quiz sont uniquement à choix multiples, chaque question ayant quatre choix et une seule réponse correcte.

## Utilisation
Pour configurer et utiliser le système de quiz, suivez ces étapes :

1. **Installation**
    - Clonez ce dépôt sur votre machine locale.
    - Installez les dépendances :
      ```bash
      composer install
      ```

2. **Configuration de la base de données, du courrier et de la file d'attente**
    - Configurez les paramètres de votre base de données dans le fichier `.env`.
    - Configurez les paramètres de votre courrier dans le fichier `.env`.
    - Convertissez `QUEUE_CONNECTION` de `sync` à `database` dans le fichier `.env`.

3. **Migration et alimentation de la base de données**
    - Exécutez les commandes suivantes pour configurer la base de données et l'alimenter avec des données initiales :
      ```bash
      php artisan migrate --seed
      ```

4. **Création de l'administrateur**
    - Pour créer un administrateur, utilisez la commande suivante :
      ```bash
      php artisan create:admin
      ```

5. **Exécution de l'application**
    - Lancez le serveur de développement :
      ```bash
      php artisan serve
      ```
    - Démarrez le travailleur de file d'attente :
      ```bash
      php artisan queue:work
      ```

6. **Accès à l'application**
    - Ouvrez votre navigateur web et accédez à `http://localhost:8000` pour accéder au système de quiz.

## Fonctionnalités Futures
    - Ajouter la possibilité de créer des quiz avec différents types de questions (par exemple, à choix multiples, vrai/faux, réponse courte, etc.).
    - Ajouter la possibilité de créer des quiz avec différentes limites de temps.
    - Ajouter la possibilité de créer des quiz avec plusieurs tentatives.
    - Ajouter une alerte conviviale à l'utilisateur.
    - Ajouter la connexion avec Google, Facebook et Twitter.

## Contribution
Les contributions sont les bienvenues ! Si vous avez des suggestions ou souhaitez signaler des problèmes, veuillez créer une demande GitHub ou soumettre une pull request.

## Licence
Ce projet est sous licence MIT - consultez le fichier [LICENSE](LICENSE) pour plus de détails.

## Contact
Pour toute question ou demande, veuillez contacter `Nader Mohammed` à l'adresse `Nader96x@gmail.com`.
