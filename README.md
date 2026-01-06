# Projet de Recherche – SMOTE et Déséquilibre de Classes

## 📌 Contexte académique
Projet réalisé dans le cadre du cours **Data Science** – M2 Actuariat (ISFA)
Encadrant : François HU (Milliman R&D)
Année universitaire : 2025–2026

## 👥 Auteurs
CERCLERON Léa
YASSIR Hafsa
BRANGER Adélaïde
FAVROT Marion

## 📄 Article de référence
**Titre** : *SMOTE: Synthetic Minority Over-sampling Technique*  
**Auteurs** : N. V. Chawla, K. W. Bowyer, L. O. Hall, W. P. Kegelmeyer (2002)

## 🎯 Objectif du projet
L’objectif de ce projet est d’étudier et d’évaluer l’impact des méthodes de rééchantillonnage,
et en particulier **SMOTE**, sur la performance prédictive de modèles de classification
appliqués à un cas d’usage actuariel présentant un **déséquilibre marqué de classes**.

Le projet vise à comparer :
- une approche sans rééchantillonnage,
- une approche avec SMOTE,
- d’autres stratégies classiques (sur-échantillonnage et sous-échantillonnage).

## 🧪 Cas d’usage actuariel
Le cas d’usage étudié concerne la **détection d’épisodes de sécheresse** à partir de données météorologiques et environnementales aux États-Unis. Pour cela, deux bases de données "soil_data.csv" et "train_timeseries.csv" sont concaténées.

- Domaine : risque climatique
- Variable cible : indicateur binaire de sécheresse
- Classe minoritaire : épisodes de sécheresse
- Enjeu actuariel : anticipation de la sinistralité liée aux événements climatiques extrêmes

Les données proviennent de jeux Kaggle (https://www.kaggle.com/datasets/cdminix/us-drought-meteorological-data?resource=download) issus notamment de sources officielles (NASA POWER Project, U.S. Drought Monitor).


## 🗂️ Structure du dépôt
data/ → jeux de données bruts et prétraités
notebooks/ → analyses exploratoires et expérimentations
src/ → implémentations modulaires (prétraitement, SMOTE, modèles)
results/ → résultats finaux, métriques et visualisations
report/ → rapport PDF soumis

## 📁 Description des dossiers
### data/
- `raw/` : données brutes, non modifiées  
- `processed/` : données après nettoyage et rééchantillonnage  
- `README.md` : description de l’origine et des variables des datasets

### notebooks/
Le notebook utilisé mise dans ce dossier

### src/
Scripts Python modulaires :
ex : 
- `preprocessing.py` : nettoyage et préparation des données  
- `resampling.py` : implémentation de SMOTE et méthodes comparatives  
- `models.py` : modèles de classification  
- `evaluation.py` : métriques et fonctions d’évaluation

## 🔬 Méthodologie
La démarche suivie est la suivante :
1. Analyse exploratoire et diagnostic du déséquilibre de classes
2. Prétraitement des données (nettoyage, standardisation)
3. Transformation de la variable cible en classification binaire
4. Séparation stricte train / test
5. Application de **SMOTE uniquement sur l’échantillon d’entraînement**
6. Entraînement de plusieurs modèles de classification
7. Évaluation des performances sur le jeu de test non modifié

## 📊 Métriques d’évaluation
Les performances sont évaluées à l’aide de métriques adaptées aux classes rares :
- Precision
- Recall
- F1-score
- AUC ROC
- AUC Precision-Recall

## ▶️ Instructions d’exécution
1. Créer un environnement virtuel :
python -m venv venv
source venv/bin/activate
2. Installer les dépendances :
pip install -r requirements.txt
3. Lancer Jupyter Notebook :
jupyter notebook
Exécuter les notebooks dans l’ordre numérique.

## ⚠️ Bonnes pratiques et points d’attention
SMOTE est appliqué uniquement sur les données d’entraînement afin d’éviter toute fuite d’information.
Les données brutes ne sont jamais modifiées.
Les résultats sont interprétés de manière critique, notamment en termes de variance et de calibration.



