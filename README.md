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

1. **Exploration initiale** : chargement du dataset (16 598 jeux), 
   inspection des types de colonnes et identification des valeurs 
   manquantes (271 dans `Year`, 58 dans `Publisher`).

2. **Nettoyage** :
   - `Publisher` : remplacement des valeurs manquantes par `"Unknown"` 
     (colonne textuelle, la valeur reste exploitable)
   - `Year` : conservation des `NaN` sans remplacement (colonne numérique), 
     puis conversion en entier (`Int64`)
   - Aucun doublon détecté

3. **Transformation** :
   - Création d'une colonne `Decennie` (`Year // 10 * 10`) pour regrouper 
     les données par grandes périodes et améliorer la lisibilité des graphiques

4. **Analyse** : 4 questions explorées via `groupby` et agrégations :
   - Ventes globales par genre
   - Évolution des ventes par décennie
   - Top 10 des plateformes par ventes globales
   - Différences de préférences par genre selon les régions (NA / EU / JP)

5. **Visualisation** : barplots et courbes avec matplotlib/pandas

##  Résultats clés / Insights
- **Le genre Action domine largement le marché** : avec plus de 1 750 millions 
  d'unités vendues, il représente environ 20 % des ventes globales, loin devant 
  Sports (~1 300 M) et Shooter (~1 050 M).

- **Le pic des ventes se situe dans les années 2000** : les ventes mondiales 
  ont crû régulièrement des années 1980 jusqu'à atteindre leur maximum dans 
  les années 2000, avant de décliner. Ce déclin apparent dans les années 2010 
  et 2020 est à nuancer : le dataset ayant été collecté vers 2016, les données 
  de ces décennies sont incomplètes.

- **La PS2 est la plateforme la plus vendue de l'histoire** : avec plus de 
  1 250 millions d'unités vendues, elle devance largement la X360 (~980 M) 
  et la PS3 (~960 M).

- **Des préférences régionales très distinctes** : l'Amérique du Nord et 
  l'Europe sont dominées par les genres Action et Sports, tandis que le Japon 
  montre une préférence marquée pour les Role-Playing Games (RPG), dont les 
  ventes y sont proportionnellement bien plus élevées qu'en NA et EU.

##  Pistes d'amélioration

À compléter.

##  Auteur

- **LERHZAL Ilyies** 
