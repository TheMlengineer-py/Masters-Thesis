# Forest Fire Detection Using Artificial Intelligence Solutions

MSc thesis submitted in partial fulfilment of the requirements for the degree of
MSc Artificial Intelligence and Data Science, University of Hull.

Author: Oyeyemi Dayo Tosin

## Abstract

Forest fires cause billions in damage annually and pose a severe threat to human
life, wildlife, and the economic stability of nations, with developing countries
often bearing the heaviest impact. Existing detection methodologies frequently
fall short of providing accurate, early warning. This study proposes a machine
learning based system for forest fire detection using meteorological features,
temperature, relative humidity, wind speed, and rainfall, as predictors of fire
occurrence. Five machine learning models were trained and evaluated on the
Algerian Forest Fire dataset from the UCI Machine Learning Repository, with the
best performing model, Support Vector Machine, identified as the most effective
approach for early and accurate forest fire prediction.

## Key Contributions

- A comparative evaluation of five machine learning models, Logistic Regression,
  Decision Tree, Random Forest, Gradient Boosting, and Support Vector Machine,
  for meteorological based forest fire prediction.
- Application of SMOTE (Synthetic Minority Oversampling Technique) to correct
  class imbalance between fire and non-fire observations.
- Feature importance analysis using SelectKBest, identifying Relative Humidity
  and Temperature as the strongest predictors of fire occurrence.
- Rigorous model validation using RepeatedStratifiedKFold cross-validation
  (n_splits=10, n_repeats=3) and statistical hypothesis testing (p-value and
  t-statistic) to compare top performing models.

## Methodology

1. **Data preprocessing and exploratory data analysis**: data cleaning,
   pairplots, histograms, correlation heatmaps, box and whisker plots, and
   scatter plots to visualise relationships between meteorological variables
   and fire occurrence.
2. **Class imbalance correction**: SMOTE applied to oversample the minority
   (not-fire) class to match the majority (fire) class.
3. **Feature selection**: SelectKBest applied to meteorological features to
   rank predictive importance.
4. **Model training**: five classifiers trained and benchmarked on test
   accuracy and wall clock time.
5. **Model validation**: RepeatedStratifiedKFold cross-validation and
   statistical hypothesis testing to determine the most robust model.


## Results

| Model | Test Accuracy | Wall Time | CV Mean Accuracy | CV Std Dev |
|---|---|---|---|---|
| Logistic Regression | 89% | 15ms | 83.5% | 0.084 |
| Decision Tree Classifier | 96% | 5ms | 89.3% | 0.062 |
| Random Forest Classifier | 93% | 350ms | 92.2% | 0.062 |
| Gradient Boosting Classifier | 93% | 87ms | 90.8% | 0.074 |
| Support Vector Machine | 93% | 2ms | 91.8% | 0.074 |

Cross-validation results show Random Forest and Support Vector Machine
achieving near equal average performance, statistically compared using
p-value and t-statistic hypothesis testing. Support Vector Machine was
identified as the optimal model, balancing strong accuracy with the lowest
wall clock time among top performers.

## Dataset

Algerian Forest Fire Dataset, UCI Machine Learning Repository.
Features: Temperature, Relative Humidity, Wind Speed, Rain.

## Tools and Technologies

Python, Scikit-learn, Pandas, NumPy, Matplotlib, Seaborn, imbalanced-learn (SMOTE)

## Project Code
https://github.com/TheMlengineer-py/Forest-Fire-Detection-ML-System

## Citation

If you reference this work, please cite:
Oyeyemi, D.T. (2022). *Forest Fire Detection Using Artificial Intelligence
Solutions*. MSc Thesis, University of Hull.
