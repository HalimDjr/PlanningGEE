# 🎓 Plateforme de Gestion des Soutenances – Interface Étudiants & Enseignants

Cette application fait partie d’un système global de gestion des soutenances.  
Elle est destinée aux **enseignants encadrants** et aux **étudiants binômes**, afin de faciliter :
- La consultation et le choix des thèmes.
- La communication avec l’encadrant.
- La visualisation du planning final des soutenances.

> 📌 **Remarque :** La gestion administrative (ajout des enseignants, étudiants, salles, création du planning, etc.) se fait dans une application séparée dédiée à l’**administration**.

---

## 🧑‍🤝‍🧑 Rôles Utilisateurs

| Rôle | Capacités |
|-----|-----------|
| **Étudiant (Binôme)** | - Se connecter<br>- Consulter la liste des thèmes proposés<br>- Sélectionner un thème selon la spécialité<br>- Envoyer une demande de validation<br>- Consulter le planning final des soutenances |
| **Enseignant** | - Se connecter<br>- Proposer, modifier et supprimer des thèmes<br>- Consulter les choix des binômes<br>- Valider ou refuser l'affectation des thèmes<br>- Consulter son planning de participation aux jurys |

---

## 🚀 Fonctionnalités Principales

### 👨‍🎓 Côté Étudiants
- Visualisation des **thèmes disponibles** selon la spécialité.
- Sélection et **demande d'affectation**.
- Suivi de l’état (en attente / accepté / refusé).
- **Consultation du planning final**.

### 👨‍🏫 Côté Enseignants
- **Proposition de nouveaux thèmes** avec description détaillée.
- Modification / Suppression des thèmes proposés.
- **Validation des choix des binômes**.
- Consultation du **planning général et personnel**.

---

## 🛠️ Stack Technique

| Technologie | Rôle |
|-----------|------|
| **Next.js** | Framework Frontend |
| **React** | Construction des interfaces |
| **Tailwind CSS** | Stylisation moderne et responsive |
| **Node.js / Express / API REST** | Logique serveur et endpoints |
| **Prisma ORM** | Traitement et mapping de la base de données |
| **JWT Auth** | Sécurisation des sessions utilisateur |

### 🗄️ Base de données & Prisma

La base de données est gérée via **Prisma ORM**, permettant :
- Migration et versionnement du schéma (`prisma migrate`)
- Accès optimisé aux données via un **client généré automatiquement**
- Sécurité des requêtes SQL (pas d’injections)

#### 📌 Commandes Prisma utiles
```bash
# Générer le client Prisma
npx prisma generate

# Appliquer les migrations
npx prisma migrate dev

# Visualiser la base de données (Prisma Studio)
npx prisma studio
```
📦 Installation & Lancement
# Installer les dépendances
npm install

# Configurer la base de données dans .env
DATABASE_URL="mysql://user:password@localhost:3306/gestion_soutenance"

# Générer Prisma Client
npx prisma generate

# Lancer le serveur de développement
npm run dev

# Accéder à l'application
http://localhost:3000

🎨 Aperçu Interface
![Enseignant - indisponibilité ](./assets/Image1.png)
![Enseignant - validation des thèmes](./assets/Image2.png)
![Etudiant - choisir thème](./assets/Image3.png)

🎯 Objectif du Projet

Cette application vise à simplifier l'organisation des soutenances, réduire les erreurs liées à la gestion manuelle
et fluidifier la communication entre les étudiants et leurs encadrants.
