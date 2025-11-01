# 🚀 Fullstack Blog — Strapi (TypeScript) + Next.js (App Router, TypeScript)

## 🧩 Description
Ce projet est un **blog complet** développé avec **Strapi** (backend CMS) et **Next.js** (frontend React moderne avec App Router et TypeScript).  
Il inclut la gestion complète du contenu (posts, catégories, tags, auteurs), la publication automatique avec ISR, le SEO dynamique, et une excellente UX.

---

## ✅ Fonctionnalités principales

### 🗂 Backend — Strapi (TypeScript)
- **Content-types :**
  - `Post`: titre, slug, contenu, résumé, image de couverture, auteur, catégorie, tags
  - `Category`: nom, slug, description
  - `Tag`: nom, slug
  - `Author`: nom, slug, bio, avatar
- Relations : 
  - `Post` ↔ `Author` (many-to-one)
  - `Post` ↔ `Category` (many-to-one)
  - `Post` ↔ `Tags` (many-to-many)
- **Système de brouillons/publications** (draft & publish)
- **API REST ou GraphQL**
- **Données de démonstration (seed)** :
  - ≥ 8 posts
  - 3 catégories
  - 5 tags
  - 2 auteurs
- Sécurité via **Roles & Permissions** configurés
- **Webhook Strapi → Next.js ISR** lors d’une publication

## 🏗️ Installation et configuration

### 1. Cloner le projet
```bash
git clone https://github.com/LouayLH10/CMS.git
cd CMS
```
 ### 2. Installer les dépendances
 ```bash
npm install
```
 ### 3. Configurer les variables d’environnement
 Crée un fichier .env à la racine :
 
# Server
HOST=0.0.0.0
PORT=1337

# Secrets
APP_KEYS=x/Wg/5yaeUEH1GcscDQcxQ==,zhZGSZUOGnJHoJXKFnZWvw==,18ZJ039e4jTlV/dZRTYbbw==,DxvtRzBASThXx52I6Z5AUw==
API_TOKEN_SALT=F0hxMI+5xhDp1hfqIBiiXg==
ADMIN_JWT_SECRET=2Kfy/nC3YfGNXkmxSUJEuA==
TRANSFER_TOKEN_SALT=ODKvrXbQpm8P4KzUYQh4uw==
ENCRYPTION_KEY=bIbQ5hn54vEeHtgwsPWYWg==

# Database
DATABASE_CLIENT=sqlite
DATABASE_HOST=
DATABASE_PORT=
DATABASE_NAME=
DATABASE_USERNAME=
DATABASE_PASSWORD=
DATABASE_SSL=false
DATABASE_FILENAME=.tmp/data.db
JWT_SECRET=lhmquUYyby+oSj3LZdLang==
 # ⚙️ Démarrage du serveur

En mode développement :
```bash
npm run develop
```
En mode Production:
```bash
npm run build && npm run start
```
Le serveur tourne par défaut sur :
👉 http://localhost:1337