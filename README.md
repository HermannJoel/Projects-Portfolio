# Projects-Portfolio
Examples of real life data machine learning projects


# [PROJECT 1: DECOMPOSING THE DIFFERENCE IN EXPECTED INFLATION: Project Overview](https://github.com/HermannJoel/Finance/tree/main/Inflation_Expectation)

## Problem Definition:

 Built regression models to predict US inflation. This could be usefull for a asset
 manager who is managing a portfolio sentitive to Inflation.
 ## Data:

* The data set is from the FED NY Survey of Expected Inflation
* The original data set can be download here [NYFED](https://www.newyorkfed.org/microeconomics/sce#/) and
  contains 3 sets

  Complete Microdata 2013-2016.csv - Survey participants attributes examples up to 2016 (close to 250,000 examples with 260+ different attributes, including mean expected inflation which is the target variable).

  Complete Microdata 2017-2019.csv - Survey participants attributes examples from January 1 2017 to Dec 30 2019 (close to 170,000 examples with the same attributes as Complete Microdata 2013-2016.csv).
  
  Complete Microdata 20-present.csv - Survey participants attributes examples from January 2020 to June 2020 (close to 7,713 examples with the same attributes as the 2 previous data sets)

* A description of the questionnaire and the name of the differents attributes can be found here.[Questionnaire](https://www.newyorkfed.org/medialibrary/interactives/sce/sce/downloads/datafrbny-sce-survey-core-module-public-questionnaire.pdf).

## Techniques:

*The main performance metric is the MSE(Mean Squarred Error)
*Out of 400,000+ examples, only 17,000+  heave unique userid. In order to use all attributes in our model, we
    should filter our data set by userid. The final data set contains only 17,000+ examples.  
*predicted inflation using 2 methods

 *1st method: Implemented with R a stepwise selection, Only 60 attributes appeared to be usefull
  *Used a pipeline to find the best parameters of 2 models simustaneously, tha DecisionTreeRegressor and RandomForestRegressor
  *Compared the MSE of the RandomForestRegressor with a Ridge regression MSE RandomForest MSE < Ridge MSE. The RandomForest achieved a slightly lower `MSE=22.11` and a higher `$$R^2$$=12.13` on the test set than the Ridge `MSE=22.31` `$$R^2$$=11.35`

![](/Images/Results1.png)

*2nd method: I implemented a RandomForestRegressor with all features and compared the MSE and MAE with the previous models results.

  *Features Inflation, Deflation, Loan12m:Much Harder and College appear to be most usefull features at predicting inflation.
  *The Ridge regression with all attributes yielded MSE=22.99 and `$$R^2$$=15.74`.

![](/Images/Results2.png)
