## Introduction
This assignment focuses on analyzing the effect of different sampling techniques on machine learning models when the dataset is imbalanced. The Credit Card Fraud Detection dataset is used, where fraudulent transactions are significantly fewer than non-fraudulent ones. Handling this imbalance is necessary to ensure fair and reliable model evaluation.

## Dataset Description
The dataset was downloaded from the GitHub link provided in the assignment. It contains multiple transaction-related features and a target column named `Class`. The value `0` represents non-fraud transactions, while `1` represents fraud transactions. Initial inspection showed that the dataset was highly imbalanced, which could bias machine learning models toward the majority class.

## Handling Class Imbalance
To meet the requirement of converting the dataset into a balanced class dataset, **random under-sampling** was applied. All fraud transactions (Class = 1) were kept, and an equal number of non-fraud transactions (Class = 0) were randomly selected. The two classes were then combined and shuffled. This resulted in a dataset with equal representation of both classes, making it suitable for training classification models.

## Sampling Techniques Used
After balancing the dataset, five sampling techniques were applied. Simple random sampling was used to randomly select a subset of the data. Bootstrap sampling was applied by sampling with replacement. Stratified sampling ensured that class proportions were preserved during sampling. Cluster sampling was performed by grouping transactions based on the transaction amount and selecting one cluster. Cross-validation was used to evaluate models using multiple folds for more reliable performance estimation.

## Machine Learning Models
Five machine learning models were used in this assignment. These include Logistic Regression, Decision Tree, Random Forest, K-Nearest Neighbors (KNN), and Naive Bayes. Each model was trained and tested using the different sampling techniques, and accuracy was used as the evaluation metric.

## Results and Observations
The results were summarized in an accuracy comparison table. Bootstrap sampling showed consistently strong performance across most models. Cross-validation produced relatively lower accuracy values, but these results are more realistic as they reflect true generalization performance. 
**Cluster sampling resulted in 100 percent accuracy for all models, which occurred due to overfitting caused by the homogeneous nature of the selected cluster.**

## Result Interpretation
The experiment shows that high accuracy does not always indicate better model performance. Cluster sampling produced misleadingly high accuracy due to sampling bias. Cross-validation, despite lower accuracy, provides a more dependable estimate of model performance. The choice of sampling technique has a significant impact on the results.
