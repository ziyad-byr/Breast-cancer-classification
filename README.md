# Diagnostic du Cancer du Sein par Machine Learning

Ce projet implémente un système de classification binaire permettant de diagnostiquer des tumeurs (malignes ou bénignes) à partir du dataset UCI Breast Cancer Wisconsin. L'objectif est de comparer plusieurs algorithmes de Machine Learning pour identifier le plus performant en milieu médical.

## 🎯 Enjeux du projet
En oncologie, la précision du diagnostic est vitale. Ce projet met l'accent sur :
* **La réduction des faux négatifs** (ne pas rater une tumeur maligne).
* **Le benchmark de modèles** : analyse comparative de 6 algorithmes.
* **L'analyse exploratoire (EDA)** : compréhension des corrélations entre les caractéristiques cellulaires.

## 🛠️ Stack Technique
* **Langage :** Python 3
* **Analyse de données :** `Pandas`, `NumPy`
* **Visualisation :** `Seaborn`, `Matplotlib`
* **Machine Learning :** `Scikit-Learn`

## 📊 Pipeline de données
1. **Nettoyage :** Suppression des colonnes inutiles (`Unnamed: 32`, `id`).
2. **Encodage :** Transformation des étiquettes (M/B) en valeurs numériques via `LabelEncoder`.
3. **Exploration :** Heatmap de corrélation pour identifier les variables les plus discriminantes.
4. **Partitionnement :** Split 75% Train / 25% Test.
5. **Normalisation :** Mise à l'échelle des données via `StandardScaler` (essentiel pour la performance du SVM et du KNN).

## 🚀 Comparatif des performances
Après entraînement et test, voici les résultats obtenus (Accuracy) :
* **Logistic Regression : 97.35%** (Meilleur modèle)
* **SVM : 97.14%**
* **Random Forest : 96.26%**
* **KNN : 96.25%**
* **Decision Tree : 93.63%**
* **Naive Bayes : 92.73%**

## 📈 Visualisations incluses
Le notebook génère :
* Une **Heatmap** des corrélations pour comprendre les liens entre les mesures (rayon, texture, périmètre, etc.).
* Un **Bar Chart** comparatif des précisions pour chaque modèle.

## 💻 Comment utiliser ce projet
1. Téléchargez le dataset `data.csv`.
2. Ouvrez le notebook `Prédiction du cancer du sein.ipynb` dans Jupyter ou Google Colab.
3. Exécutez les cellules pour reproduire l'analyse et les entraînements.
