Poker API est une API RESTful développée dans le cadre d’un cours de qualité logiciel et tests. Elle permet la gestion de parties de poker en ligne : création de tables, gestion des joueurs, distribution des cartes, logique du jeu, etc.


*genèse du projet*
À l’origine, ce projet a été conçu comme une API RESTful développée dans le cadre d’un cours dédié à la création d’API. Le développement initial de l’API a été réalisé par Lallie Chappon et Antoine Cormier, avec pour objectif principal de modéliser et gérer les mécaniques d’un jeu de poker (tables, joueurs, cartes, tours de jeu, etc.).

Dans un second temps, dans le cadre d’un autre cours centré sur le développement d’interfaces web, un frontend a été conçu pour accompagner cette API. Cette partie a été réalisée par Lola Castan et Lallie Chappon, permettant une interaction utilisateur avec les fonctionnalités de l’API via une interface graphique.

Enfin, dans un troisième cours consacré à la qualité logicielle et aux tests, le projet a été repris et enrichi. Ce travail s’est fait en collaboration entre Lola Castan, Louis Baye, et Lallie Chappon. L’objectif de cette dernière étape était d’améliorer la robustesse du code, d’écrire des tests unitaires et d’intégration, et de mettre en place de bonnes pratiques en matière de couverture de code, de refactorisation et de documentation technique.


*Branches*
main : branche de production, contient les versions stables.

develop : branche de développement principal.

feature/* : pour le développement de nouvelles fonctionnalités.

fix/* : pour la correction de bugs.

release/* : pour préparer une nouvelle version à partir de develop.



*Éléments d’architecture*
L’API est conçue selon une architecture REST avec les composants suivants :

Backend : Node.js + Express

Base de données : MongoDB (schéma joueur, partie, cartes)

Authentification : JWT (JSON Web Tokens)

Gestion des états de jeu : via un contrôleur centralisé GameManager

Tests : Jenkins ochestre et jest execute les tests unitaires.


*Labels applicables au projet*
fix : gestion d'un bug
style: ajout style sans logique
feat : Proposition d’amélioration ou nouvelle fonctionnalité
doc : Changements ou ajouts dans la documentation
alt : Besoin de clarification ou discussion
urgent : Tâche prioritaire à traiter rapidement
refacto: Réorganisation du code sans ajout de fonctionnalité
test : Élément lié aux tests unitaires ou d’intégration

