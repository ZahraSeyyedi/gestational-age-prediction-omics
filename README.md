# gestational-age-prediction-omics
This repository contains a machine learning project that focuses on the **prediction of gestational age during pregnancy** using **multiomics biomarkers**.

### Technologies Used:
- **Python**: the main programming language for data processing and model building  
- **Scikit-learn**: used for implementing the ElasticNet regression model and performing cross-validation  
- **Pandas / NumPy**: for dataset handling and preprocessing  
- **Matplotlib / Seaborn**: for visualization and analysis  

### Dataset:
This project is based on the study by *Ghaemi et al. (2019)*:  
*"Multiomics modeling of the immunome, transcriptome, microbiome, proteome and metabolome adaptations during human pregnancy"*.  

- The dataset consists of longitudinal biological samples from pregnant women.  
- **Features (X):** multiomics biomarkers including immunome, transcriptome, microbiome, proteome, and metabolome.  
- **Target (y):** gestational age (in weeks).
- An ElasticNet regression model was designed and trained.
ElasticNet combines L1 (Lasso) and L2 (Ridge) penalties to handle high-dimensional data and correlated features.

Best hyperparameters found via GridSearch:

α = 1, l1_ratio = 0.9, max_iter = 1000
The model was trained and evaluated using 5-fold cross-validation.

Results:
R² scores ranged from -0.05 to 0.70, with a mean of ≈ 0.39 (explains ~39% of variance)
MAE ≈ 7.8

RMSE ≈ 9.3

Spearman correlation (ρ) = 0.545, p < 0.001 → moderate positive correlation
