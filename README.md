# Prob_v00
Calcul Probability of event using Random Forrest !!

Ce programme est une application graphique (GUI) développée avec Tkinter qui permet d’entraîner un modèle de classification Random Forest à partir de données historiques, puis d’utiliser ce modèle pour prédire des probabilités sur de nouvelles données.

Fonctionnalités principales :
Chargement des données historiques

L’utilisateur peut charger un fichier Excel contenant des données historiques.

Ce fichier doit comporter obligatoirement 11 colonnes nommées Var1 à Var10 (variables explicatives) et Target (variable cible).

Ces données servent de base pour entraîner le modèle.

Entraînement du modèle

Après chargement des données historiques, le modèle Random Forest est entraîné.

La variable cible Target est binarisée : on calcule la médiane de Target dans les données historiques, puis on crée une variable binaire indiquant si la valeur dépasse cette médiane ou pas.

Le modèle est entraîné pour prédire cette variable binaire à partir des variables Var1 à Var10.

Les données sont divisées en ensemble d'entraînement (80%) et test (20%) pour entraîner et évaluer le modèle (bien que l’évaluation avec AUC soit commentée dans ce code).

Chargement des nouvelles données et prédiction

L’utilisateur peut charger un nouveau fichier Excel contenant les mêmes variables Var1 à Var10 (sans la variable cible).

Le modèle prédit alors la probabilité que Target dépasse la médiane définie précédemment.

Ces probabilités sont ajoutées au tableau sous une nouvelle colonne.

Affichage des résultats

Les résultats des prédictions sont affichés dans la fenêtre sous forme de texte, listant pour chaque ligne l’index, la date (présente dans les nouvelles données) et la probabilité exprimée en pourcentage avec deux décimales.

Sauvegarde des prédictions

L’utilisateur peut sauvegarder les nouvelles données enrichies des probabilités dans un fichier Excel.

Interface utilisateur soignée

Boutons clairement identifiés pour chaque étape : charger données historiques, entraîner le modèle, charger nouvelles données & prédire, enregistrer résultats, et quitter l’application.

Messages d’état et instructions claires dans la fenêtre pour guider l’utilisateur.

En résumé
Ce programme permet de charger des données historiques, d’entraîner un modèle de forêt aléatoire pour classifier si une variable cible dépasse un seuil médian, puis d’appliquer ce modèle à de nouvelles données pour prédire des probabilités associées. Tout cela est encapsulé dans une interface graphique conviviale pour faciliter l’usage même sans connaissance en programmation.
