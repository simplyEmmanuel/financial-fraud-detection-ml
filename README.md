# Financial Fraud Detection Using Machine Learning

Description: 
This is a comprehensive project on detecting financial fraud using machine learning techniques. The project includes data preprocessing, feature selection, model training and evaluation, and visualization of results.

## Table of Contents
1. [Introduction](#introduction)
2. [Dataset](#dataset)
3. [Data Preprocessing](#data-preprocessing)
4. [Models and Evaluation](#models-and-evaluation)
5. [Results and Discussion](#results-and-discussion)
6. [Conclusion](#conclusion)
7. [Future Work](#future-work)
8. [References](#references)
9. [License](#license)

## Introduction 
![image](https://github.com/simplyEmmanuel/financial-fraud-detection-ml/assets/57048981/08a0321a-5915-4069-af20-6bb8f3e180ba)


  In today's digital age, financial fraud poses a significant threat to consumers and institutions, leading to substantial economic losses and erosion of trust in financial systems. With the increasing volume and complexity of digital transactions, detecting fraudulent activities has become a critical priority. Financial fraud encompasses various malicious activities, including unauthorized transactions, account takeovers, and money laundering, which can lead to severe economic repercussions. Recent reports indicate that global losses due to financial fraud amount to billions of dollars annually, underscoring the urgent need for effective fraud-detection mechanisms (ACFE, 2022; PwC, 2021).

  Effective fraud detection is essential to maintaining the integrity of financial systems and protecting stakeholders. Advanced machine learning models offer promising real-time solutions for identifying fraudulent transactions, enabling financial institutions to respond swiftly and mitigate potential damages. This study leveraged a synthetic dataset generated using the PaySim simulator, mimicking mobile money transactions based on real financial logs. The dataset comprehensively represents legitimate and fraudulent transactions, making it an ideal testbed for developing and evaluating fraud detection models.
  
## Dataset
The dataset contains:
- 6,362,620 transactions, with 11 columns initially,
- reduced to 7 columns after preprocessing.

## Data Preprocessing
Steps include:
- Dropping irrelevant columns (`nameOrig` and `nameDest`).
- Encoding categorical variables (`type`) using one-hot encoding.
- Standardizing numerical features (`amount`, `oldbalanceOrg`, `newbalanceOrig`, `oldbalanceDest`, `newbalanceDest`).

![image](https://github.com/simplyEmmanuel/financial-fraud-detection-ml/assets/57048981/fcc3b735-fb94-42c6-81e2-30295714e6d0)

The data frame from the previous screen has now been reduced to this, 

![image](https://github.com/simplyEmmanuel/financial-fraud-detection-ml/assets/57048981/53d3416a-7df2-42d2-aecd-b80e664b19eb)

## Models and Evaluation
We implemented and evaluated the following models:
- Logistic Regression
- Random Forest
- Gradient Boosting
- Naive Bayes

![image](https://github.com/simplyEmmanuel/financial-fraud-detection-ml/assets/57048981/8793cc94-64d1-4275-b045-443fe4c4d1e9)

![image](https://github.com/simplyEmmanuel/financial-fraud-detection-ml/assets/57048981/047f1c6f-6a06-4450-baac-e2c72e5b447a)

`Summary of Confusion Matrices:`
  The confusion matrices for the Logistic Regression, Random Forest, Gradient Boosting, and Naive Bayes models highlight the performance of each model in distinguishing between fraudulent and non-fraudulent transactions.

- Logistic Regression shows a balanced but less effective performance with a notable number of false positives and false negatives.
- Random Forest and Gradient Boosting outperform Logistic Regression with higher precision and recall values, indicating their robustness in detecting fraud.
- Naive Bayes, while having a high recall for fraud, suffers from a significant number of false positives, indicating it is less reliable in this context.

## Results and Discussion
  I compared the models based on accuracy, precision, recall, F1 score, and ROC AUC score. Feature selection techniques like RFE and PCA were used to improve model performance. The Random Forest and Gradient Boosting models performed best in detecting fraudulent transactions.

![image](https://github.com/simplyEmmanuel/financial-fraud-detection-ml/assets/57048981/de858165-e4c9-466c-89de-1156d74e3663)

## Conclusion
  Ensemble methods such as Random Forest and Gradient Boosting are highly effective for fraud detection. Feature selection significantly improves model interpretability and performance. However, the synthetic nature of the dataset and potential imbalances are limitations. 

  The feature importance plot for the Random Forest model reveals that 'amount', 'step', and 'type_TRANSFER' are the most significant features in predicting fraudulent transactions.
'type_CASH_OUT' and 'type_PAYMENT' are given less importance, suggesting that these features have less influence on the model's predictions.

## Future Work
Future efforts include validating models using real-world datasets, exploring advanced techniques like deep learning, and continuously updating models with new data to maintain accuracy.

## References
- Association of Certified Fraud Examiners (ACFE). (2022). Report to the Nations: 2022 Global Study on Occupational Fraud and Abuse.
- PricewaterhouseCoopers (PwC). (2021). Global Economic Crime and Fraud Survey 2021.
- Bolton, R. J., & Hand, D. J. (2002). Statistical fraud detection: A review. Statistical Science, 17(3), 235-255.
- Dataset: Lopez-Rojas, E. A., Elmir, A., & Axelsson, S. (2016). Synthetic Financial Datasets For Fraud Detection. (n.d.). Kaggle.com. Retrieved June 14, 2024, from https://www.kaggle.com/datasets/ealaxi/paysim1/discussion/298516

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
