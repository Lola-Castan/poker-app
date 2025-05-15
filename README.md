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
