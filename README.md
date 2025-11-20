# Titanic Survival Prediction  
Machine Learning Projekt zur Teilnahme an der **[Kaggle „Titanic – Machine Learning from Disaster“](https://www.kaggle.com/c/titanic) Competition**

## Projektübersicht  
Dieses Notebook untersucht die Überlebenswahrscheinlichkeit der Passagiere der RMS Titanic anhand von Passagierdaten. Ziel ist die Vorhersage, wer überlebt hat („Survived“: 1) und wer nicht („Survived“: 0).  
Dabei werden klassische Schritte eines Data-Science-Workflows verfolgt: Datenexploration (EDA), Feature Engineering, Preprocessing, Modellierung, Hyperparameter-Optimierung und Interpretation.

## Inhalt  
- **Explorative Datenanalyse (EDA):**  
  - Fehlende Werte identifizieren  
  - Kategorische Verteilungen (z. B. Geschlecht, Klasse, Einschiffungshafen) visualisieren  
  - Neue Features ableiten (z. B. `FamilySize`, `IsAlone`, `Deck` aus „Cabin“)  
- **Preprocessing & Pipeline:**  
  - Numerische Features: Imputation mittels Median  
  - Kategorische Features: Imputation, One-Hot-Encoding  
  - Gemeinsam in `ColumnTransformer` eingebunden  
- **Modellierung:**  
  - Baseline: Logistic Regression  
  - Leistungsmodell: Random Forest (mit Hyperparameter-Tuning via `GridSearchCV`)  
- **Modellinterpretation:**  
  - Feature Importance des Random Forest  
- **Submission:**  
  - Finale Vorhersage für das Test-Dataset erstellt und als `submission.csv` exportiert, geeignet für Einreichung auf Kaggle

## Wichtige Ergebnisse  
- Cross-Validation (5-fold) mit Random Forest erreichte eine mittlere Accuracy von **ca. 0.82**  
- Die besten Hyperparameter waren:  
  ```text
  max_depth = 10  
  n_estimators = 200  
  min_samples_split = 2  
  min_samples_leaf = 1
  ```
