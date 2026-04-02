This repository contains the code and methodological framework used to develop supervised machine learning models for sex estimation based on morphometric measurements of root canals from first molars obtained through cone-beam computed tomography (CBCT).

## Overview

Human identification in forensic contexts often relies on biological structures resistant to degradation. Dental tissues, particularly root structures, provide stable morphometric features that can support sex estimation. This project explores the use of internal dental anatomy combined with machine learning algorithms to identify patterns associated with sexual dimorphism.

The approach focuses on extracting linear morphometric measurements from CBCT images and applying multiple classification algorithms to model the relationship between anatomical features and sex.

## Study Design

- Retrospective cross-sectional design  
- CBCT-based morphometric analysis  
- Dataset composed of first molars from multiple individuals  
- Measurements obtained from sagittal and axial reconstructions  
- Standardized alignment along the long axis of the root  

All data were previously anonymized, and the study followed ethical guidelines for research involving human data :contentReference[oaicite:0]{index=0}.

## Features

The models were trained using morphometric variables derived from root canal anatomy, including:

- Distance from root apex to cementoenamel junction (CEJ)
- Measurements across different root canals (e.g., mesiobuccal, distobuccal, palatal)
- Dentin thickness (mesial and distal)
- Presence of anatomical variations (e.g., second mesiobuccal canal)
- Dental arch classification (maxilla or mandible)

These features were selected to capture both structural and contextual anatomical information.

## Machine Learning Models

The following supervised classification algorithms were implemented:

- Logistic Regression  
- Support Vector Machine (SVM)  
- K-Nearest Neighbors (KNN)  
- Decision Tree  
- Random Forest  
- Gradient Boosting  
- AdaBoost  
- Multilayer Perceptron (MLP)  

This combination allows comparison between interpretable linear models and more complex nonlinear approaches.

## Model Development Pipeline

The modeling process followed a structured pipeline:

1. **Data splitting**
   - 70% training set  
   - 30% independent test set  

2. **Cross-validation**
   - 5-fold cross-validation applied to the training data  

3. **Class imbalance handling**
   - Synthetic Minority Oversampling Technique (SMOTE) applied only to the training set  

4. **Hyperparameter optimization**
   - Grid Search used to identify optimal model configurations  

5. **Overfitting control**
   - Combination of cross-validation, SMOTE, and hyperparameter tuning to improve generalization  

## Evaluation Metrics

Model performance was assessed using multiple complementary metrics:

- Area Under the ROC Curve (AUC)  
- Accuracy  
- Precision  
- Recall (Sensitivity)  
- F1-score  

To ensure statistical robustness, 95% confidence intervals were estimated using bootstrap resampling (1,000 iterations).

## Feature Importance

For models that support interpretability (e.g., tree-based methods), feature importance analysis was conducted to identify the most relevant morphometric predictors contributing to sex estimation.

## Reproducibility

- Programming language: Python (v3.10.12)  
- Environment: Google Colab  
- Libraries: scikit-learn, imbalanced-learn, NumPy, pandas  

The full code and metadata are available via DOI:
https://doi.org/10.5281/zenodo.12945492

## Applications

This framework can be applied in:

- Forensic identification  
- Anthropological research  
- Dental morphometric analysis  
- Automated decision-support systems  

## Limitations

- Single-center dataset  
- Retrospective design  
- Lack of external validation  
- Restricted set of morphometric variables  

Future studies should include multicenter datasets, external validation, and additional anatomical features to improve model generalizability.

## License

This project is intended for academic and research purposes.
