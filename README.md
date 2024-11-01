# Customer Segmentation for Marketing Strategy

## Introduction

Ce projet a été réalisé sur **Databricks** et vise à créer une segmentation de clientèle en utilisant des algorithmes de **clustering** appliqués aux données de transactions et d’attributs de comptes de **9 000 titulaires de cartes de crédit actifs sur une période de 6 mois**. L'objectif est de soutenir les décisions stratégiques en matière de marketing en regroupant les clients en segments distincts.

## Objectifs du Projet

- **Optimiser les hyperparamètres** des algorithmes de clustering pour obtenir les segments les plus pertinents.
- **Explorer différentes méthodes de clustering** disponibles dans PySpark, comme **KMeans**, **BisectingKMeans** et **Gaussian Mixture Models (GMM)**.
- **Évaluer les performances des modèles** via des métriques telles que le score de silhouette, afin d’identifier la méthode la plus appropriée.
- **Fournir une analyse comparative** des différentes approches de clustering non supervisé utilisées.

## Contenu du Projet

### Première Approche
- Utilisation des modèles de clustering **KMeans**, **BisectingKMeans**, et **GMM**.
- **Validation croisée** pour optimiser les hyperparamètres des modèles.
- Hyperparamètres optimisés : le nombre de clusters, le nombre maximum d'itérations, et le seed pour assurer la reproductibilité des résultats.

### Deuxième Approche
- Utilisation d'un **pipeline intégré** avec des évaluateurs pour faciliter le processus de clustering et d'optimisation.
- Adoption d'une structure similaire à la première approche, mais en exploitant des évaluateurs intégrés dans le pipeline pour une meilleure gestion et reproductibilité.

### Troisième Approche
- Structuration des opérations en définissant des **fonctions pour optimiser les paramètres** de **KMeans** et **BisectingKMeans**.
- Mise en œuvre d'une approche modulaire pour le **modèle de formation et d'évaluation**, en facilitant la répétition et la personnalisation des étapes.

### Quatrième Approche
- Optimisation des hyperparamètres spécifiques de chaque algorithme en utilisant **ParamGridBuilder**.
- Simplification du processus d'optimisation en définissant directement les grilles de paramètres sans créer explicitement d'instances d'algorithmes.
- Cela permet de gagner en clarté et en efficacité, en gérant les hyperparamètres de manière centralisée.

## Optimisation des Modèles

L'optimisation des hyperparamètres a été effectuée par :
- **Grid Search** : Utilisation de ParamGridBuilder pour tester différentes combinaisons de paramètres.
- **Validation croisée** : Pour chaque modèle, des évaluateurs intégrés au pipeline évaluent les performances.
- **Visualisation du score de silhouette** : Graphiques comparatifs du score de silhouette pour chaque modèle, permettant d'évaluer visuellement la qualité des segments formés.

## Résultats Attendues

Le projet nécessite :
1. **Un notebook Jupyter** avec tout le code commenté.
2. **Un document PDF** contenant :
   - Les graphiques principaux avec explications détaillées.
   - Une analyse comparative des différentes approches de clustering utilisées.

## Prérequis et Installation

### Prérequis

- **Apache Spark** avec la bibliothèque **PySpark** pour clustering.
- Environnement de **Python 3.x** avec support Spark (exécuté sur **Databricks**).

### Installation

1. **Clonez le dépôt** :
   ```bash
   git clone <URL_du_dépôt>
   cd Customer_Segmentation_Marketing
