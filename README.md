# Diagnosis Predictor
This project is to help signify what is likely for people to get certain diagnosis such as, sepsis, pnenoumia, etc. There are certain features in this dataset that can be useful into providing what is the most likely driving force of why somone would get diagnose with an illness such as age, blood pressure, gluclose elvel, sex, etc. 

## Dataset source
https://www.kaggle.com/datasets/uom190346a/synthetic-clinical-tabular-dataset

## How to run code
- First run the import block of code first as everything is depedant on that.
- Then follow step by step in each code block area to run the code that is need.
    - Note: Charts and grpahs will be eneded to be reran if models are changed and data is modified

## Results
| Model           | Key Hyperparameters                               | Accuracy | Weighted F1-score | Training Time (s)
|-----------------|--------------------------------------------------|----------|-----------------|-----------------
| Random Forest   | n_estimators=200, max_depth=None, random_state=42 | 0.557    | 0.402232        | 0.333020        
| Neural Network  | 2 hidden layers [32,16], ReLU, softmax output   | 0.559    | 0.400874        | 16.227932       
