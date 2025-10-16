<h1 align="center"> 🍎 Projet 2 : Santé publique France : Analyse & Idée d’Application à partir du jeu de données Open Food Facts </h1>

> 🧠 *« Mieux comprendre les données alimentaires pour mieux nourrir demain. »*

<p align="center">
  <img src="https://camo.githubusercontent.com/166e03c1ba1444c6f5b5ee48b8aaeb33742566927ccda9ec6b1a935763a2396b/68747470733a2f2f7374617469632e646174612e676f75762e66722f696d616765732f39642f3762333132303830666534663538383638613932386264646266663330662e706e67"
       alt="Nutriscore logo"
       width="200"
       height="100"
       style="margin-right: 30px;">
  <img src="https://camo.githubusercontent.com/08ea261279923a8ec7a9fca299eecccab13e5ede6698eac6dbf27077c3ce902a/68747470733a2f2f7777772e7374796c62696f2e66722f696d672f636d732f696d616765732f6766782f6c6f676f2d757364612d6f7267616e69632e706e67"
       alt="Organic logo"
       width="200"
       height="100">
</p>


---

<h2 align="center"> 🎯 Contexte du projet : </h2>

<h3 align="center"> Scénario : </h3>

L'agence "Santé publique France" a lancé un appel à projets pour trouver des idées innovantes d’applications en lien avec l'alimentation. Vous souhaitez y participer et proposer une idée d’application.

Le jeu de données Open Food Facts est disponible sur le site officiel : **https://world.openfoodfacts.org/**

Les variables sont définies à cette adresse : **https://world.openfoodfacts.org/data/data-fields.txt**

<h3 align="center"> Les champs sont séparés en quatre sections : </h3>

- Nom, date de modification, etc.
- Un ensemble de tags : catégorie du produit, localisation, origine, etc.
- Les ingrédients composant les produits et leurs additifs éventuels.
- Des informations nutritionnelles : quantité en grammes d’un nutriment pour 100 grammes du produit.

<h3 align="center"> Qu'est ce que le Nutriscore : </h3>

Le **Nutri-score** est un système d'étiquetage nutritionnel à cinq niveaux, allant de **A** à **E** et du vert au rouge, établi en fonction de la valeur nutritionnelle d'un produit alimentaire. 

Il a pour but de favoriser le choix de produits plus sains d'un point de vue nutritionnel par les consommateurs et ainsi de participer à la lutte contre les maladies cardiovasculaires, l'obésité et le diabète de type 1.

<h3>Le score est calculé par un système de points, le score le plus faible étant le meilleur : </h3>

- Eléments défavorables au score :

    - apport calorique 
    - teneur en sucre 
    - teneur en graisses saturés 
    - teneur en sel

- Eléments favorables au score :

    - teneur en fruits, légumes, légumineuses et oléagineux 
    - teneur en fibres 
    - teneur en protéines

Source : **https://fr.wikipedia.org/wiki/Nutri-score**


<h3 align="center">Qu'est ce que le Label Organic : </h3>

Le label **ORGANIC** est une certification qui vous garantit qu'un produit est fabriqué avec le moins d'impact possible sur l'environnement tandis que le **label BIO** assure que les producteurs n'ont pas utilisé de pesticides ou autres produits chimiques pour cultiver leurs produits ou pour nourrir leurs animaux.

---

<h2 align="center"> 🧠 Objectifs du projet : </h2>

1. **Proposer une idée d’application** innovante, réaliste et fondée sur les données.  

2. **Explorer et nettoyer** le jeu de données Open Food Facts :  
   - Identifier les **variables pertinentes** (nutritionnelles, environnementales, catégorielles).  
   - Détecter et traiter les **valeurs manquantes**, **doublons** et **valeurs aberrantes**.  
   - Créer du feature engineering pour optimiser l'analyse
   - Nettoyage de la feature pays pour homogénéiser
   - Pour l'analyse on ne va garder que les produits > 50
   - Imputation des donnees via un **KNN Imputer**

3. **Analyser les données** :
   - Réaliser une **analyse univariée** (comportement individuel des variables).  
   - Réaliser une **analyse multivariée** (corrélations, tests statistiques, visualisations croisées).  

4. **Confirmer ou infirmer** des hypothèses en lien avec l’idée d’application.  

5. **Évaluer la faisabilité** du concept à partir des données disponibles.

---

<h2 align="center"> 🧰 Outils & Librairies utilisées : </h2>

- **Langage :** Python  
- **Environnement :** Jupyter Notebook  
- **Librairies d’analyse :** Pandas, NumPy, SciPy  
- **Librairies de visualisation :** Matplotlib, Seaborn, Plotly  
- **Tests statistiques :** ANOVA, corrélation de Pearson/Spearman, tests de normalité  

---

<h2 align="center">  🧩 Étapes principales du projet : </h2>

<h3 align="center"> 1. Traitement des données : </h3>

- Sélection des variables pertinentes pour l’application.  
- Analyse des valeurs manquantes et traitement par :
  - Imputation (moyenne/médiane/modale),
  - Suppression conditionnelle,
  - Estimation à partir d’autres variables.  
- Détection et correction des **valeurs aberrantes** (z-score, IQR).  
- Uniformisation des formats (unités, catégories, labels).  
- Automatisation des étapes via fonctions Python.

<h3 align="center"> 2. Analyse univariée  : </h3>

- Étude descriptive de chaque variable pertinente (moyenne, médiane, distribution).  
- Visualisations adaptées :
  - Histogrammes, boxplots, bar charts, pie charts.  
- Interprétation en langage simple, accessible au grand public.

<h3 align="center"> 3. Analyse multivariée : </h3>

- Étude des corrélations entre variables nutritionnelles et autres indicateurs.  
- Visualisation croisée (heatmaps, pairplots, scatterplots, matrice de corrélation).  
- Tests statistiques pour valider la significativité des relations.

<h3 align="center"> 4. Idée d’application  : </h3>

Pour mon cas,j'ai decide de mettre en avant le top des marques par : 

- Produit sans additifs
- Produit sans huile de palme
- Produit BIO
- Produit ORGANIC
- Produit Nutriscore A, B, C, D, E

---

<h2 align="center"> 🧠 Compétences évaluées : </h2>

- Communiquer ses résultats à l’aide de **visualisations claires et pertinentes**.  
- Effectuer des **opérations de nettoyage** sur des données structurées.  
- Réaliser une **analyse statistique univariée et multivariée**.  
- Argumenter la **faisabilité d’une application data-driven** à partir d’un jeu de données réel.

---

<h3 align="center">📌 Projet réalisé dans le cadre de la formation Data Scientist - Machine learning. </h3>
