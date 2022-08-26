# House Rocket
![image](https://user-images.githubusercontent.com/97919969/186555599-c9fe683f-519d-4c01-a3aa-84ce37b346ac.png)










# Rossmann Store Salles Prediction
![img_sales](https://user-images.githubusercontent.com/97919969/187002748-1e0cb509-4ef9-43f8-bdbf-16a4da828b83.jpeg)


# 1.0 Context:
Rossmann is a company witch operates over three thousand drugs stores, in seven European countries.

# 2.0. BUSINESS PROBLEM

Buget definition for the refurbishment of stores.

Cause:

The current Sales Prediction displays many divergence;

The Sales Prediction process is based on pass experiences;

All of Sales Prediction has been done manually by 1.115 Rossmann Stores;

The visualisation of Sales is limited by computer;

# Solution:

Use Machine Learning to perform the Sales Prediction for all Stores;

The visualization of Salles Prediction can be seen by a Smartphone;

#Attribute List:

- Id - an Id that represents a (Store, Date) duple within the test set;
- Store - a unique Id for each store;
- Sales - the turnover for any given day (this is what you are predicting);
- Customers - the number of customers on a given day;
- Open - an indicator for whether the store was open: 0 = closed, 1 = open;
- StateHoliday - indicates a state holiday. Normally all stores, with few exceptions, are closed on state holidays. Note that all schools are closed on - public holidays and weekends. a = public holiday, b = Easter holiday, c = Christmas, 0 = None;
- SchoolHoliday - indicates if the (Store, Date) was affected by the closure of public schools;
- StoreType - differentiates between 4 different store models: a, b, c, d;
- Assortment - describes an assortment level: a = basic, b = extra, c = extended;
- CompetitionDistance - distance in meters to the nearest competitor store;
- CompetitionOpenSince[Month/Year] - gives the approximate year and month of the time the nearest competitor was opened;
- Promo - indicates whether a store is running a promo on that day;
- Promo2 - Promo2 is a continuing and consecutive promotion for some stores: 0 = store is not participating, 1 = store is participating;
- Promo2Since[Year/Week] - describes the year and calendar week when the store started participating in Promo2;
- PromoInterval - describes the consecutive intervals Promo2 is started, naming the months the promotion is started anew. E.g. "Feb,May,Aug,Nov" means - each round starts in February, May, August, November of any given year for that store

# 3. Solution Development

The method used for the project was CRISP-DM, apply as the steps below:

- Step 01. Data Description: The goal is to use statistical metrics to identify outliers in the business scope and also analyze basic statistical metrics such as: mean, median, maximum, minimum, range, skew, curtosis and standard deviation.

- Step 02. Feature Engineering: The goal of this step is to obtain new attributes based on the original variables, in order to better describe the phenomenon to be modeled.

- Step 03. Data Filtering: The goal of this step it to filter rows and delete columns that are not relevant for the model or are not part of the business scope.

- Step 04. Exploratory Data Analysis: The goal of this step is to explore the data to find insights and better understand the impact of variables on model learning.

- Step 05. Data Preparation: The goal of this step is to prepare the data prepare data for application of the machine learning model.

- Step 06. Feature Selection: The goal of this step is to select the better attributes to train the model. It was used Boruta Algorithm to make the selection.

- Step 07. Machine Learning Modeling: The goal of this step is to do the machine learning model training.

- Step 08. Hyperparameter Fine Tunning: The goal of this step is to choose the best values for each of the parameters of the model selected in the previous step.

- Step 09. Convert model performance to business values: The goal of this step is to convert model performance to a business result.

- Step 10. Deploy Model to Production: The goal of this step is to publish the model in a cloud environment so that other people or services can use the results to improve the business decision. The cloud application platform choosed was Heroku.

- Step 11. Telegram Bot: The goal of this step is to create a bot on the telegram app, that make possible to consult the forecast at any time.

# Mind Map

![mindmap](https://user-images.githubusercontent.com/97919969/187002839-33f607e7-9cc3-4cc1-8285-582b383080ac.png)

# Hipothesys List

- Stores with biggest assortment should sell over/more.
- Stores with competitors around should sell less.
- Stores with longer competitors should sell over/more.
- Stores with activate promotion for more time should sell over/more.
- Stores with more promotion days should sell over/more.
- Stores with consecultive promotion should sell over/more.
- Opened stores on Christimas holliday should sall over/more.
- Stores should sell more throughout the year.
- Stores should sell more on the second semestre of the year.
- Stores should sell more after 10th day of eatch month.
- Stores should sell less on wekeends.
- Stores should sell less on hollidays school.
- Best Insights

# H1. - Stores with biggest assortment should sell more.

FALSE Screen Shot 2022-05-05 at 6 53 12 AM

# H2. - Stores with competitors around should sell less.

FALSE Screen Shot 2022-05-05 at 6 56 32 AM

# H3 - Opened stores on Christimas holliday should sall over/more.

FALSE

Screen Shot 2022-05-05 at 6 58 49 AM

# H4. - Stores should sell more after 10th day of eatch month.

TRUE Screen Shot 2022-05-05 at 7 01 11 AM

# Tested Machine Learning Models

- Average Model
- Linear Regression Model
- Linear Regression Regularized Model (Lasso)
- Random Forest Regressor
- XGBoost Regressor
- Machine Learning Model Performance

Screen Shot 2022-08-26 at 9 25 29 AM

# Machine Learning Performance after Hyperparemeter Fine Tuning

Screen Shot 2022-08-26 at 8 35 08 AM

Although the Random Forest Regressor Model presented better performance, this model usually requires a large amount of space on the server in deploy step, generating a significant cost increase for the company. Therefore, it was choosen the XGBoost Regressor Model, which after the hyperparameter fine tuning presented similar performance and requires less space on the server, generating a lower cost for the company.

# Business Performance vs Value

In addition to overall sales prediction, it was also calculated the sales prediction for the worst and the best scenario.
<img width="357" alt="Screen Shot 2022-08-26 at 9 50 20 AM" src="https://user-images.githubusercontent.com/97919969/187002912-2454cbb8-2ecc-4b66-8f50-6c430f3e292d.png">


# How to access the prediction

Sign up Telegram and create an account

# Telegram

To acess the predictions on Telegram, click in the below:

https://web.telegram.org/z/#5356439509

# How to get the prediction

- Send the store number (one each time) and get the sales prediction for the next six weeks.
- If the store number does not exist, it will get as an answer the message: "Store Not Available".
<img width="1012" alt="Screen Shot 2022-08-26 at 9 05 30 AM" src="https://user-images.githubusercontent.com/97919969/187002958-36bbe474-26f2-4d04-92b8-a7ba50a969f2.png">


# Conclusion

Considering the first CRISP-DS cycle, the final model presented a usefull performance, considering the MAPE (Mean Absolute Percentage Error) of 0.12. However, for some stores, higher MAPE values were observed, such as 0.37 and 0.52, but this is a point that could be improved in the next CRISP cycle.

# Technologies:

- Jupyter notebook
- Python
- Telegram
- Deploy into production

# Deploy into Production
- Back end: Heroku
- Front end web: Telegram
- Database: Kaggle

#Contact
https://www.linkedin.com/in/adriele-pinto/



