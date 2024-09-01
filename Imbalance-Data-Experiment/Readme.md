
# Imbalance Data Experiment

This project focuses on handling imbalanced datasets using various resampling techniques and machine learning models. The goal is to improve the detection of minority class instances while maintaining a balance between precision and recall.

## Table of Contents
1. [Data Import and Initial Exploration](#data-import-and-initial-exploration)
2. [Data Cleaning and Preprocessing](#data-cleaning-and-preprocessing)
3. [Feature Engineering](#feature-engineering)
4. [Model Training and Evaluation](#model-training-and-evaluation)
5. [Model Evaluation](#model-evaluation)
6. [Results and Recommendations](#results-and-recommendations)
7. [Key Takeaways](#key-takeaways)
8. [Final Comments](#final-comments)

## Data Import and Initial Exploration
- **Libraries Imported**: Various libraries such as `pandas`, `numpy`, `matplotlib`, `seaborn`, and several `sklearn` modules were imported.
- **Data Loading**: The dataset was loaded from a CSV file named `data.csv`.
- **Initial Data Exploration**: The first few rows of the dataset were displayed to understand its structure.

## Data Cleaning and Preprocessing
- **Missing Values Check**: The dataset was checked for missing values.
- **Handling Missing Values**: Missing values in the `elevation` and `vegetationindex` columns were filled with their respective medians, while missing values in the `landcovertype` column were filled with the mode.

## Feature Engineering
- **Label Encoding**: Categorical variables were encoded using `LabelEncoder`.
- **Feature Scaling**: Features were scaled using `StandardScaler`.

## Model Training and Evaluation
- **Train-Test Split**: The dataset was split into training and testing sets.
- **Model Selection**: Various models such as `RandomForestClassifier`, `GradientBoostingClassifier`, `AdaBoostClassifier`, and `SVC` were selected for training.
- **Resampling Techniques**: Different resampling techniques like `SMOTE`, `ADASYN`, `BorderlineSMOTE`, and `SVMSMOTE` were applied to handle class imbalance.
- **Pipeline Creation**: Pipelines were created to streamline the process of resampling, scaling, and model training.
- **Grid Search**: Hyperparameter tuning was performed using `GridSearchCV`.

## Model Evaluation
- **Evaluation Metrics**: Models were evaluated using metrics such as `accuracy_score`, `roc_auc_score`, `confusion_matrix`, `precision_score`, `recall_score`, and `f1_score`.
- **Threshold Tuning**: The decision threshold was tuned to balance precision and recall, with strategies to maximize F1 Score and Recall.
- **Best Models**: The best models and their respective thresholds were identified and stored.

## Results and Recommendations
- **Model Performance**: The performance of models with and without resampling, and with tweaked thresholds, was compared.
- **Recommended Model**: Gradient Boosting with ADASYN (Maximize Recall) was recommended as the best model for detecting the minority class instances.
- **Future Work**: Suggestions for further improvements included feature engineering, additional data collection, advanced hyperparameter tuning, hybrid resampling methods, and experimenting with more ensemble and tree-based models.

## Key Takeaways
- **Without Resampling**: High precision and specificity but low recall.
- **With Resampling**: Improved recall but at the cost of precision.
- **With Resampling and Tweaked Thresholds**: Best balance of high recall and precision, maintaining a strong F1 score and ROC AUC.

## Final Comments
- **Feature Engineering**: Create new features and analyze the importance of existing features.
- **Additional Data**: Collect more data to improve the model.
- **Hyperparameter Tuning**: Focus on Bayesian optimization.
- **Hybrid Resampling Methods**: Combine over-sampling and under-sampling techniques.
- **Experiment with More Models**: Try more ensemble and tree-based models.


#### Proposed Deployment Architecture
![Architecture Diagram](proposedArchitecture.png)



