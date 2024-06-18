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

## Data Preprocessing
Steps include:
- Dropping irrelevant columns (`nameOrig` and `nameDest`).
- Encoding categorical variables (`type`) using one-hot encoding.
- Standardizing numerical features (`amount`, `oldbalanceOrg`, `newbalanceOrig`, `oldbalanceDest`, `newbalanceDest`).

## Models and Evaluation
We implemented and evaluated the following models:
- Logistic Regression
- Random Forest
- Gradient Boosting
- Naive Bayes

## Results and Discussion
I compared the models based on accuracy, precision, recall, F1 score, and ROC AUC score. Feature selection techniques like RFE and PCA were used to improve model performance. The Random Forest and Gradient Boosting models showed the best performance in detecting fraudulent transactions.

## Conclusion
Ensemble methods such as Random Forest and Gradient Boosting are highly effective for fraud detection. Feature selection significantly improves model interpretability and performance. However, the synthetic nature of the dataset and potential imbalances are limitations.

## Future Work
Future efforts include validating models using real-world datasets, exploring advanced techniques like deep learning, and continuously updating models with new data to maintain accuracy.

## References
- Association of Certified Fraud Examiners (ACFE). (2022). Report to the Nations: 2022 Global Study on Occupational Fraud and Abuse.
- PricewaterhouseCoopers (PwC). (2021). Global Economic Crime and Fraud Survey 2021.
- Bolton, R. J., & Hand, D. J. (2002). Statistical fraud detection: A review. Statistical Science, 17(3), 235-255.
- [Additional references as needed]

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
