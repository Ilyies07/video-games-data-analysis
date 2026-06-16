# Video Game Sales Analysis

> Analyse et nettoyage d'un dataset de ventes de jeux vidéo (1980-2020), avec exploration par genre, plateforme et région.

##  Contexte / Objectif du projet

Ce projet consiste à analyser le dataset Video Game Sales (VGSales), un ensemble de données publié en 2016 qui recense plus de 16 000 jeux vidéo sortis entre les années 1980 et 2016.
L’objectif principal est de réaliser une analyse exploratoire (EDA) afin de mieux comprendre la répartition des jeux, les tendances du marché, les plateformes dominantes et les genres les plus populaires.

Le travail commence par une phase de nettoyage des données, notamment la gestion des valeurs manquantes dans les colonnes Year et Publisher.
La colonne Publisher a été nettoyée en remplaçant les valeurs manquantes par "Unknown", tandis que la colonne Year a été convertie en entier tout en conservant les NaN lorsque l’année n’est pas renseignée.

L’analyse met en évidence plusieurs tendances, comme la forte concentration de jeux dans les années 2000, période correspondant à l’explosion du marché du jeu vidéo.
La décennie 2010 semble moins représentée, non pas à cause d’un ralentissement du marché, mais parce que le dataset s’arrête en 2016, ce qui ne couvre que la moitié de la décennie.

##  Source des données

- **Dataset** : Video Game Sales
- **Lien** : https://www.kaggle.com/datasets/gregorut/videogamesales
- **Description** : ~16 500 jeux vidéo avec leurs ventes par région (NA, EU, JP, autres) et ventes globales, ainsi que plateforme, genre, éditeur et année de sortie.
- **Licence** : CC0 (domaine public)

##  Outils et bibliothèques utilisés

- Python 3.x
- pandas
- matplotlib / seaborn
- Jupyter Notebook

##  Structure du dépôt

```
.
├── data/
│   └── vgsales.csv
│   └── analysis.ipynb
│   └── README.md

```

##  Méthodologie / Démarche

1. **Exploration initiale** : structure du dataset, types de colonnes, valeurs manquantes
2. **Nettoyage** :
   - Traitement des valeurs manquantes dans `Year` et `Publisher`
   - Conversion des types de colonnes
   - Vérification des doublons et valeurs aberrantes


##  Résultats clés / Insights
Le dataset regroupe 16 598 jeux vidéo publiés entre 1980 et 2016, ce qui couvre plus de 35 ans d’évolution du marché.

Deux colonnes présentent des valeurs manquantes :

Year : 271 valeurs manquantes

Publisher : 58 valeurs manquantes

La distribution par décennie montre une forte croissance du nombre de jeux dans les années 2000, période correspondant à l’expansion massive du marché (PS2, Wii, DS, X360, PS3).

La décennie 2010–2020 apparaît moins représentée, non pas à cause d’un ralentissement du marché, mais parce que le dataset s’arrête en 2016, ce qui ne couvre que la moitié de la décennie.

Les plateformes les plus performantes en termes de ventes globales sont PS2, X360, PS3 et Wii.

Les genres les plus populaires et les plus rentables sont Action, Sports et Shooter, qui dominent largement le marché.

##  Pistes d'amélioration


À compléter.

##  Auteur

- **LERHZAL Ilyies** 
