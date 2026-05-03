## 🎥 Pipeline ETL YouTube : Ingestion & Transformation Analytique


### 📝 Présentation du Projet
Ce projet consiste à concevoir un pipeline **ETL** (Extract - Transform - Load) complet pour automatiser la collecte et l'analyse de données provenant de l'API **YouTube Data v3**. En tant que **Data Engineer**, l'objectif est de transformer des réponses API brutes (JSON) en un dataset structuré prêt pour une exploitation décisionnelle sous **Power BI**.

### 🎯 Objectifs Pédagogiques
* **Interrogation d'API** : Manipuler des requêtes HTTP et exploiter des réponses au format JSON.
* **Gestion de Flux** : Maîtriser la pagination, les contraintes de quotas et le traitement par lots (*batching*).
* **Sécurité** : Sécuriser les identifiants via des variables d'environnement (`.env`).
* **Pipeline de Transformation** : Nettoyer et normaliser des données pour produire un dataset propre et structuré.
* **Business Intelligence** : Exploiter les données dans Power BI pour analyser l'engagement (vues, likes, commentaires).

### 🛠️ Stack Technique
* **Langage** : Python (Requests, Pandas, Json, Dotenv).
* **Source de Données** : API YouTube Data v3.
* **Visualisation** : Power BI Desktop.
* **Gestion de Projet** : Jira & GitHub.

---

### 🏗️ Architecture du Pipeline
Le pipeline suit une logique de type ETL industrielle :
1.  **Extraction** : YouTube API → Ingestion Python → Stockage brut (JSON).
2.  **Transformation** : Nettoyage → Normalisation → Dataset structuré.
3.  **Chargement** : Dataset structuré → Power BI.

---

### 🚀 Étapes de Réalisation

### 1. Configuration & Sécurité 🔐
*   Installation de l'environnement virtuel et des dépendances nécessaires.
*   Création d'un projet sur **Google Cloud Platform** et activation de l'API YouTube.
*   Utilisation d'un fichier `.env` pour stocker la clé API en évitant toute exposition sur GitHub.

### 2. Ingestion des Données 📥
*   Interrogation de l'API pour récupérer les playlists d'une chaîne.
*   Extraction des identifiants vidéo via l'endpoint `PlaylistItems` avec gestion de la pagination.
*   Récupération des métadonnées détaillées (titre, date, vues, likes) via l'endpoint `Videos`.

### 3. Transformation & Structuration ⚙️
*   Conversion des données JSON vers une structure tabulaire (DataFrame Pandas).
*   Normalisation des champs (dates, durées, types numériques).
*   Gestion des valeurs manquantes et sauvegarde en format structuré (CSV ou JSON).

### 4. Analyse et Visualisation 📊
*   Importation du dataset dans Power BI.
*   Création d'un dashboard analytique : performance des vidéos, évolution des vues dans le temps et analyse de l'engagement.

---

### 📦 Livrables
1. **Code Python** : Script du pipeline ETL.
2. **Dataset final** : Données propres et structurées.
3. **Dashboard Power BI** : Rapport interactif et décisionnel.

