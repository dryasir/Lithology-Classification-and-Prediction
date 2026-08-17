# Learning Across Wells: A Robust Framework for Lithology Classification and Prediction 

Yasir Bashir*, Zoonash Arshad, Hülya Kurt, Caner İmren, Muhsan Ehsan

# What is this repository for?

This repository provides a machine learning framework for automated lithology classification and prediction from wireline-log data. It implements Random Forest (RF) and K-Nearest Neighbors (KNN) classifiers using shared petrophysical well-log measurements, including gamma ray (GR), bulk density (RHOB), corrected sonic transit time (DT_CORR), and effective porosity (PHIE).

The framework focuses on inter-well generalization, using Leave-One-Well-Out (LOWO) cross-validation and blind-well testing to evaluate the robustness of lithology prediction across previously unseen wells. The repository also provides the workflow for model training, hyperparameter optimization, performance evaluation, feature-importance analysis, and prediction-confidence assessment.

The code and workflows are designed to support reproducible machine learning–based lithology classification and provide a foundation for extending the approach to additional wells, petrophysical logs, and more advanced ensemble learning methods.

# Source Code

1. RF_vs_KNN_MultiWell_Lithology.ipynb

This Jupyter Notebook contains the complete source code for the study, covering the workflow from initial data loading and preprocessing to lithology classification, model training, validation, evaluation, and visualization.

The notebook uses well-log and seismic data for implementation and reproduces the complete methodology presented in the paper, including:

* Initial data loading and quality control
* Well-log preprocessing and preparation
* Feature selection and data organization
* Lithology classification using Random Forest (RF) and K-Nearest Neighbors (KNN)
* Hyperparameter optimization
* Blind-well testing
* Leave-One-Well-Out (LOWO) cross-validation
* Model performance evaluation
* Feature-importance analysis
* Prediction-confidence and model-agreement analysis
* Generation of figures and results reported in the manuscript

The entire processing and machine learning workflow is provided in a single Jupyter Notebook to facilitate reproducibility and allow users to follow the analysis sequentially from the raw input data through to the final results.


# Overview of Paper

Subsurface characterization relies on wireline-log lithology classification for volumetric calculations, completion design, and reservoir delineation. Manual log interpretation is time-consuming and biased; therefore, supervised machine learning is replacing it for automated facies and lithology prediction. We evaluate two widely supervised classifiers, Random Forest (RF) and K-Nearest Neighbors (KNN), for multi-well lithology prediction. Gamma ray (GR), bulk density (RHOB), corrected sonic transit time (DT_CORR), and effective porosity (PHIE) are the four shared wireline curves for the four genuine North Sea wells F02-01, F03-02, F03-04, and F06-01. Without core-calibrated ground truth and regular petrophysical cut-offs, lithology names were Shale, Sandstone, Tight Sand, and Carbonate. Validation methods included training on three wells and blind testing on a fourth, unknown well (F06-01). First, a Leave-One-Well-Out (LOWO) cross-validation across all four wells tested inter-well generalization more rigorously. We selected four KNN neighbors and twenty-five Random Forest estimators using stratified five-fold cross-validation to fine-tune the model's hyperparameters. Random Forest scored 100.0% (weighted F1 = 1.000) and KNN 98.45% on the blind test. Random Forest averaged 99.58% and KNN 97.10% on all four held-out wells for the whole LOWO assessment. The strongest distinguishing curves were gamma ray (GR, significance 0.434), bulk density (RHOB, 0.333), and effective porosity (PHIE, 0.221). Sonic transit time correction (DT_CORR, 0.012) was hardly significant. In 98.4% of blind-well samples, the two classifiers agreed, but prediction-confidence analysis showed that Random Forest was accurate in all disagreements. Due to its bagged, feature-randomized ensemble structure, Random Forest beats the distance-based KNN classifier in inter-well log variability resilience even without feature scaling. We highlight the limitations of rule-based labeling without core data, review machine learning literature for lithology and facies classification, and propose resistivity logs, ensemble boosting, and core-calibrated labels for further research.
