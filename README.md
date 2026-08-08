# PREDICTIVE MAINTENANCE SYSTEM ⚙️
### Machine learning project
## *Author: Balkis Joudi* 
**LinkedIn:** https://www.linkedin.com/in/balkis-joudi-332076328/

---
---


## **I/OBJECTIF:** <br>
 Les pannes imprévues, les arrets soudains des machines entrainant une interruption de la production et une perte de productivité , les couts élevés de réparation... tous ces problèmes que témoignent les industries quotidiennement peuvent etre résolus par un système de maintenance prédictive qui est capable de prédire les pannes des machines avant qu’elles surviennent en se basant sur leurs données de fonctionnement.

---
---
## **II/DATASET UTILISE:** <br>
https://www.kaggle.com/datasets/hiimanshuagarwal/predictive-maintenance-dataset

---
---
FEATURES <br>
1/date : date de la mesure. <br>
2/ device: identifiant de la machine. <br>
3/ metric1, metric2, metric3, metric4, metric5, metric6, metric7, metric8, metric9 : les mesures des différents capteurs. (Dans notre cas, les mesures sont anonymes).
    
TARGET (CIBLE) <br>
4/failure : indique si la machine est en panne ou non. <br>
*failure=0: Pas de panne.
*failure=1: Panne.

---
---
## **III/EDA:** <br>
C’est la partie de l’exploration des données du dataset avant de les manipuler. <br>
*Visualisation des valeurs manquantes.
*Vérification de l’existence des doublons.
*Visualisation des valeurs aberrantes (outliers).
*Relation entre les variables.
*Comptage des valeurs.
*Analyse de la variable cible.

---
---
## **IV/PRETRAITEMENT:** <br>
*Suppression des doublons.
*Séparation des jours, mois et années et leur visualisation.
*Encodage des identifiants des machine dans un nouvel attribut “device_encoded”.
*Suppression des colonnes “device”, “date” et “metric8”.

---
---
## **V/SEPARATION DES DONNEES:** <br>
*Standardisation (Pour que toutes les variables aient la meme unité): On sépare ensuite les données d’entrainement de celles du test et on fait l’équilibrage nécessaire pour les données d’entrainement. Dans notre cas, on a choisi de faire un oversampling avec la fonction SMOTE(). On peut aussi un undersampling, mais dans ce cas, on va perdre des données.

---
---
## **VI/MODELE DU MACHINE LEARNING:** <br>
Il s’agit d’un problème de classification donc on peut utiliser l’algorithme XGBOOST: <br>
Avantages: <br>
  Ce modèle offre une très grande précision, il n’est pas sensible aux outliers. De plus, on peut changer sa précision en manipulant ses hyperparmaètres. <br>
-n_estimators: nombre d'arbres (trees) utilisés dans le modèle. <br>
-learning_rate: contrôle la contribution de chaque arbre. <br>
-max_depth: profondeur maximale de chaque arbre. <br>
-scale_pos_weight: rééquilibre les erreurs pendant l'entraînement. <br>
Inconvénients: <br>
   XGBOOST est plus lent si on demande une grande précision, plus complexe puisqu’on doit donner les valeurs optimales pour ses hyperparamètres.

---
---
## **VII/ENTRAINEMENT DU MODELE:** <br>
Le modèle est entrainé sur les données d’entrainement puis il utilise les données de test pour prédire la valeur cible.

---
---
## **VIII/EVALUATION:** <br>
*La précision du système est: 99,91% mais le système a un problème à détecter les pannes. 

---
---
## **IX/TEST:** <br>
Finalement, On entre un nouvel échantillon avec des nouvelles valeurs qu’on choisit et on voit le prédiction du système. 

---
---
## **X/CONCLUSION:** <br>
 Au cours de ce projet, on a appris qu’on peut fusionner la technologie avec l’industrie en concevant un système de maintenance prédictive à base de ML offrant l’opportunité de prédire l'état des composants d'une machine à partir des données issues des capteurs. 
    Un démarche composé d’un EDA, suivi d’un prétraitement des données, un entraînement du modèle et finalement une évaluation nous a identifié le modèle le plus performant pour cette tâche. 
       Les résultats montre ,ainsi, qu’un tel modèle permet d'anticiper les défaillances, réduire les arrêts imprévus et optimiser les opérations de maintenance dans les secteurs industriels.
       

