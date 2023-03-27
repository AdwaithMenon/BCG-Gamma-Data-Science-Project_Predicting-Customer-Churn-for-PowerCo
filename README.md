# _BCG Gamma Data Science Project: Predicting Customer Churn for PowerCo_

## **Project Description**

PowerCo, a significant gas and electricity provider, caters to a broad range of clients, including corporate, Small and Medium Enterprises (SMEs), and residential customers. However, the liberalization of the energy market in Europe has resulted in considerable customer churn, particularly in the SME sector. To tackle this issue, PowerCo has joined forces with BCG to investigate the root cause of the SME customer churn.

The Hypothesis is that "Customer Churn is affected by Price Sensitivity".

The objective of this project is to create a classification model capable of detecting SME clients who are more likely to churn if PowerCo maintains its current prices. Furthermore, the aim is to identify the most significant factors/predictors associated with customer churn. Upon analysis, recommendations will be made to enhance customer retention.


## **Observations**


### a) **Scatterplot for Net Margin on Power Subscription vs Subscribed Power**

<img width="341" alt="image" src="https://user-images.githubusercontent.com/70052374/228011806-fa9fa013-078a-4c84-9a7e-738700d13634.png">

* There is a positive correlation between Subscribed Power and Net Margin.



### b) **Box Plots for Current Paid Consumption for Customers who have churned vs Customers who have not Churned**

<img width="508" alt="image" src="https://user-images.githubusercontent.com/70052374/228012173-60fb58dd-187b-43e2-bb0c-9e94236acd05.png">

* The median value for Current Paid Consumption is slightly higher for Customers who have churned vs Customers who have not churned.



### c) **Distribution of Electricity Consumption for Past 12 months**

<img width="341" alt="image" src="https://user-images.githubusercontent.com/70052374/228012390-edd4cc61-e318-4789-96d1-2cb37ef21e75.png">

* The distribution is righ-skewed. Majority of the clients have a total consumption of less than 100000 in the last 12 months.


## **About the Model**

* The chosen approach for tackling this problem involves implementing a Random Forest Classifier. Falling under the category of ensemble algorithms, the Forest is composed of multiple Decision Trees, which are tree-based learning algorithms. The strength of an ensemble algorithm is attributed to the laws of averaging, weak learners, and the central limit theorem.

* A Total Accuracy of **0.9** and a Precision of **0.8** were achieved on the Test Set using the Random Forest Classifier.


## **Feature Importance**

* Feature importances convey the significance of a feature in the predictive model. In the case of Random Forest, the feature importance is a measure of how frequently each feature is employed for splitting across all the trees.

<img width="739" alt="image" src="https://user-images.githubusercontent.com/70052374/228014585-ca6048d1-1531-4c98-b509-25d3c10609be.png">


* In this model, total net margin and consumption over a 12-month period are the primary factors that drive churn.

* Margin on power subscription also has a significant impact on churn.

* Price sensitivity features are present in the model but do not have a significant impact on customer churn.


## **Testing the Hypothesis**

    > Is churn driven by the customers' price sensitivity?

After analyzing the feature importances, it appears that the **feature in question (price sensitivity) does not have a significant impact on the model's performance and can be considered a minor factor**. Nonetheless, further experimentation is necessary to make a definitive conclusion.
