# Projects-Portfolio
Examples of real life data machine learning projects to showcase my programming and data science skills 

# [PROJECT 1: BULLDOZER SALE PRICE PREDICTION USING LINEAR REGRESSION: Project Overview](https://github.com/HermannJoel/Finance/tree/main/Bulldozer%20Sale%20Price%20Prediction)

* The techniques used in here have been inspired and adapted from [Mrbourke]()
* Created a regression model that predict the future sale price of a bulldozer based given its characteristics previous examples of how much similar bulldozers have been sold     for.
* There are 3 datasets:
  Train.csv - Historical bulldozer sales examples up to 2011 (close to 400,000 examples with 50+ different attributes, including SalePrice which is the target variable).
  Valid.csv - Historical bulldozer sales examples from January 1 2012 to April 30 2012 (close to 12,000 examples with the same attributes as Train.csv).
  Test.csv - Historical bulldozer sales examples from May 1 2012 to November 2012 (close to 12,000 examples but missing the SalePrice attribute, as this is what we'll be trying    to predict).
* The main performance metric is the RMSLE(Rot Mean Squarred Log Error)  
* Find Hypertuning parameter using RandomizedSearchcv
* Trained and test the model with sales data up to 2011 and validated the model with sales data from May 1 2012 to November 2012 and succeded to predict buldozer price with a
  MSE of $5979.24 a RMSLE of 0.24 and R^2 of 0.88.
* Bulldozer YearMade, ProductSize and SaleYear appear to be the most important features at predicting Bulldozer sale price 

---

# [PROJECT 2: CRM CUSTOMERS CLUSTERING USING PCA and K-MEANS: Project Overview](https://github.com/HermannJoel/Finance/tree/main/Customers%20Clustering%20using%20K-Means)

* Overview
* Created PowerBi daschboard to showcase the different cluster

[PowerBi dashboard clusters](https://github.com/HermannJoel/Finance/blob/main/Customers%20Clustering%20using%20K-Means/Customers_Clusters_Dashboard.pbix)

---
# [PROJECT 3: BANK CUSTOMERS CHURN PREDICTION USING LOGISTIC REGRESSION: Project Overview](https://github.com/HermannJoel/Finance/tree/main/Bank_Customers_Churn_Prediction)

* Overview
* Created PowerBi daschboard to showcase the different cluster

[PowerBi dashboard clusters](https://github.com/HermannJoel/Finance/blob/main/Bank_Customers_Churn_Prediction/Bank_Customers_Churn.pbix)

---

# [PROJECT 4: CREDIT RISK MODELLING: Project Overview](https://github.com/HermannJoel/Finance/tree/main/Credit_Risk_Modeling)

* Overview

---

# [PROJECT 5: DECOMPOSING THE DIFFERENCE IN EXPECTED INFLATION: Project Overview](https://github.com/HermannJoel/Finance/tree/main/Inflation_Expectation)

* For this project I built regression models to predict the inflation. This could be usefull for a asset manager who is managing a portfolio sentitive to Inflation.
* The data set is from the FED NY Survey of Expected Inflation
* The original data set can be download here [NYFED](https://www.newyorkfed.org/microeconomics/sce#/) and contains two sets

  Complete Microdata 2013-2016.csv - Survey participants attributes examples up to 2016 (close to 250,000 examples with 260+ different attributes, including mean
  expected inflation which is the target variable).
  
  Complete Microdata 2017-2019.csv - Survey participants attributes examples from January 1 2017 to Dec 30 2019 (close to 170,000 examples with the same attributes as
  Complete Microdata 2013-2016.csv).
* A description of the questionnaire and the name of different attribute can be found here.[Questionnaire](https://www.newyorkfed.org/medialibrary/interactives/sce/sce/downloads/data/frbny-sce-survey-core-module-public-questionnaire.pdf).

* The main performance metric is the MSE(Mean Squarred Error)
* Out of 400,000 examples, only 17,000+ have unique userid, participant responded to question regarding attribute as Education Level or Sex only once. Consequently, similar
  attribute have a lot of missing values. In order to use such participant attribute in our model, we have to filter our data set by userid; our final data set contains only
  17,000+ examples.  
* A was able to predict inflation using 2 methods
* 1st method: I implemented with R a stepwise selection, Only 60 appeared to be usefull
* I used a pipe line to find the best parameters of 2 models simustaneously, tha DecisionTreeRegressor and RandomForestRegressor 
* Compared the MSE of the RandomForestRegressor with a Ridge regression MSE
  RandomForest MSE < Ridge MSE. The RandomForest achieved a slightly lower MSE=22.11 and a higher R^2=12.13 on the testing data than the Ridge MSE=22.31 R^2=11.35
  
![](/Images/Results1.png)

* 2nd method: I implemented a RandomForestRegressor with all features and compared the MSE and MAE with the previous models results.
* Features Inflation, Deflation, Loan12m:Much Harder and College appear to be most usefull features at predicting inflation.
* The Ridge regression will all attribute yielded MSE=22.99 and R^2= 15.74.
  
![](/Images/Results2.png)


---
