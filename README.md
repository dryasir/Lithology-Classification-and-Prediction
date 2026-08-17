# Learning Across Wells: A Robust Framework for Lithology Classification and Prediction 

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

# Hardware requirements: 
        Intel(R) Xeon(R) CPU E5-2678 v3 @ 2.50 GHz and an NVIDIA GeForce GTX 1080 Ti GPU. 
# Programming language: 
        Python
# Software required: 
        Anaconda, Jupyter Notebook
# Program size: 
        5 Gigabytes 


# Objectives of the Study

The primary objective of this study is to develop and evaluate a robust machine learning framework for multi-well lithology classification and prediction using wireline-log data. The specific objectives are to:

* Develop an automated lithology classification workflow using commonly available wireline-log measurements, including gamma ray (GR), bulk density (RHOB), corrected sonic transit time (DT_CORR), and effective porosity (PHIE).
* Evaluate and compare two supervised machine learning classifiers, Random Forest (RF) and K-Nearest Neighbors (KNN), for multi-class lithology prediction involving Shale, Sandstone, Tight Sand, and Carbonate.
* Assess inter-well generalization capability by training the models on multiple wells and evaluating their performance on previously unseen wells through blind-well testing.
* Implement Leave-One-Well-Out (LOWO) cross-validation to provide a rigorous assessment of model robustness and generalization across different wells.
* Optimize the model hyperparameters using stratified five-fold cross-validation and identify suitable configurations for KNN and Random Forest classifiers.
* Determine the relative importance of the input wireline-log features and investigate which petrophysical measurements contribute most strongly to lithology discrimination.
* Evaluate model agreement and prediction confidence between Random Forest and KNN, particularly for samples where the two classifiers produce different predictions.
* Investigate the robustness of machine learning models to inter-well log variability, with particular emphasis on the performance advantage of ensemble-based Random Forest compared with the distance-based KNN approach.
* Identify the limitations associated with lithology labels derived without core-calibrated ground truth or standardized petrophysical cut-offs, and discuss their implications for supervised machine learning.
* Provide a reproducible framework for future lithology prediction studies and identify potential improvements, including the integration of resistivity logs, ensemble boosting methods, and core-calibrated lithology labels.

# Contact

We welcome feedback, questions, suggestions, and discussions related to the use and further development of this repository. If you use this code in your research or have ideas for improving the workflow, please feel free to contact the author.

Author and Technical Contact:
# _Dr. Yasir Bashir_
Department of Geophysics
Istanbul Technical University (ITU), Türkiye
Email: ybashir@itu.edu.tr, dryasir.bashir@live.com

For questions related to the implementation, machine learning workflow, lithology classification, well-log processing, or reproducibility of the results presented in the paper, please contact Dr. Yasir Bashir.
