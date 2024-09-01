# Imbalanced Data Experiment - Modelling

## Overview
This project explores the challenge of handling imbalanced datasets in a classification task. The primary focus is on applying different resampling techniques and evaluating various models to improve the performance of predicting the presence of a particular species.

## Dataset
The dataset used in this project contains the following features:
- **species**: The species under observation.
- **elevation**: The elevation at which the species is found.
- **landcovertype**: The type of land cover where the species is found.
- **vegetationindex**: A numerical index representing vegetation.
- **presence**: The target variable indicating the presence (1) or absence (0) of the species.

## Preprocessing Steps
### Missing Values Handling
- Missing values were found in the `elevation`, `landcovertype`, and `vegetationindex` columns.
- Missing values were filled using the median for numerical columns and mode for categorical columns.

### Outlier Detection and Removal
- Outliers were identified in `elevation` and `vegetationindex` using the Interquartile Range (IQR) method.
- Outliers were removed to ensure better model performance.

### Feature Engineering
- Interaction features were created, such as `elevation_vegetationindex`.
- Features were standardized using `StandardScaler`.

### Label Encoding
- Categorical features like `landcovertype` were label encoded.

### Correlation Analysis
- A heatmap was generated to identify the correlation between features and the target variable.

## Model Training and Evaluation
### Without Resampling
Three tree-based models were selected due to their ability to handle imbalanced datasets:
- **Random Forest**
- **Gradient Boosting**
- **AdaBoost**

Hyperparameters were optimized using `GridSearchCV`. The performance of these models was evaluated using metrics like Precision, F1 Score, ROC AUC, Sensitivity, and Specificity.

### With Resampling
Given the class imbalance, the following resampling techniques were applied:
- **SMOTE**
- **ADASYN**
- **BorderlineSMOTE**
- **SVMSMOTE**

These methods were used in conjunction with the tree-based models to improve sensitivity, especially for the minority class.

## Results
- **Without Resampling**: Random Forest performed best but showed lower sensitivity.
- **With Resampling**: Gradient Boosting with SVMSMOTE provided the best balance between sensitivity and overall performance, making it the preferred model.

## Optimization
To further improve the model, decision thresholds were adjusted to maximize either the F1 Score or Recall, depending on the application requirements.

## Conclusion
This project demonstrates the importance of handling imbalanced datasets, particularly in ecological studies where missing critical predictions could have significant consequences. The best model was selected based on its ability to generalize well to the minority class, ensuring that important ecological insights are not missed.

#### Proposed Deployment Architecture
![Architecture Diagram](proposedArchitecture.png)
