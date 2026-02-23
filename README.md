# 🕵️ Projet GOTHAM (Personal Project)
### Souveraineté des Données & Ingénierie de Renseignement (Link Analysis)

## 📖 Philosophie Opérationnelle
Le projet **GOTHAM** est une initiative personnelle visant à fusionner l'expertise de terrain acquise en gendarmerie avec l'ingénierie de données moderne. L'objectif est de transformer des données publiques brutes en intelligence actionnable grâce à la **Link Analysis** (Analyse de liens).

La vision centrale repose sur l'**Ancrage Terrain** : ne jamais traiter une donnée sans comprendre la réalité physique ou tactique qu'elle représente.

---

## 🌐 Sources de Données & Ingestion
Contrairement aux flux industriels, GOTHAM se base exclusivement sur des sources ouvertes (OSINT) et publiques :
* **Open Data** : Exploitation des jeux de données massifs de **Data.gouv.fr** (Justice, Intérieur, Territoires).
* **Web Scraping** : Collecte automatisée de données issues de sources publiques pour enrichir les analyses.
* **OSINT** : Recherche et structuration d'informations provenant de sources ouvertes pour le renseignement criminel ou administratif.

---

## 🏗️ Architecture Technique (Type ELT)
Le projet applique une rigueur industrielle de type ELT pour garantir la fiabilité des analyses.

### 1. Couche SOURCE : Collecte & Souveraineté
* **Ingestion Massive** : Gestion de sources hétérogènes (API, CSV, JSON issus du scraping).
* **Traçabilité** : Chaque donnée est importée brute avec un suffixe de traçabilité (`_raw`) pour garantir l'intégrité de la "Preuve".

### 2. Couche CLEAN : Standardisation
* **Data Quality** : Nettoyage drastique pour éliminer les bruits de fond et les erreurs de saisie publique.
* **Normalisation** : Conversion des entités (Noms, Lieux, Dates) dans un format standardisé pour permettre le croisement.

### 3. Couche ENRICHED : Link Analysis (La Valeur Ajoutée)
* **Jointures Complexes** : Création de liens entre des datasets qui "ne se parlent pas" naturellement (ex: Cartographie criminelle vs Données socio-économiques).
* **Clés de Voûte** : Identification d'identifiants pivots pour lier des dossiers, des individus ou des lieux géographiques.

### 4. Couche ONTOLOGY : Visualisation & Renseignement
* **Graphe de Relations** : Structuration finale pour des outils de Link Analysis ou de visualisation dynamique.
* **Dashboard Tactique** : Mise à disposition d'indicateurs permettant une compréhension immédiate des phénomènes analysés.

---

## 🛠️ Stack Technique GOTHAM
* **Langages** : Python (Pandas pour le wrangling, BeautifulSoup/Scrapy pour la collecte), SQL.
* **Environnement** : Développé sous **Google Antigravity** avec l'assistance de **Claude 4.6 Opus**.
* **Analyse** : Méthodologies d'investigation criminelle appliquées à la Data Science.

---

## 🎯 Roadmap du Projet
1. **Phase 1** : Automatisation du scraping des sources prioritaires sur Data.gouv.
2. **Phase 2** : Mise en place d'une base de données relationnelle pour la Link Analysis.
3. **Phase 3** : Déploiement d'une interface de visualisation des réseaux d'influence ou de causalité.

---
[cite_start]*Note : Ce projet est mené à titre personnel et illustre une capacité à gérer des architectures de données complexes en toute autonomie[cite: 3].*
