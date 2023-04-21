# titanic_kaggle

Predict survival on the titanic using trees and ensembles (bagging and boosting): best score = 0,7751

Lien vers notebook Kaggle :https://www.kaggle.com/code/hlnecorbel/corbel-survival-titanic/notebook

Différentes versions du notebook, la dernière (version 16) avec les 2 scores de soumission

Démarche de modélisation:

De façon générale, examen d'un ensemble de métriques de performance pour chaque modèle et train_test split (75% 25%) aléatoire en amont des optimisation d'hyperparamètres.

-entrainement d'un tree classifier sans contrainte, choix des features définitives
-entrainement d'un tree classifier contraint par des hyperparamètres optimisés: première soumission (accuracy score)
-entrainement d'un random forest, d'un extratreeclassifier, d'un adaboost avec hyperparamètres optimisés
-entrainement d'un xgboost avec d'abord peu d'arbre et un taux d'apprentissage rapide, et sélection d'hyperparamètres sur cette base
-Les hyperparamètres retenus précedemment sont ensuite utilisés avec un nombre croissant d'arbres et un taux décroissant d'apprentissage.
-sélection du meilleur modèle (xgboost) et deuxième soumission (accuracy score)

Table of Contents version 16

1. Préparation des données
1.1. Imports
1.2. Récupération et description des données
1.3. Nettoyage, exploration et création des features de base
2. Baseline: tree classifier, sélection des features de base
3. Optimisation hyperparamètetres tree classifier
---> première soumission
4. Méthodes ensemblistes
4.1. Bagging
4.1.1. Random Forest
4.1.2. Extratree Classifier
4.2. Boosting
4.2.1. Adaboost
4.2.2. XGBoost
---> seconde soumission
