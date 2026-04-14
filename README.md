# Prédiction énergétique des bâtiments non-résidentiels — Seattle

Projet de data science dans le cadre de la formation OpenClassrooms.

**Objectif** : aider la ville de Seattle à atteindre la neutralité carbone en 2050 en prédisant la consommation d'énergie et les émissions de CO₂ des bâtiments non-résidentiels non encore mesurés, à partir des relevés 2016.

## Résultats

| Cible | Modèle | R² test |
|-------|--------|---------|
| Consommation énergétique (`log_SiteEnergyUse`) | Ridge (α=2.81) | **0.707** |
| Émissions CO₂ (`log_TotalGHGEmissions`) | Gradient Boosting (optimisé) | **0.691** |

## Structure du projet

```
Projet_3/
├── 2016_Building_Energy_Benchmarking.csv            # données brutes Seattle 2016
├── building_energy_cleaned.csv                      # données nettoyées 
├──1_analyse.ipynb                    # EDA et feature engineering
├──2_modelisation_target_energie_V2.ipynb   # modèle énergie
└──3_target_emission_V2.ipynb               # modèle émissions 
```

## Installation

```bash
poetry config virtualenvs.in-project true
poetry env use /usr/local/bin/python3.14
poetry install
```

## Stack

- Python 3.14 — scikit-learn, pandas, numpy, matplotlib, seaborn, plotly
- Gestion des dépendances : Poetry
