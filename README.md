📄 Security Information and Event Management (SIEM)
Abstract
This project focuses on the development and evaluation of machine learning models for classifying the legitimacy of software applications based on their static attributes.
The primary objective is to enhance cybersecurity defenses by leveraging static analysis and machine learning methodologies to detect potential malware, while maintaining a low false positive rate and high detection accuracy.
Classification models such as Random Forest, K-Nearest Neighbors (KNN), and XGBoost have been implemented and compared to identify the most effective approach.

Key Features
Static Malware Analysis without executing files.

Machine Learning-based Classification (Random Forest, KNN, XGBoost).

Dimensionality Reduction through Principal Component Analysis (PCA).

Cross-Validation (15-Fold) to ensure robust and generalizable models.

Visualization of feature space, variance, and model performance using Plotly and Matplotlib.

Performance Metrics: Accuracy, Precision, Recall, F1-Score, ROC-AUC.

Technologies Used
Python 3.10+

Libraries:
scikit-learn, XGBoost, Pandas, NumPy, Matplotlib, Plotly

Hardware Used:
AMD Ryzen 5700U, Intel i7 11th/12th Gen, NVIDIA RTX 3050/4060 GPUs.

Dataset
Collected from malware repositories such as VirusTotal.

Features used:

Name (application identifier)

MD5 (hash for integrity verification)

SizeOfCode

Legitimate (binary classification label)

Project Workflow
Data Preprocessing

Duplicate removal, missing value imputation.

One-Hot Encoding for categorical features.

Standardization and normalization of numerical features.

Feature Selection

Using Extra Trees Classifier for identifying significant features.

Model Training

Random Forest Classifier

K-Nearest Neighbors (KNN)

XGBoost Classifier

Dimensionality Reduction

Principal Component Analysis (PCA) to retain maximum variance with fewer dimensions.

Model Evaluation

Metrics: Accuracy, Precision, Recall, F1-Score, ROC-AUC.

15-Fold Cross-Validation.

Visualization

2D/3D Scatter plots of PCA-reduced features.

Explained Variance Ratio plot.

ROC Curve analysis.

Results
Random Forest achieved the highest classification accuracy.

XGBoost closely followed in performance.

KNN displayed reasonable results but was relatively less effective.

PCA significantly improved model efficiency and clarity of data patterns.

Cross-validation demonstrated model robustness and generalization capability.

Performance Highlights:


Model	Accuracy (%)	F1-Score (%)
Random Forest	99.84	99.70
XGBoost	98.50	97.60
K-Nearest Neighbors (KNN)	93.80	92.10
System Design Overview
Input: Static attributes of software applications (size, name, MD5 hash).

Preprocessing: Encoding, scaling, cleaning.

Training: Application of machine learning models.

Dimensionality Reduction: PCA.

Prediction: Software classified as legitimate or malicious.

Visualization: Interactive and static graphs to support analysis.

Conclusion
The project successfully demonstrates that static analysis combined with machine learning models can effectively distinguish between malicious and legitimate software.
The use of PCA and robust validation practices greatly enhanced model accuracy and computational efficiency, offering a promising pathway towards real-world malware detection systems.

Future Scope
Development of a Graphical User Interface (GUI) for wider usability.

Integration with Network Security Systems for real-time threat detection.

Sequence-based malware scanning for detecting evolving threat patterns.

Linux porting to extend cross-platform compatibility.

Continuous model enhancement through hyperparameter tuning and external threat intelligence integration.

Credits
Team Members:

JPS Saahil (21052423)

Aditya Pandey (21052471)

Jatin Pathak (21052422)
