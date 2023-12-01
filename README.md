# SYRIATEL Churn-Analysis
![churn image 1](https://github.com/101Prudencia-py/Churn-Analysis/assets/141912223/1bc2b90f-5cf3-49cc-96c6-319ae99f1f6b)

# OVERVIEW
Syriatel is one of the major telecommunications companies in Syria, providing a range of services including mobile and fixed-line telephony, internet, and other related services. Conducting a churn analysis for Syriatel involves examining customer behaviors and patterns to predict which customers are likely to discontinue their services with the company.

This project uses the syriatel dataset to conduct a comprehensive analysis of churn predictions using various models such as logistic regression , Decison trees classifier and random forest classifier as it is a binary classification problem.

We seek to gather insights that can help syriatel predict which customers are most likely to leave and stay and what factors cause or instigate this decision.

# BUSINESS UNDERSTANDING
Our main objective is to build a model that can accurately predict when a customer is about to leave by analysisng the behaviors and trends that precede churn. Identify indicators or triggers indicating a higher likelihood of churn.

To identify which features are correlated to churn.

How can we keep our customer base to reduce churn whule also attracting new customers.

To the stakeholder which is SyriaTel. We are interested in reducing how much money is lost because of customers who don't stick around very long and take precautions.

# DATA UNDERSTANDING
The dataset contains information about syriaTel customers and is in a csv file format. Some features included in the data are minutes clients have used, state the customer is in , their area code , how many day/evening/international calls they have made, the number of times a customer has called customer service and if they have churned. Our target variable is Churn. The dataset contains 3333 rows and 21 columns. As the analysis progresses, some rows may be dropped such as phone number as they aren't useful when modelling. You can find the data [here]
(bigml_59c28831336c6604c800002a)

#### EDA
The data was quite clean, only dropped phone numbeer features and some outliers. However the charges columns were removed due to multicollinearity with the miutes columns.

# MODEL
Diffeent classification models were built for this project. They include:

Logistic Regression Classifier
Decisioin Tree Classifier
Random Forest Classifer

We evaluated our models based on the recall score metric as well as the corresponding confusion matrix. Once the best model was identified, which was random forest classifier, we assessed the model performance on a seperate test set to determine whether the model continued to perform well or if the model was overfitting.Hyperparameter tuning was also performed to try and improve our models.

The decision behind choosing to evaluate the model on recall was made by considering the cost and impact of false negative predictions, that is, we determined that it was more costly for the company for the model to predict that a customer would stay with SyriaTel when in fact that would churn/leave. This would lead to a missed opportunity for the company to dedicate retention resources towards that customer and keeping their business. Maximising recall score accounts for this scenario in our model and so it was for this reason that we chose this as our evaluation metric.

![churn](churn-rate.png)
# CONCLUSION
The random forest classier performed the best with a recall of 79%, indicating that the model correctly identified around 79% of the actual positive cases, which isn't bad. And an acccuracy score of 93%.

A high f1-score of 78% shows a balanced evaluation of the model's accuracy in predicting both churn and non-churn customers.

Texas has the highest churn rate.

Based on the graph Total day minutes, total eveing minutes and total international minutes are the most important features when predicting churn.

# RECOMMENDATIONS
Implement a strategy that could include giving discounts to international plans and voice mail subscriptions as we've seen those without these plans tend to churn. Many of them may see these plans as too expensive to purchase hence opting not to . This could help attract these niche customer base.

People with large total call minutes must be charged large amounts of money and may be dissatisfied with the charges hence decide to leave. To counteract this, we could introduce package deals to those who call for long periods of time.

Loyalty points / cards and deals for customers who have had their account for more than 3 yrs or more for example.

Improve Customer feedback - This could include conducting surveys of customers who have churned to understand why they left and the reasoning behind it. Thsi could also include improving customer service calls as they play a role in churn. Find out the most common issues that customers call about.

# NEXT STEPS AND LIMITATIONS
Further investigate on what trends might be causing high churn in certain states such as texas and how we can prevent this.

There could be othr features that affect churn other than the ones privided in our dataset.

Explore other model classifiers that may provide better results than random forest classifier.
