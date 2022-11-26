# **Ecommerce Customer**

# Use Case

- Use Case Summary
- Objective Statement:
  * Get business insight about how to decide whether focusing development on mobile apps or website.

- Challenges:
  * Need to workaround with the code python.

- Methodology / Analytic Technique:
  * Descriptive analysis
  * Graph analysis
  
- Business Benefit:
  * Helping Development Team to decide whether their focusing on website development or mobile apps development.

- Expected Outcome:
  * Know the priority of development apps.
 
# Business Understanding

- Knowing who contribute the most of yearly amount spent.

# Data Understanding

- Data of Ecommerce Customer
- The Dataset has 8 columns and 500 rows
- Data dictionary : 
  Email = email of the customer
  Address = address of the customer
  Avatar = avatar of the customer
  Avg. Session Length = customer avarage session time 
  Time on App  = customer 
  Time on Website  
  Length of Membership 
  Yearly Amount Spent 

# Data preparation 

- Code Used:
- Python Version: 3.7.6
- Packages: Pandas, Numpy, Matplotlib, Seaborn, Sklearn and statsmodels

# Data Cleansing 

- After checking the dataset, the data doesnt need to be clean because there are no missing value, Nan, Null or duplicated rows.

# Exploratory Data Analysis

* From the coefficient values above, we can see that `Length of Membership` is the highest contribute in target variable increment. It's mean that an increase of 1 point in `Lengh of Membership`, while the other features are kept fixed, is associated with an increase of 61.89 point in `Yearly Amount Spent` (target variable)
* If we want to choose do we have to focus our effort on `Mobile App` or `Website` development, based on table above the answer is on ` Mobile App`. Because the coefficient value on `Time on App` is biggest than coefficient value on `Time on Website`. It's mean, people that looking for shoping in mobile app will tend to buy the product

# Modeling Data: Linear Regression

- KDE Plot

![image](https://user-images.githubusercontent.com/113915274/204073980-bc015643-e547-46dd-8956-0a69849625b8.png)

* As we can see that all numerical columns look symmetric

- Bivariate Analysis

![image](https://user-images.githubusercontent.com/113915274/204074018-dffde7ca-ddfe-407c-a509-1dd51c8d1e09.png)

* Length of Membership is highly correlated with Yearly Amount Spent. it is mean the higher Length of Membership, the higher contribution of Yearly Amount Spent

![image](https://user-images.githubusercontent.com/113915274/204074049-61850f62-0e17-4a83-93f3-42232e13648e.png)

![image](https://user-images.githubusercontent.com/113915274/204074150-6fc6f4ee-281b-4257-9097-48af46ed54f0.png)

![image](https://user-images.githubusercontent.com/113915274/204074160-ffed96bf-7fb5-47a6-970f-5da0b4b95ca8.png)

* seems like there is no meaningful pattern above

![image](https://user-images.githubusercontent.com/113915274/204074169-cfaf070b-a5be-4c75-9992-cc6746d3b6cb.png)

![image](https://user-images.githubusercontent.com/113915274/204074176-68a0e780-ffc6-45f9-8463-8862c28bfdb5.png)

* The higher `Time on App` will contribute increment on `Yearly Amount Spent`

* Based on this visualization, we can see that `Length of Membership` is the most correlated feature with `Yearly Amount Spent`

# Evaluating Model: Linear Regression

- Training Error Check

R-squared for training data is 0.9817562058732432
RMSE for training data is 10.336893843068001

* The R-squared value is 0.981. It's mean `98.1%` of variability of Yearly Amount Spent is successfuly explained using all the features in the model
* The standard deviation of prediction errors is 9.788 (RMSE) from the regression line in training error check, it's mean the residuals mostly deviate between moreover 9.788

- Testing Error Check

* The standard deviation of prediction errors is 8.933 (RMSE) from the regression line in testing error check, it's mean the residuals mostly deviate between moreover 8.933. The value of RMSE in testing error is lower than training error. It's mean that our model is a good fit.  
