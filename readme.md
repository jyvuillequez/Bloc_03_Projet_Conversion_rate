# Bloc 03 – Projet Conversion Rate

Analyse de données marketing pour comprendre les facteurs qui influencent le taux de conversion et optimiser les parcours utilisateurs.

Projet réalisé dans le cadre de la certification **RNCP Niveau 6 – Concepteur Développeur en Science des données (Jedha Bootcamp)**.

## 1. Contexte & enjeux

- **Problématique métier :** 
Ce projet vise à exploiter des données de navigation utilisateur pour comprendre les comportements associés à la conversion, anticiper les conversions futures et proposer des leviers d’optimisation.
- **Décideurs cibles :** marketing, produit, direction business

## 2. Objectifs du projet

- Analyser les comportements utilisateurs influençant le taux de conversion.
- Construire et comparer plusieurs modèles de classification binaire.
- Gérer un fort déséquilibre de classes (faible taux de conversion).
- Évaluer les modèles avec des métriques adaptées au contexte business.
- Formuler des recommandations pour améliorer la conversion.

## 3. Compétences mobilisées

- Analyse exploratoire de données (EDA)
- Préparation et nettoyage des données
- Feature engineering
- Modélisation en classification (Logistic Regression, Random Forest, XGBoost)
- Évaluation de modèles (ROC AUC, F1-score, Precision, Recall)
- Visualisation et data storytelling

## 4. Données

- **Source :** dataset fourni dans le cadre d’un challenge de classification
- **Périmètre :**
  - 285 000 lignes
  - Taux de conversion = 3 %
- **Variables clés :**
  - `age`
  - `country`
  - `new_user`
  - `source`
  - `total_pages_visited`
  - `converted` (variable cible)

## 5. Méthodologie

### 1. Préparation des données
- Gestion des valeurs manquantes.
- Nettoyage des valeurs aberrantes (ex : âge).
- Création de variables dérivées (bins d’âge, nombre de pages visitées).
- Encodage des variables catégorielles.

### 2. Analyse exploratoire (EDA)
- Analyse du déséquilibre de la variable cible.
- Étude du taux de conversion par pays, âge et volume de navigation.
- Analyse des corrélations entre variables numériques.

### 3. Modélisation
- **Baseline :** Régression Logistique.
- **Modèles avancés :** Random Forest, XGBoost
- Validation croisée et tuning d’hyperparamètres.
- Comparaison des performances sur jeu de test.

### 4. Évaluation
- Métriques principales
- Analyse des matrices de confusion.
- Étude de la distribution des prédictions.

### 5. Restitution
- Comparaison synthétique des modèles.
- Choix du modèle final.

## 6. Résultats & recommandations

### Résultats clés
- Tous les modèles présentent une excellente capacité de séparation (ROC AUC = 0.99).
- XGBoost offre le meilleur compromis global entre précision et recall.
- La complexité accrue des modèles n’apporte qu’un gain marginal par rapport à la baseline.

### Limites & pistes d’amélioration
- Absence de données temporelles.
- Pas d’information sur le contenu des pages visitées.

## 7. Installations des librairies Python
```text
python -m pip install -r requirements.txt
```

## 8. Organisation du projet

```text
.
├─ data/
│  ├─ raw/       # données brutes
│  └─ outputs/   # prédictions et résultats exportés
├─ notebooks/    # notebooks Jupyter (EDA, modèles)
├─ src/          # scripts Python réutilisables
└─ présentation/ # slides, exports captures d'images
