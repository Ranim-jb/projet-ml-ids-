# Expliquer un détecteur d'intrusion (UNSW-NB15)

Projet 1 du module Machine Learning pour la cybersécurité : interprétabilité d'un détecteur d'intrusion
(random forest, XGBoost, baseline) avec importance interne, importance par permutation et SHAP.

Question centrale : le modèle apprend-il des comportements d'attaque ou des artefacts de collecte ?

## Structure
```
projet-ml-ids/
├── projet1_unsw_nb15_interpretabilite.ipynb   # code + rapport
├── requirements.txt
├── README.md
├── .gitignore
├── data/                                      # CSV non versionnés (voir data/README.md)
└── figures/                                   # figures exportées pour le rapport
```

## Installation (Windows PowerShell, Python 3.12 recommandé)
```powershell
py -3.12 -m venv .venv
.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
python -m pip freeze > requirements-lock.txt   # versions exactes utilisées
```
Linux / macOS : `python3.12 -m venv .venv && source .venv/bin/activate`.

## Données
Voir `data/README.md`. Les données brutes ne sont pas dans le dépôt.

## Exécution
```powershell
jupyter lab --no-browser
```
Ouvrir l'adresse `http://localhost:8888/lab?token=...` affichée, puis le notebook, vérifier le noyau Python 3.
Exécuter de haut en bas. La section 8 (ablation) demande de remplir la liste `SUSPECT`
après l'audit de la section 7.

## Reproductibilité
- Graine fixée (`SEED = 42`) pour les découpages, modèles et échantillons.
- Test utilisé une seule fois pour les résultats finaux ; aucune opération apprise sur le test.
- Versions des bibliothèques : voir `requirements-lock.txt` et la première cellule du notebook.

## Éthique
Données publiques uniquement ; aucune attaque contre un système réel.

## Auteur
[Nom Prénom], travail individuel.
