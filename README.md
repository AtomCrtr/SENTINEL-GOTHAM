# 🕵️ Projet SENTINEL-GOTHAM
### Souveraineté des Données & Ingénierie de Renseignement (Link Analysis)

## 📖 Philosophie Opérationnelle : L'Ancrage Terrain
Le projet **Sentinel-Gotham** n'est pas une simple architecture technique ; il est la fusion entre l'expertise en ingénierie de données et la réalité tactique de la gendarmerie de terrain. 

La vision centrale repose sur l'**Ancrage Terrain** : garantir une compréhension physique de la donnée (connaître l'objet réel derrière la ligne de code) pour crédibiliser chaque choix technique face aux opérationnels. En tant que **Sole Contributor**, j'assume l'auto-conception de l'architecture et la recherche autonome des accès complexes.



---

## 🏗️ Architecture Technique (Type ELT)
Le pipeline est structuré pour transformer des flux hétérogènes en une ontologie robuste, permettant un pilotage réactif et automatisé.

### 1. Couche SOURCE : L'Ingestion Massive
* **Systèmes Cœurs** : Ingestion des tables SAP (Finance A2, Logistique, Production Header Core) servant de "Source de Vérité" unique.
* **Shadow IT** : Intégration des besoins métiers spécifiques via Google Sheets pour les données manuelles résiduelles.
* **Datasets Complexes** : Gestion de tables brutes massives (jusqu'à 174 colonnes) avec traçabilité garantie via suffixes spécifiques (type `_xprog`).

### 2. Couche CLEAN : Standardisation (Pipeline Builder)
* **Nettoyage Critique** : Standardisation des formats pour éliminer le "téléphone arabe de la donnée" issu des fichiers intermédiaires fragiles.
* **Filtres Périmétriques** : Application de filtres stricts sur les codes sites (Plant Code = "NZF") et centres de coûts ($Cost\ Center = "A350"$).
* **Normalisation** : Conversion systématique des formats de dates et typage rigoureux des colonnes.

### 3. Couche ENRICHED : La Valeur Ajoutée (Jointures Complexes)
* **La Clé de Voûte (AUFNR)** : L'Ordre de Fabrication est le pivot central reliant l'aspect financier, la matière physique et l'unité de production (MSN/Avion).
* **Jointures Tripartites** : Croisement des flux Logistique (Consommables) + Production (Planning/MSN) + Finance (Prix/Amount).
* **KPI Automatisé** : Calcul du coût unitaire via la formule :
[cite_start]$$unit\_price = \frac{amount}{quantity}$$ [cite: 31]
* **Gestion de la Granularité** : Utilisation de clés composées pour éviter les doublons entre les documents d'en-tête et les lignes d'items SAP.

### 4. Couche ONTOLOGY : Consommation & Visualisation
* **Mise à disposition** : Création du dataset final structuré pour les outils de visualisation (Slate / Streamlit).
* **Restitution Visuelle** : Dashboards permettant une mise à jour quotidienne des indicateurs et une réactivité accrue sur les aléas de production.

---

## 🛠️ Expertise Systèmes & Quick Wins
* **Maîtrise SAP** : Compréhension profonde de la relation entre Document Article et Items, et décodage des WBS Elements pour retrouver le numéro de série avion (MSN).
* **Full-Stack Agile** : Développement d'outils tactiques ("Waterspider") utilisant **Google Apps Script (JS)** pour sécuriser les saisies et **Looker Studio** pour le reporting immédiat.
* **Diagnostic Qualité** : Utilisation de **Python (Pandas/Jupyter)** pour l'analyse exploratoire et la validation des pivots stratégiques avant industrialisation.

---

## 🎯 Roadmap Stratégique
1. **Sprint 1-2** : Ingestion automatisée des sources manuelles et premières jointures physiques/financières.
2. **Sprint 3-4** : Intégration des données de planification pour finaliser le KPI "Coût par MSN".
3. **Long Terme** : Automatisation complète du pipeline industriel et suppression des silos externes.

---
*Ce projet est développé sous l'IDE **Google Antigravity** avec le support de l'IA **Claude 4.6 Opus**.*
