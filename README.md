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

# Poker Web App – Projet Fullstack (Front + API)

Bienvenue dans le dépôt principal de notre projet scolaire de Poker en ligne. Ce dépôt regroupe deux sous-modules Git :

* **`frontend-app`** : Interface utilisateur développée en TypeScript avec React.
* **`poker-api-mds`** : API REST développée en NestJS pour la gestion des tables de poker.

Les deux projets communiquent via des requêtes HTTP et sont conteneurisés avec Docker.

---

## Structure du dépôt

```bash
poker-project/
├── front/                 # Sous-module Git pour l'application front-end
├── api/                   # Sous-module Git pour l'API backend
├── docker-compose.yml     # Configuration multi-conteneurs Docker
└── README.md              # Ce fichier
```

---

## Objectif du projet

Développer une plateforme de poker (Texas Hold'em) fonctionnelle avec :

* Création et gestion d’utilisateurs
* Connexion / déconnexion
* Affichage du profil (pseudo + solde)
* Rejoindre une table de poker
* Démarrer une partie
* Jouer un tour complet (check, call, fold, bet...)

---

## Technologies principales

### Front-end

* React + TypeScript

### Back-end

* NestJS + TypeScript
* SQLite
* JWT pour l'authentification

### Infrastructure

* Docker / Docker Compose
* Git Submodules

---

## Installation & Lancement (via Docker)

### 1. Cloner ce dépôt **avec les sous-modules**

```bash
git clone --recurse-submodules https://github.com/votre-compte/poker-project.git
cd poker-project
```

> Si vous avez déjà cloné sans `--recurse-submodules`, vous pouvez faire :

```bash
git submodule update --init --recursive
```

### 2. Lancer les conteneurs

```bash
docker-compose up --build
```

Cela lance :

* Le front sur `http://localhost:5173`
* L’API sur `http://localhost:3000`

---

## Tests

### Outils

* Jest pour les tests unitaires
* Playwright pour les tests end to end

### Lancer les tests

```bash
# Tests unitaires
cd front
npm run test

# Tests E2E
cd front
npx playwright test --ui
```

---

## Équipe

* **Chapon Lallie**
* **Castan Lola**
