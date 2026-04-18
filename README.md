# Diagnosis Predictor
This project develops machine learning models to predict patient diagnoses such as Sepsis, Pneumonia, and Heart Failure using clinical features including age, BMI, blood pressure, glucose levels, and medical history indicators. The goal is not just to maximize accuracy, but to improve detection of critical conditions using appropriate evaluation metrics for imbalanced healthcare data.

## Dataset source
https://www.kaggle.com/datasets/uom190346a/synthetic-clinical-tabular-dataset

## How to run code
- First run the import block of code first as everything is depedant on that.
    - If needed, run this comand to install these libraries locally first: `pip install pandas numpy scikit-learn matplotlib seaborn tensorflow`
- Then follow step by step in each code block area to run the code that is need.
    - Note: Charts and grpahs will be eneded to be reran if models are changed and data is modified

## Results

| Model                | Key Hyperparameters                                              | Balanced Accuracy | Recall | True NEgative | F1-score | Training Time (s) |
|---------------------|------------------------------------------------------------------|------------------|--------------|-------------------|------------------|------------------|
| Random Forest       | n_estimators=300, max_depth=8, min_samples_leaf=5, balanced_subsample | 0.255            | 0.255        | 0.75              | 0.423            | 0.576            |
| Logistic Regression | C=0.2, solver=saga, class_weight=balanced                        | 0.259            | 0.259        | 0.74              | 0.281            | 0.044            |


## Key Insights
- Class imbalance significantly impacts model behavior, causing models to favor the Normal Diagnosis.
- Logistic Regression produces more balanced predictions, improving recall for critical conditions like Sepsis.
- Feature engineering (age groups, BMI categories, blood pressure categories, gluclose categories, cholestrol categories) helped models capture clinically meaningful patterns.
- Both models show relatively low confidence, indicating overlapping feature patterns and inherent difficulty of the task.
- Both models however showed relatively high true negative values, both above .7

## Recomendation
Logistic Regression provides the better model for the goal here and provides slightly better recall and true negative for non normal diagnosis which is better in a healthcare setting. This offers the ebst balance between performance, interetability, and realiability for real medical use.

## Project Structure/WorkFlow
- Setting up Project (dataset inclusion)
- Setting up Data and Imports
    - includes basic information of data and shows what was cleaned or what was missing
- 5 Feature Groups
    - Age Groups
    - BMI Category
    - Blood Pressure Category
    - Gluclose Category
    - CHolestrol Category
- Prepare Date For modeling
- Random Forest Implementation
- Logistic Regression Implmentation
- Comparison of Models
    - Performance Comparison
- Ethical Analysis
- Business Recomendations

