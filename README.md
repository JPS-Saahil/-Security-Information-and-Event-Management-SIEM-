# 📄 Security Information and Event Management (SIEM)

## Abstract
This project focuses on the development and evaluation of machine learning models aimed at classifying the legitimacy of software applications based on their static attributes. The primary objective is to enhance cybersecurity defenses by leveraging static analysis combined with machine learning techniques to detect potential malware while maintaining a low false positive rate and high detection accuracy. The classification models implemented include Random Forest, K-Nearest Neighbors (KNN), and XGBoost, which have been compared to determine the most effective approach.

## Key Features
- **Static Malware Analysis**: Malware detection is performed without executing files.
- **Machine Learning-based Classification**: Utilizes Random Forest, KNN, and XGBoost models for classification tasks.
- **Dimensionality Reduction**: Implements Principal Component Analysis (PCA) to reduce the feature space while retaining maximum variance.
- **Cross-Validation**: 15-Fold Cross-Validation is employed to ensure robust and generalizable model performance.
- **Visualization**: Interactive visualizations of feature space, variance, and model performance using Plotly and Matplotlib.
- **Performance Metrics**: Evaluation of models using Accuracy, Precision, Recall, F1-Score, and ROC-AUC.

## Technologies Used
- **Programming Language**: Python 3.10+
- **Libraries**: 
  - scikit-learn
  - XGBoost
  - Pandas
  - NumPy
  - Matplotlib
  - Plotly
- **Hardware**:
  - AMD Ryzen 5700U
  - Intel i7 11th/12th Gen
  - NVIDIA RTX 3050/4060 GPUs

## Dataset
The dataset is collected from various malware repositories, including VirusTotal. The following features are used for analysis:
- **Name**: Application identifier.
- **MD5**: Hash for integrity verification.
- **SizeOfCode**: Size of the executable code.
- **Legitimate**: Binary classification label indicating whether the software is legitimate or malicious.
  <p align="center">
  <img src="https://github.com/JPS-Saahil/-Security-Information-and-Event-Management-SIEM-/blob/master/Assets/Screenshot%202025-04-26%20065833.png" width="700" />
</p>

## Project Workflow

### 1. Data Preprocessing
- **Duplicate Removal**: Eliminating redundant data entries.
- **Missing Value Imputation**: Handling missing values in the dataset.
- **One-Hot Encoding**: Encoding categorical variables.
- **Feature Standardization & Normalization**: Ensuring numerical features are on the same scale.

### 2. Feature Selection
- **Extra Trees Classifier**: Used to identify the most significant features contributing to classification.

### 3. Model Training
- **Random Forest Classifier**
- **K-Nearest Neighbors (KNN)**
- **XGBoost Classifier**

### 4. Dimensionality Reduction
- **Principal Component Analysis (PCA)**: Reduces the feature space while retaining maximum variance for model efficiency.
  <p align="center">
  <img src="https://github.com/JPS-Saahil/-Security-Information-and-Event-Management-SIEM-/blob/master/Assets/PCA.png" width="700" />
  </p>
  <p align="center">
  <img src="https://github.com/JPS-Saahil/-Security-Information-and-Event-Management-SIEM-/blob/master/Assets/PCA%20_COMPONENTS.png" width="700" />
  </p>

### 5. Model Evaluation
- **Performance Metrics**: Accuracy, Precision, Recall, F1-Score, ROC-AUC.
- **Cross-Validation**: 15-Fold Cross-Validation to ensure model robustness.
<p align="center">
  <img src="https://github.com/JPS-Saahil/-Security-Information-and-Event-Management-SIEM-/blob/master/Assets/performance.png" width="700" />
</p>

### 6. Visualization
- **2D/3D Scatter Plots**: Visualizing PCA-reduced feature space.
- **Explained Variance Ratio Plot**: Visualizing the contribution of each principal component.
- **ROC Curve Analysis**: Evaluating model performance across various thresholds.

## Results
- **Random Forest**: Achieved the highest classification accuracy.
  - **Accuracy**: 99.84%
  - **F1-Score**: 99.70%
- **XGBoost**: Close performance to Random Forest.
  - **Accuracy**: 98.50%
  - **F1-Score**: 97.60%
- **K-Nearest Neighbors (KNN)**: Showed reasonable results, but was less effective compared to the other models.
  - **Accuracy**: 93.80%
  - **F1-Score**: 92.10%
- **PCA**: Significantly improved model efficiency and clarity of data patterns.
- **Cross-Validation**: Demonstrated model robustness and generalization capability.
- **AUC-ROC**: Curve for model comparision.
  <p align="center">
  <img src="https://github.com/JPS-Saahil/-Security-Information-and-Event-Management-SIEM-/blob/master/Assets/AUC_ROC.png" width="700" />
  </p>

## System Design Overview
<p align="center">
  <img src="https://github.com/JPS-Saahil/-Security-Information-and-Event-Management-SIEM-/blob/master/Assets/Screenshot%202025-04-26%20071243.png" width="700" />
  </p>

### Input
- Static attributes of software applications, such as name, size, and MD5 hash.

### Preprocessing
- Encoding, scaling, and cleaning of features.

### Training
- Application of machine learning classifiers (Random Forest, KNN, XGBoost).

### Dimensionality Reduction
- PCA to retain maximum variance with fewer dimensions.

### Prediction
- Classification of software as legitimate or malicious.

### Visualization
- Static and interactive graphs to support data analysis and model evaluation.

## Conclusion
This project demonstrates the effective use of static analysis combined with machine learning models to distinguish between legitimate and malicious software applications. The use of PCA and robust validation practices significantly enhanced both model accuracy and computational efficiency, offering a promising pathway for real-world malware detection systems.

## Future Scope
- **GUI Development**: Building a graphical user interface (GUI) for broader usability.
- **Real-Time Threat Detection**: Integration with network security systems to enable real-time malware detection.
- **Cross-Platform Compatibility**: Porting the tool to Linux to extend its compatibility.
- **Sequence-Based Malware Scanning**: Implementing sequence-based methods to detect evolving threat patterns.
- **Continuous Model Enhancement**: Enhancing the model through hyperparameter tuning and incorporating external threat intelligence sources.

## Credits
- **JPS Saahil jpssaahil203@outlook.com**
- **Jatin Pathak sonic.zeus1@gmail.com**
