# Credit_Risk_Analysis

## Overview of Analysis
The purpose of this analysis is to build and evaluate several machine learning models in the branch of Supervised Learning to predict credit risk. The follwing steps were carried out:

**Preprocessing steps:**
- Acquire the dataset (in this case text file)

**Transformational steps:**
- Identifying and handling the missing values (None)
- Encoding categorical variables with a mix of Pandas and Scikit Learn's 'LabelEncoder'

**Splitting the data set:**
- Feature scaling with StandardScaler
- Normalization

**Implement machine learning models:**
- Random Oversampling
- SMOTE
- Undersampling
- SMOTEEN (combined under-/oversampling)
- Balanced Random Forest Classifier
- Easy Ensemble AdaBoost Classifier

## Analysis Results
**Random Oversampling**
- Balanced accuracy score = 65%
- Precision score for high-risk group = 1%
- Recall/sensitivity score = 62%
- F1 score = 2%

<img width="1067" alt="Random Oversampling_accuracy score" src="https://user-images.githubusercontent.com/93743169/163449954-a2c5f9b5-9719-4b99-ac5d-718d371e4992.png">

<img width="805" alt="Random Oversampling_classification report" src="https://user-images.githubusercontent.com/93743169/163450159-21d2eb79-a8f9-4be7-b983-e2a799cd1b3e.png">

**SMOTE**
- Balanced accuracy score = 64%
- Precision score for high-risk group = 1%
- Recall/sensitivity score = 63%
- F1 score = 2%

<img width="975" alt="SMOTE_accuracy score" src="https://user-images.githubusercontent.com/93743169/163450607-b57e82e0-a190-4c61-88df-ffad69b36042.png">

<img width="800" alt="SMOTE_classification report" src="https://user-images.githubusercontent.com/93743169/163450636-57984991-cb39-45bc-bcc6-b06d6b9104e4.png">

**Undersampling**
- Balanced accuracy score = 52%
- Precision score for high-risk group = 1%
- Recall/sensitivity score = 59%
- F1 score = 1%

<img width="983" alt="Undersampling_accuracy score" src="https://user-images.githubusercontent.com/93743169/163451183-788646fa-b0a1-479f-8fb0-bca2960f6d3a.png">

<img width="802" alt="Undersampling_classification report" src="https://user-images.githubusercontent.com/93743169/163451291-2f3ea67c-8806-4abe-9f73-8baf82d80e68.png">

**SMOTEEN**
- Balanced accuracy score = 61%
- Precision score for high-risk group = 1%
- Recall/sensitivity score = 67%
- F1 score = 1%

<img width="990" alt="SMOTEEN_accuracy score" src="https://user-images.githubusercontent.com/93743169/163451955-0cfe27c6-0d7a-422f-85b0-16dff2f35bfd.png">

<img width="734" alt="SMOTEEN_classification report" src="https://user-images.githubusercontent.com/93743169/163451991-ba56983c-acdf-4450-b85e-8060025036ea.png">

**Balanced Random Forest Classifier**
- Balanced accuracy score = 92%
- Precision score for high-risk group = 4%
- Recall/sensitivity score = 71%
- F1 score = 8%

<img width="981" alt="BRFC_accuracy score" src="https://user-images.githubusercontent.com/93743169/163452411-320dfb15-cde5-4282-b9fa-b8af40d153f9.png">

<img width="804" alt="BRFC_classification report" src="https://user-images.githubusercontent.com/93743169/163452435-31038ee4-31ea-4770-b154-413dc3578f4f.png">

**Easy Ensemble AdaBoost Classifier**
- Balanced accuracy score = 93%
- Precision score for high-risk group = 8%
- Recall/sensitivity score = 91%
- F1 score = 14%

<img width="988" alt="AdaBoost_accuracy score" src="https://user-images.githubusercontent.com/93743169/163452910-4b459d54-ffe2-498b-92ea-6e2426bac896.png">

<img width="815" alt="AdaBoost_classification report" src="https://user-images.githubusercontent.com/93743169/163452934-c778d7b6-df46-45e1-a117-8e9800fb910f.png">

## Summary
Of the 6 models used in this analysis, the ensemble models (Balanced Random Forest & AdaBoost) had the highest balanced accuracy scores. The recall or sensitivity score for the AdaBoost model was the highest at 91%, indicating it is effective in detecting a large portion of high risk credit. However, when one examines the precision scores, it is evident that all the models scored less than 10% , which results in a lot of low risk credits being falsely detected as high risk, which would result in missed opportunities for the financial institutions. Also, the F1 scores are low, indicative of how accurate the models are at predicting credit risk (when balancing precision & recall in an imbalanced real-world sample). After considering the analysis & results, I would not recommend any of the 6 machine learning models. However, it would behoove us to use other ensemble alogorithms, like GradientBoosted Tree or XGBoost to compare their predictive performance as compared to the 2 we used in this analysis.
