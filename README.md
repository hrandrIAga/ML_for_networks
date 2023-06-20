# ML_for_networks

## Résultats au 07/06/2023 (challenge en cours) : 
> **2e position avec un MAE de 0.0025**

A compléter :
* Projet dans le cadre du module NET4550 de Télécom Sudparis
* Egalement un challenge public de l'ENS : [lien](https://challengedata.ens.fr/participants/challenges/89/)

### **Contexte**

SNCF-Transilien est l’opérateur des trains de banlieue en Île-de-France. SNCF-Transilien fait circuler plus de 6 200 trains permettant à 3,4 millions de voyageurs de se déplacer. Il collecte un nombre croissant de données sur les flux de voyageurs à bord grâce à des systèmes de comptage infra-rouges au niveau des portes des trains. Ce nombre croissant de données aide SNCF-Transilien à proposer de nouveaux services destinés aux voyageurs et à améliorer l’exploitation de tous les jours.

### **Objectifs**
Le but de ce challenge pour SNCF-Transilien est d**’explorer la possibilité de prédire à court terme le taux d’occupation à bord des trains en temps réel**. Cela permettrait de pouvoir donner un service d’informations en temps réel de la charge à bord à ses voyageurs au travers de ses médias numériques.

Lorsqu'un voyageur attend un train **k**à la gare **s**, le train peut se trouver plusieurs gares en amont, cependant nous souhaitons donner au voyageur l’information d’affluence la plus cohérente possible avec son expérience au moment où il montera dans le train. Pour ce faire, nous devons prédire pour chaque train la réalité des taux d’occupation aux prochaines gares. Ici, nous proposons de prédire, plus simplement, le **taux d’occupation à la prochaine gare** seulement.

### **Structure des données :**
Nous utilisons k pour spécifier le train, s pour spécifier la station et d pour spécifier le jour. k, s, d définit alors un arrêt.

* Un jeu de données Xtrain.csv avec 31 119 lignes (i.e. 31 119 arrêts k, s, d) et 12 colonnes
* Un jeu de données Xtest.csv avec 13 752 lignes (i.e. 13 752 arrêts k, s, d) et 12 colonnes
* Un jeu de données Ytrain.csv avec 31 119 lignes et une colonne, donnant la variable à prédire pour le jeu d'entraînement

Après avoir construit un modèle, on fait les prédictions sur Ytrain.csv
Cela nous donnera Ypred.csv qu'il faudra déposer comme rendu.
Un score est alors établi pour insérer le travail dans le classement (fondé sur la métrique MAE).



