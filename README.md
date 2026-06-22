# Security Information and Event Management (SIEM)

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-yellow)
![XGBoost](https://img.shields.io/badge/XGBoost-Gradient%20Boosting-green)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

## Overview

This repository presents a static malware analysis system for classifying software applications as legitimate or malicious using machine learning. The approach relies on file attributes that can be extracted without executing the sample, which makes it suitable for early-stage screening and large-scale analysis. The project evaluates Random Forest, K-Nearest Neighbors, and XGBoost to identify the most effective classifier for this task.

## Abstract

The objective of this project is to improve malware detection by combining static feature analysis with supervised machine learning. The pipeline is designed to support strong classification performance while reducing false positives and preserving computational efficiency. Model comparison is performed using standard evaluation metrics and cross-validation to support reliable performance assessment.

## Key Features

| Capability | Description |
|---|---|
| Static Malware Analysis | Classifies files without executing them |
| Machine Learning Classification | Uses Random Forest, KNN, and XGBoost |
| Feature Selection | Applies Extra Trees Classifier to identify important variables |
| Dimensionality Reduction | Uses PCA to reduce feature space while preserving variance |
| Cross Validation | Uses 15-fold cross-validation for robust evaluation |
| Visualization | Produces plots with Matplotlib and Plotly |
| Performance Metrics | Reports Accuracy, Precision, Recall, F1-Score, and ROC AUC |

## Technologies Used

The project is implemented in Python 3.10+ and uses the following libraries and tools: scikit-learn, XGBoost, Pandas, NumPy, Matplotlib, and Plotly. The models were developed and tested on common desktop and laptop hardware configurations, including AMD Ryzen 5700U, Intel i7 11th and 12th generation processors, and NVIDIA RTX 3050 or RTX 4060 GPUs.

## Dataset

The dataset is assembled from malware repositories, including VirusTotal. The following fields are used for analysis.

| Feature | Description |
|---|---|
| Name | Application identifier |
| MD5 | Hash used for integrity verification |
| SizeOfCode | Size of the executable code |
| Legitimate | Binary label indicating whether the software is legitimate or malicious |

The repository also includes visual summaries of the dataset and model outputs.

## Project Workflow
<p align="center">
  <img src="https://github.com/JPS-Saahil/-Security-Information-and-Event-Management-SIEM-/blob/master/Assets/Screenshot%202025-04-26%20071243.png" width="700" />
</p>

### Data Preprocessing

The preprocessing stage removes duplicate records, handles missing values, applies one hot encoding to categorical variables, and standardizes numerical features to a common scale.

### Feature Selection

An Extra Trees Classifier is used to rank variables according to their contribution to the classification task.

<p align="center">
  <img src="https://github.com/JPS-Saahil/-Security-Information-and-Event-Management-SIEM-/blob/master/Assets/Screenshot%202025-04-26%20065833.png" width="700" />
</p>

### Model Training

Three classifiers are trained and compared: Random Forest, KNN, and XGBoost.

### Dimensionality Reduction

Principal Component Analysis is used to compress the feature space while retaining the maximum practical amount of variance.

<p align="center">
  <img src="https://github.com/JPS-Saahil/-Security-Information-and-Event-Management-SIEM-/blob/master/Assets%2FPCA.png" width="700" />
</p>

### Model Evaluation

Performance is assessed using Accuracy, Precision, Recall, F1-Score, ROC AUC, and 15-fold cross-validation.

<p align="center">
  <img src="https://github.com/JPS-Saahil/-Security-Information-and-Event-Management-SIEM-/blob/master/Assets/performance.png" width="700" />
</p>

### Visualization

The project includes 2D and 3D scatter plots, explained variance plots, and ROC curve analysis to support interpretation of the results.

## Results

| Model | Accuracy | F1-Score |
|---|---:|---:|
| Random Forest | 99.84% | 99.70% |
| XGBoost | 98.50% | 97.60% |
| K-Nearest Neighbors | 93.80% | 92.10% |

Random Forest delivered the strongest performance in this study. XGBoost followed closely, while KNN produced lower but still reasonable results. PCA improved both interpretability and computational efficiency. Cross-validation indicated that the models generalize well within the scope of the dataset.

## Visualization

The project includes the following visual outputs to support interpretation of the data and the model results.

### Feature Space Visualization

2D and 3D scatter plots are used to visualize the PCA-reduced feature space. These plots help illustrate the separation between legitimate and malicious samples after dimensionality reduction

<p align="center">
  <img src="https://github.com/JPS-Saahil/-Security-Information-and-Event-Management-SIEM-/blob/master/Assets/PCA%20_COMPONENTS.png" width="700" />
</p>.

### Explained Variance Ratio

An explained variance ratio plot is used to show how much information is retained by each principal component. This helps assess the effectiveness of PCA in reducing dimensionality while preserving structure in the data.

### Model Performance Visualization

ROC curve analysis is used to compare model performance across classification thresholds. This provides a clearer view of the trade-off between true positive rate and false positive rate for each classifier.

<p align="center">
  <img src="https://github.com/JPS-Saahil/-Security-Information-and-Event-Management-SIEM-/blob/master/Assets/AUC_ROC.png" width="700" />
</p>


## System Design Overview

The system accepts static application attributes as input. These values are cleaned, encoded, and scaled during preprocessing. Feature selection reduces the dimensionality of the original data, after which the models are trained and evaluated. PCA supports the reduction of high dimensional input into a more compact form. The final output is a classification decision indicating whether the sample is legitimate or malicious. Visualization modules provide plots to support analysis and interpretation.

## Conclusion

This project demonstrates that static analysis combined with supervised machine learning can be used to distinguish between legitimate and malicious software with high accuracy. The use of feature selection, PCA, and cross-validation strengthens the reliability of the results and supports the development of practical malware screening systems.

## Future Scope

Future work may include a graphical user interface, real time threat detection, Linux support, sequence based malware scanning, and continuous improvement through hyperparameter tuning and external threat intelligence.

## Credits

JPS Saahil, jpssaahil2003@outlook.com

Jatin Pathak, sonic.zeus1@gmail.com
