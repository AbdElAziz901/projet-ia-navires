# Projet IA Navires

Analyse et modélisation des comportements de navigation des navires à partir de données AIS.  
Le projet permet de regrouper, classifier et prédire les trajectoires des navires grâce au Machine Learning.

## Objectifs

- **Clustering** : Regrouper automatiquement les navires selon leurs comportements de navigation.  
- **Classification** : Prédire le type d’un navire (supervisé).  
- **Régression** : Prédire la trajectoire future d’un navire.
- À partir du fichier nettoyé export_IA.csv (issu de la partie Big Data).
- Fournir trois scripts exécutables pour chaque besoin client.

## Fonctionnalités Implémentées

### Besoin Client 1 – Clustering (Non supervisé)
- **Algorithmes** : K-Means + HDBSCAN
- **Variables** : Direction (COG → coordonnées cartésiennes), Vitesse (SOG), Heading
- **Évaluation** : Indice de Silhouette (jusqu’à 0.85)
- **Résultat** : Détection automatique des voies maritimes et profils de navigation

### Besoin Client 2 – Classification (Supervisé)
- **Objectif** : Prédire le VesselType (60, 70, 80…)
- **Sélection de variables** : Corrélation → Cargo, Draft, Width, Length
- **Modèle** : KNN (meilleur que Dummy Classifier)
- **Évaluation** : Matrice de confusion, F1-score, précision/rappel
- **Modèles sauvegardés** : model_knn.pkl, scaler_knn.pkl

### Besoin Client 3 – Régression (Prédiction de trajectoire)
- **Objectif** : Prédire la position future (LAT/LON) d’un navire
- **Méthode** : Régression linéaire sur séquences de 5 points → prédire le 6e
- **Traitement** : Groupement par MMSI + tri chronologique
- **Résultat** : Prédiction cohérente sur des milliers de points

## Technologies Utilisées
- Python : pandas, numpy, scikit-learn, hdbscan, seaborn, joblib
- Jupyter Notebook (.ipynb)
- Modèles persistés (.pkl) et scripts de prédiction interactifs

## Contenu du dépôt

- Code_client_1.ipynb  Clustering (directions, vitesses).
- Code.ipynb Classification (sélection variables, modèles KNN/Dummy).
- Code_client_3.ipynb  Régression (trajectoires).
- Visualisations PNG générées (ex. matrice de confusion).
- Modèles .pkl et fichiers de variables sélectionnées.
- export_IA.csv (Fichier de données non inclus pour cause de taille).

## Comment exécuter

- Télécharge le projet puis unzip le dossier et Ouvre le dossier dans VS Code
- Chaque dossier Besoin_Client_X contient un code.ipynb réalisant le besoin spécifique.  
- models/ contient les modèles sauvegardés.  
- scripts/ contient les scripts exécutables en ligne de commande.
- je vous conseille de lire le document "sujet.pdf" pour bien comprendre les besions 

