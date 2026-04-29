# Alzheimer Classification Using Machine Learning: A Comparative Analysis of Optimization Strategies

## Overview
This project investigates the use of Machine Learning techniques for the classification of Alzheimer’s disease, with a focus on comparing different nonlinear optimization strategies applied to predictive models. The study replicates and extends previous research by evaluating how optimization methods impact model performance in medical diagnosis tasks.

The project was developed as part of the Bachelor's Degree in Data Science and Artificial Intelligence at the Federal University of Paraíba (UFPB), within the course of Nonlinear Optimization.

## Authors
- Julia Gabriele Mendes Barbosa  
- Matheus Bruno da Silva Oliveira  
- Micael Oliveira Lima Toscano  
- Sérgio Cauã dos Santos  

**Institution:** Federal University of Paraíba (UFPB) – Center for Informatics  
**Year:** 2026  

## Motivation
Alzheimer’s disease is a progressive neurodegenerative disorder that affects memory, cognition, and daily functioning. Early diagnosis is challenging because initial symptoms are often confused with normal aging. This project explores how Machine Learning models can assist in distinguishing early-stage Alzheimer’s from typical cognitive decline.

## Objectives

### General Objective
- Replicate prior experiments to identify the best-performing Machine Learning models for Alzheimer’s classification and evaluate the impact of nonlinear optimization methods.

### Specific Objectives
- Preprocess and integrate OASIS-1 and OASIS-2 datasets  
- Implement baseline models: Random Forest, AdaBoost, SVM, KNN, and Logistic Regression  
- Evaluate models using accuracy, precision, recall, and F1-score  
- Apply nonlinear optimization methods such as Conjugate Gradient, Newton-CG, and BFGS  
- Compare performance before and after optimization  

## Dataset
The study uses data from the **OASIS (Open Access Series of Imaging Studies)**:
- **OASIS-1 (cross-sectional):** 436 records, 12 features  
- **OASIS-2 (longitudinal):** 373 records, 15 features  

After merging and preprocessing:
- 373 records and 13 relevant features remained  

## Methodology

### Data Preprocessing
- Removal of columns with more than 60% missing values  
- Imputation of missing data using KNN Imputer  
- Creation of binary target variable (`group`):  
  - 1 → Alzheimer’s diagnosis  
  - 0 → No diagnosis  
- Dimensionality reduction using PCA  
- Feature scaling and normalization  
- Train/test split: 80% / 20%  

### Machine Learning Models
- Random Forest (RF)  
- AdaBoost  
- Support Vector Machine (SVM)  
- K-Nearest Neighbors (KNN)  
- Logistic Regression (LR)  

### Optimization Techniques
Applied to Logistic Regression, SVM, and AdaBoost:
- Conjugate Gradient (CG)  
- Newton-CG  
- BFGS (Quasi-Newton)  
- L-BFGS-B  
- Additional solvers: Liblinear, SAG, SAGA  

### Evaluation Metrics
- Accuracy  
- Precision  
- Recall  
- F1-Score  

## Results

| Model                | Accuracy |
|---------------------|----------|
| Logistic Regression | 97%      |
| Random Forest       | 96%      |
| SVM                 | 96%      |
| AdaBoost            | 91%      |
| KNN                 | 92%      |

- Logistic Regression achieved the best overall performance  
- Random Forest and SVM showed strong and consistent results  
- Optimization methods did not significantly improve SVM and Logistic Regression, indicating near-optimal convergence  
- AdaBoost performance decreased (~5%) after optimization, likely due to the discrete nature of decision trees  

## Conclusion
The results confirm that Machine Learning models, particularly Logistic Regression, SVM, and Random Forest, are effective tools for Alzheimer’s classification using OASIS datasets.

The application of nonlinear optimization methods demonstrated that:
- Some models already operate close to optimal solutions with standard implementations  
- Gradient-based optimization is not always suitable for tree-based models like AdaBoost  

This study highlights both the strengths and limitations of optimization techniques in medical Machine Learning applications.

## Technologies Used
- Python  
- Scikit-learn  
- NumPy  
- Pandas  
- SciPy  

## References
- Biau, G. (2010). Analysis of a Random Forests model  
- Boateng, E. Y.; Abaye, D. A. (2019). Logistic Regression in medical research  
- Bansal, M.; Goyal, A.; Choudhary, A. (2022). Comparative ML analysis  
- Tyralis, H.; Papacharalampous, G. (2021). Boosting algorithms review  
- OASIS Brain Datasets  
- SciPy, NumPy, Pandas, Scikit-learn documentation  

## License
This project is intended for academic and research purposes.
