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
  RMSLE of $xxxK

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

* The techniques used in here have been inspired and adapted from []()
* Created regression models that predict the inflation given the FED NY Survey of Consumers Expectations.
* There are 2 datasets: the original data set can be download here [NYFED](https://www.newyorkfed.org/microeconomics/sce#/).

  Complete Microdata 2013-2016.csv - Survey participant predicted inflation examples up to 2016 (close to 250,000 examples with 260+ different attributes, including mean
  extected inflation   which is the target variable).
  Complete Microdata 2017-2019.csv - Survey participants predicted inflation examples from January 1 2017 to Dec 30 2019 (close to 170,000 examples with the same attributes as
  Complete Microdata 2013-2016.csv).
* A description of the questionnaire and the name of different attribute can be found here.[Questionnaire](https://www.newyorkfed.org/medialibrary/interactives/sce/sce/downloads/data/frbny-sce-survey-core-module-public-questionnaire.pdf).

* The main performance metric is the MSE(Mean Squarred Error)
* Out of 400,000 examples, only 17,000+ have unique id, participant responded to queation regarding attribute as Education Level or Sex only once. Consequently, similar
  attribute have a lot of missing values. In order to use such participant attribute in our model, we have to filter our data set by UserId; our final data set contains only
  17,000+ examples.  
* After preprocessing the data and do some features engineering, I employed 2 methods
  - The 1st method consisted at implementing with R a stepwise selection. From 200+ attributes only 60 appeared to be usefull
* I used a pipe line to find the best parameters of 2 models simustaneously namely DecisionTreeRegressor and RandomForestRegressor 
* Then compared the MSE of the RandomForestRegressor with a Ridge regression MSE
  ![RandomForestVsRidge](https://github.com/HermannJoel/Data_Scientist/blob/master/Pictures/Results1.png)
  
  RandomForest MSE < Ridge MSE. The RandomForest achieved a slightly lower MSE=22.11 and a higher R^2=12.13 on the testing data than the Ridge MSE=22.31 R^2=11.35  
  - With the second method, I implemented a RandomForestRegressor with all features and compared the MSE and MAE with the previous models    
  ![RandomForestVsRidge](https://github.com/HermannJoel/Data_Scientist/blob/master/Pictures/Results2.png)
  
  The Ridge will all attribute achieved a MSE=22.99 and R^2= 15.74   
---
