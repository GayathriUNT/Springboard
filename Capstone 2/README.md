## Credit Card Customer Churn Prediction
The credit card service in the bank possesses high risk as well as high profits. The existing customers leaving their credit card services are considered as churned customers.  Customer Churn is one of the most important and challenging problems with banks. It is easier for banks to keep the existing customer than adding new ones. To support the bank, reduce churn rate, its crucial to predict customers that are high risk of churn. The bank customer dataset was used to build machine learning model to find customers who are most likely to cancel the credit cards.  This could help bank staffs to proactively follow up with customers to provide better services and turn their decision to keep them with the bank.

### 1. Data
 The bank customer dataset was extracted from Kaggle dataset: https://www.kaggle.com/sakshigoyal7/credit-card-customers This dataset contained 10127 records and 21 features about customers mentioning their age, salary, marital_status, credit card limit, credit card category, etc. Since this dataset was obtained from the Kaggle and was already clean which made the preparation task easier. Though, this is not the case with the real-world data. 
 
 ### 2. EDA
The target variable was ‘Attrition_Flag’ and almost 84% of the record belonged to ‘Existing customer’ category and 16% was ‘Attired customer’ category. Since, most of the record belong to one category the dataset had imbalanced class problem which was handled before training the model. <br>
 ![image](https://user-images.githubusercontent.com/59039411/135375471-ea00b0e0-de71-4be7-aff6-4e85c79a7ed5.png)

&emsp;- Female customers churned more than male. Almost 9% of  churned customers were female and 7% were Male <br>
&emsp;- 6% of Churned customers were Graduate <br>
&emsp;- 7% of Churned customers were in Married Category<br>
&emsp;- Customers with income between 40K – 60K cancelled more than other income group<br>
&emsp;- Most of the churned customers were Blue card holders <br>

### 3. Modeling

The Logistic Regression classifier was used as a base line model and various machine learning models were developed and results were compared to choose the best model.The hyper-parameter tunning was carried using GridSearch CV for various model such as RandomForest, Gradient Boosting and XGBoosting to find the best hyper-parameter for each model. All the other models performed better the Logistic Regression.<br>
The table below shows the Accuracy and AUC score for different models-<br>
![image](https://user-images.githubusercontent.com/59039411/135376542-a8f57517-6bd2-4e6e-ab5f-7af2e458ce02.png)

The comparison of the ROC curve for all the models were shown below- <br>
![image](https://user-images.githubusercontent.com/59039411/135376734-d84d6ca7-7b5e-4753-9ed0-6ff3dd0165fd.png)

The XGBoost classifier had the best performance with AUC score of almost .94. XGBoost had a feature that allows to select the important feature in the dataset and the above figure-5 visualizes the contribution of each variable. The total_Trans_ct  almost contibuted 100% and Total_relationship_count  was close to 40%. These were the  variables that contributed the most in classifying the dataset. <br>

**Feature Importance** <br>

![image](https://user-images.githubusercontent.com/59039411/135376976-55ca46c3-0d85-4401-963c-2ef02569c014.png)

### 4. Conclusion
&emsp;- The Total_tran_ct was one of important feature from all the models. If a customer had not transacted in while with less total_trans_ct are more likely to chrun.<br>
&emsp;- Total_relationship_count was another important variable. <br>
&emsp;- It would be important to proactively reach out to those customers to improve a personalize customer experience.<br>
&emsp;- Bank could collect more information about the customers as how long they are with the service <br>
&emsp;- Collect data  based on  satisfaction survey about credit card services <br>






 

