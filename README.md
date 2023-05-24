# Phase 3 Project - Churn prediction of SyriaTel Customers.
 ![Damuscus city at night](https://github.com/Muramati/Churn_prediction_Telecom_Customer/blob/main/images/Damascus.jpg?raw=true)
 Damascus City at night, the HQs of SyriaTel.

## Overview

In the telecom industry, customer churn refers to customers ending their relationship with a company or service provider. Churn rates range from 15% to 25% annually due to intense competition. Retaining customers individually is challenging due to the large customer base, making personalized efforts impractical. However, predicting high-risk churn customers enables companies to optimize resources and improve loyalty. Retaining existing customers is more cost-effective than acquiring new ones. Understanding customer interactions is crucial for detecting and addressing churn. Telecom companies strive to reduce attrition, implement retention strategies, and achieve sustainable success by expanding their customer base and reducing acquisition costs.

## Business and Data Understanding
### Business Understanding
Customer churn is a significant concern for Syriatel, a leading telecommunications company in Syria. To mitigate churn, Syriatel should analyze historical churn data, segment its customer base, measure customer satisfaction, and implement personalized retention efforts. Providing quality customer service, competitive pricing, and proactive communication are crucial. By understanding customer behavior and preferences, Syriatel can tailor retention strategies to address specific customer segments and improve overall customer satisfaction, ultimately reducing churn rates and driving business growth.

One effective approach to address customer churn in the telecom industry is the use of predictive models. By leveraging customer data and employing machine learning algorithms, predictive models can identify customers who are at a higher risk of churn. These models analyze historical customer data, such as demographics, usage patterns, billing information, and customer interactions, to identify patterns and indicators associated with churn.

## Data Understanding
[Churn in Telecom's dataset](https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset)

The csv file has the following columns:

1. State: The state where the customer is located.
2. Account Length: The duration of the customer's account in terms of days.
3. Area Code: The area code associated with the customer's phone number.
4. International Plan: Whether the customer has an international calling plan (Yes/No).
5. Voice Mail Plan: Whether the customer has a voice mail plan (Yes/No).
6. Number of Voicemail Messages: The number of voicemail messages the customer has.
7. Total Day Minutes: The total number of minutes the customer used during the daytime.
8. Total Day Calls: The total number of calls made by the customer during the daytime.
9. Total Day Charge: The total charge for daytime usage.
10. Total Evening Minutes: The total number of minutes the customer used during the evening.
11. Total Evening Calls: The total number of calls made by the customer during the evening.
12. Total Evening Charge: The total charge for evening usage.
13. Total Night Minutes: The total number of minutes the customer used during the night.
14. Total Night Calls: The total number of calls made by the customer during the night.
15. Total Night Charge: The total charge for night usage.
16. Total International Minutes: The total number of international minutes used by the customer.
17. Total International Calls: The total number of international calls made by the customer.
18. Total International Charge: The total charge for international usage.
19. Number of Customer Service Calls: The number of customer service calls made by the customer.
20. Churn: The target variable indicating whether the customer has churned or not (Yes/No).

The telecommunication churn dataset provides data that is essential for understanding customer churn in the telecommunication industry. It offers insights into various aspects of customer behavior, service usage, and account information. By exploring and analyzing these aspects of the dataset, businesses can gain a comprehensive understanding of customer churn in the telecommunication industry. This understanding forms the foundation for developing strategies to mitigate churn, improve customer retention, and enhance overall business performance.


## Modeling
The models used in the analysis were Logistic Regression, Random Forests, K-Nearest Neighbors (KNN), and XGBoost. Each model was chosen for its specific characteristics and potential to predict customer churn in the telecommunications dataset.

1. Logistic Regression:

    Logistic Regression is a commonly used model for binary classification tasks like churn prediction.It provides interpretable results and can estimate the probability of churn based on the input features.Logistic Regression was chosen as a baseline model to establish a benchmark for performance and interpretability.

2. Random Forests:

    Random Forests are an ensemble learning method that combines multiple decision trees.
    They are known for their ability to handle complex relationships and interactions between features.
    Random Forests can capture non-linear patterns in the data and provide robust predictions.
    This model was selected to leverage its ensemble nature and potential for high accuracy.
    K-Nearest Neighbors (KNN):

3. KNN is a non-parametric algorithm that classifies data points based on their proximity to other points in the feature space.
    It can capture local patterns and is suitable when the decision boundary is not well-defined.
    KNN was included to explore the performance of a different type of model and assess its ability to identify churn.
    XGBoost:

4. XGBoost is an optimized gradient boosting algorithm known for its high predictive power and efficiency.
    It combines multiple weak models to create a strong ensemble model.
    XGBoost can handle complex interactions, feature importance, and missing data effectively.
    It was selected as a powerful model to potentially outperform other algorithms and improve prediction accuracy.
    Tuning the XGBoost model was performed to optimize its hyperparameters and further improve its performance. The tuned model achieved perfect accuracy on the training data, indicating its potential to capture complex patterns and overfitting risks.

Overall, a combination of different models was chosen to explore their strengths and weaknesses in predicting churn. Logistic Regression provided interpretability, Random Forests offered robustness, KNN explored local patterns, and XGBoost aimed for high accuracy. This approach helped assess various aspects of the data and select the most effective models for predicting customer churn in the telecommunications dataset.



## Evaluation

These are the results of the modelling:
### Logistic Regression:

    Accuracy: 81.82%
    Specificity / True Negative Rate: 82.79%
    Sensitivity / True Positive Rate / Recall: 75.34%
    False Negative Rate: 24.66%
    False Positive Rate: 17.21%
    This model provided a balanced performance with reasonable accuracy and recall.

### Random Forests:

    Accuracy: 93.05%
    Specificity / True Negative Rate: 95.7%
    Sensitivity / True Positive Rate / Recall: 75.34%
    False Negative Rate: 24.66%
    False Positive Rate: 4.3%
    The Random Forests model achieved higher accuracy and specificity compared to logistic regression, indicating better     overall performance.

### K-Nearest Neighbors (KNN):

    Accuracy: 70.23%
    Specificity / True Negative Rate: 72.54%
    Sensitivity / True Positive Rate / Recall: 54.79%
    False Negative Rate: 45.21%
    False Positive Rate: 27.46%
    The KNN model had lower accuracy and sensitivity compared to the other models, indicating a weaker performance in    predicting churn.

### XGBoost (Untuned):

    Accuracy: 94.83%
    Specificity / True Negative Rate: 97.34%
    Sensitivity / True Positive Rate / Recall: 78.08%
    False Negative Rate: 21.92%
    False Positive Rate: 2.66%
    The untuned XGBoost model demonstrated high accuracy and specificity, along with a reasonable level of sensitivity.

### XGBoost (Tuned):


Accuracy: 93.76% 

Precision for class : 97% 

Recall for class : 96%

F1-Score for class : 96%

In summary, the model achieved an accuracy of 93.76%, which indicates that it classified 93.76% of the instances correctly. It performed well in terms of specificity (96.11%) and sensitivity (78.08%), indicating a good balance between correctly classifying both negatives and positives. 
    

### ROC AUC Curve
    The ROC AUC (Receiver Operating Characteristic Area Under the Curve) score of 0.89 indicated that the model has good discrimination power in distinguishing between the positive and negative classes. The score also suggests that the model has a high true positive rate and a relatively low false positive rate which in turn indicates that the model is performing well in terms of classifying the positive instances correctly and minimizing false positives.

## Conclusions

1. Overall, the Random Forests and XGBoost models (both untuned and tuned) performed the best in terms of accuracy and  other evaluation metrics. These models exhibited higher accuracy and better balance between sensitivity and specificity, making them more suitable for predicting customer churn in the telecommunications dataset.The model created by the XGBoost untuned though is the best as it would predict the data at an accuracy of 94.83% and has an ROC AUC score of 89% which is good.git

2. While determining the features to take action on as they look for ways to improve, SyriaTel should consider the following features from their data set: total eve calls international plan, total day calls, total night calls, total night minutes and customer service call as they rank the first in feature importances which represent the relative importance of each feature in predicting the target variable in the most performing model, the untuned XGboost.

3. A relationship between the features and the target was found and it does make sense considering the classification metrics and it would be advisable for SyriaTel to use the model.