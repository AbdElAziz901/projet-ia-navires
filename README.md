# Projet IA Navires

Analyse et modélisation des comportements de navigation des navires à partir de données AIS.  
Le projet permet de regrouper, classifier et prédire les trajectoires des navires grâce au Machine Learning.

## Objectifs

- **Clustering** : Regrouper automatiquement les navires selon leurs comportements de navigation.  
- **Classification** : Prédire le type d’un navire (supervisé).  
- **Régression** : Prédire la trajectoire future d’un navire.  
- Fournir trois scripts exécutables pour chaque besoin client.

## Compétences mobilisées

- Machine Learning : clustering, classification, régression.  
- Traitement de données et pipeline IA.  
- Évaluation de modèles : Silhouette, Calinski-Harabasz, F1-score, etc.  
- Manipulation de données : pandas, NumPy.  
- Visualisation : Plotly, Mapbox.  
- Packaging de projets IA : scripts et modèles persistés.

## Contenu du dépôt

code_client_1.ipynb – Clustering (directions, vitesses).
code_client_3.ipynb – Régression (trajectoires).
Code.ipynb – Classification (sélection variables, modèles KNN/Dummy).
Visualisations PNG générées (ex. matrice de confusion).
Modèles .pkl et fichiers de variables sélectionnées.
(Fichier de données non inclus pour cause de taille).
export_IA.csv 

## Comment utiliser le projet

- Télécharge le projet puis unzip le dossier et Ouvre le dossier dans VS Code
- Chaque dossier Besoin_Client_X contient un code.ipynb réalisant le besoin spécifique.  
- models/ contient les modèles sauvegardés.  
- scripts/ contient les scripts exécutables en ligne de commande.
- je vous conseille de lire le document "sujet.pdf" pour bien comprendre les besions 

