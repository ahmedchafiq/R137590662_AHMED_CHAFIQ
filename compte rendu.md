# 📘 RAPPORT COMPLET – ANALYSE DATA SCIENCE DU CANCER DU SEIN
![IMG_5613.jpg](https://github.com/ahmedchafiq/R137590662_AHMED_CHAFIQ/blob/75e49df8852661a4311221856dd805c4094dc65e/IMG_5613.jpg)

---

## 1. Contexte Médical & Objectif du Projet

### 🎯 Problème
Le diagnostic du cancer du sein repose sur des images microscopiques complexes. Fatigue humaine, erreurs de lecture et surcharge de travail peuvent entraîner des erreurs critiques.

Ces erreurs n’ont pas le même impact :

- ⚠ **Faux Positif** (annoncer un cancer à tort) → stress + examens inutiles  
- ❌ **Faux Négatif** (ne pas détecter un vrai cancer) → risque vital

### 🎯 Mission du projet
Développer un modèle de Machine Learning capable de prédire si une tumeur est **maligne (0)** ou **bénigne (1)** à partir de caractéristiques cellulaires.

**Objectif prioritaire : maximiser le Recall pour éviter les faux négatifs.**

---

## 2. Le Dataset Utilisé

Nous utilisons le **Breast Cancer Wisconsin Dataset** (Scikit-Learn).

### 🧩 Structure :
- **30 variables explicatives (features)**  
  Exemples :  
  - mean radius  
  - texture  
  - perimeter  
  - concavity  
  - symmetry  

- **1 variable cible : target**  
  - `0` = Malin  
  - `1` = Bénin  

Ce dataset est une référence internationale pour les tâches de classification médicale.

---

## 3. Simulation des Données Réelles (“Données Sales”)

Pour rendre le projet réaliste, le script introduit **5% de valeurs manquantes (NaN)** dans les colonnes des features.

Cela simule des problématiques courantes :

- erreurs de mesure  
- capteurs défaillants  
- saisie manuelle incorrecte  
- fichiers incomplets  

Cette étape est essentielle pour apprendre à gérer des données imparfaites.

---

## 4. Nettoyage & Préparation (Data Wrangling)

### 🧹 Problème : les NaN
Les algorithmes de Machine Learning ne peuvent pas fonctionner avec des valeurs manquantes.

Une seule valeur NaN peut faire échouer :

- les calculs matriciels  
- les arbres de décision  
- les distances entre points  

### 🔧 Solution : Imputation par la Moyenne
Le script applique :


