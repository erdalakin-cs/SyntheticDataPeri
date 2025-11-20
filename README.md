# Synthetic Data as a Tool for Prototyping Early-Stage Periodontitis Detection Models

This repository has two notebooks that can be reused for reproducing and evaluation:

# 1. Data_Generation.ipynb

  Create an initial dataset of 800 samples based on expert-defined biomarker ranges from previous literature.
  
  A Tabular Variation Autoencoder (TVAE) was trained on the initial dataset to synthetically extend it to 4000 data points.
  
# 2. ML-generation.ipynb

  # applying ML models to the generated dataset by evaluating their effectiveness:

    • XGBoost: Bayesian Optimization was used to fine-tune hyperparameters, resulting in optimal values of learning rate: 0.13, max depth: 1, and n estimators: 387.
    • KNN: For optimal performance, Grid Search was used with parameters such as algorithm: auto, metric: manhattan, n neighbors: 15, and weight: uniform.
    • SVM: Optimal hyperparameters were determined using Grid Search: C: 1, gamma: auto, and kernel: rbf.
    • LR: Grid Search was employed once again for tuning, resulting in the best values being C:10, penalty: l1, and solver: liblinear.
    • RF: The best parameters were determined using Grid Search, yielding: criterion: entropy, max depth: 10, min samples leaf: 1, min samples split: 2, and n estimators: 200.
    • DNN: The sequential model was tuned using Random Search. Optimal parameters were:units: 128, dropout: 0.4, and learning rate: 0.001.


# TO-DO:
  -Creating a user-friendly environment for parameter tuning.
