# credit-risk-classification

## Model 1 Report
### Overview of the Analysis
The purpose of this analysis was to build a machine learning model to predict loan statuses based on various financial information. The dataset used for this analysis contained features such as loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, and total debt. The goal was to predict whether a loan is healthy (0) or high-risk (1) based on these features.

### Results of Model 1
- Balanced Accuracy Score: 0.952
- Precision (high-risk loan): 0.85
- Recall (high-risk loan): 0.91
### Description of Model 1
Model 1 utilized logistic regression on the original imbalanced data. Logistic regression is a commonly used classification algorithm that works well for binary classification tasks.

### Balanced Accuracy Score
The balanced accuracy score of Model 1 was 0.952, which is a good indicator of overall model performance. This score takes into account the class imbalance in the dataset, providing a more balanced evaluation of the model's accuracy.

### Precision and Recall
For high-risk loans (label 1), Model 1 achieved a precision of 0.85 and a recall of 0.91. Precision measures the proportion of true high-risk loans among all the loans predicted as high-risk. Recall, on the other hand, measures the proportion of true high-risk loans that were correctly identified by the model.

A precision of 0.85 indicates that 85% of the loans predicted as high-risk were indeed high-risk loans, while a recall of 0.91 indicates that the model correctly identified 91% of the actual high-risk loans.

### Summary of Model 1
Model 1 showed promising results in predicting loan statuses. It achieved a high balanced accuracy score, indicating that the model performs well in predicting both healthy and high-risk loans.

The precision and recall scores for high-risk loans are also reasonable, with precision at 0.85 and recall at 0.91. This means that the model can correctly identify a significant proportion of high-risk loans while maintaining a relatively low false positive rate.

Overall, Model 1 is a good starting point for loan status prediction. However, it's essential to consider the business context and the impact of false negatives and false positives. Depending on the specific objectives and requirements of the lending institution, further adjustments and optimizations may be needed to achieve the desired model performance.

### Recommendation
Considering the performance of Model 1 and the problem we are trying to solve (predicting loan statuses), the model seems to be a reasonable choice. Its accuracy, precision, and recall scores are all above 85%, indicating that it can effectively predict both healthy and high-risk loans.

However, as the dataset is imbalanced, and the cost of misclassifications can vary depending on the business context, it might be beneficial to explore other techniques to handle class imbalance. Model 2, which utilizes logistic regression with resampled training data, showed even better performance, particularly in terms of recall for high-risk loans. Therefore, it may be worth considering Model 2 as an alternative option to improve performance further.

Ultimately, the decision on which model to use should be made after carefully evaluating the business requirements and the costs associated with different types of misclassifications. Regular model evaluation and monitoring should also be conducted to ensure the model's performance remains satisfactory over time.

## Model 2 Report

### Overview of the Analysis
The purpose of this analysis was to build a machine learning model to predict loan statuses based on various financial information. The dataset used for this analysis contained features such as loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, and total debt. The goal was to predict whether a loan is healthy (0) or high-risk (1) based on these features.

### Results of Model 2
Balanced Accuracy Score: 0.994
Precision (high-risk loan): 0.84
Recall (high-risk loan): 0.99
Description of Model 2
Model 2 utilized logistic regression with resampled training data to handle the class imbalance present in the dataset. Class imbalance can be an issue in classification tasks, as it may lead to biased models that are more biased towards predicting the majority class. To address this, Model 2 employed the RandomOverSampler technique to balance the number of samples in the two classes (healthy and high-risk loans).

### Balanced Accuracy Score
The balanced accuracy score of Model 2 was an impressive 0.994, indicating excellent overall model performance. This score considers the class imbalance, providing a more reliable evaluation of the model's accuracy.

### Precision and Recall
For high-risk loans (label 1), Model 2 achieved a precision of 0.84 and a recall of 0.99. A precision of 0.84 means that 84% of the loans predicted as high-risk were actually high-risk loans. Meanwhile, a recall of 0.99 indicates that the model correctly identified 99% of the actual high-risk loans, making it highly effective in catching high-risk loans.

### Summary of Model 2
Model 2 demonstrated exceptional performance in predicting loan statuses, particularly high-risk loans. Its balanced accuracy score of 0.994 indicates that the model is highly accurate and effectively classifies both healthy and high-risk loans.

The precision score of 0.84 implies that the model's predictions of high-risk loans are quite reliable, and it avoids misclassifying healthy loans as high-risk loans to a large extent. The high recall score of 0.99 indicates that the model can effectively identify nearly all actual high-risk loans, minimizing the number of false negatives.

The utilization of the RandomOverSampler technique to address class imbalance significantly improved the model's ability to predict high-risk loans correctly. By resampling the training data, the model achieved a better balance in learning from both classes, resulting in improved performance.

### Recommendation
Based on the outstanding results of Model 2 and the problem we are trying to solve (predicting loan statuses), this model is highly recommended for deployment. Its accuracy, precision, and recall scores are all above 80%, and the model effectively handles the class imbalance issue.

The exceptional recall score of 0.99 for high-risk loans means that the model can capture almost all high-risk loans, which is particularly important for risk assessment and decision-making in lending. While the precision of 0.84 indicates some false positives, it still maintains a high level of accuracy in predicting high-risk loans.

Continued monitoring and evaluation of Model 2's performance will be essential to ensure its effectiveness in real-world scenarios. Additionally, as the lending landscape and data evolve, it may be necessary to periodically retrain the model and make necessary adjustments to maintain its reliability.

In conclusion, Model 2 with logistic regression and resampled training data is a powerful tool for loan status prediction, especially in identifying high-risk loans accurately. Its robust performance and ability to handle class imbalance make it a valuable asset for lending institutions seeking to improve their risk assessment and decision-making processes.
