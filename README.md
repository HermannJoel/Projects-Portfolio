#### Projects-Portfolio
Examples of real life data machine learning projects


#### [PROJECT 1: DECOMPOSING THE DIFFERENCE IN EXPECTED INFLATION: Project Overview](https://github.com/HermannJoel/Finance/tree/main/Inflation-Expectation-Prediction/src)

##### 1.Problem Definition

 Built regression models to predict US inflation. This can be usefull for an asset
 manager who is managing a portfolio sentitive to Inflation.
##### 2.Data

The Original data set is the FED NY Survey of Expected Inflation. It can be download here [NYFED](https://www.newyorkfed.org/microeconomics/sce#/) and contains 3 sets.

* Complete Microdata 2013-2016.csv - Survey participants attributes examples up to 2016 (close to 250,000 examples with 260+ different attributes, including mean expected inflation which is the target variable).

* Complete Microdata 2017-2019.csv - Survey participants attributes examples from January 1 2017 to Dec 30 2019 (close to 170,000 examples with the same attributes as Complete Microdata 2013-2016.csv).
  
* Complete Microdata 20-present.csv - Survey participants attributes examples from January 2020 to June 2020 (close to 7,713 examples with the same attributes as the 2 previous data sets)

A description of the questionnaire and the name of the differents attributes can be found here.[Questionnaire](https://www.newyorkfed.org/medialibrary/interactives/sce/sce/downloads/data/frbny-sce-survey-core-module-public-questionnaire.pdf).

##### 3.Techniques

* The main performance metric is the MSE(Mean Squarred Error).
 Out of 400,000+ examples, only 17,000+  heave unique userid. In order to use all attributes in our model, we 
 should filter our data set by userid. The final data set contains only 17,000+ examples.
 
* The target variable is a continiuos variable. It requires regression models. 

We will implement 8 diffrents machine learning algorythms:`decisiontreeRegressor`, `randomforestRegressor`, `Ridge Regression`, `adaboostRegressor`, `lightgbmRegressor`, `GradientBoostingRegressor`, `XGBRegressor`, `CatBoostRegressor`.

##### 4.Implementation
* After data cleansing and features engineering, the final data set contains ~ 15799 observations and 160 variables.
* In R, I run a stepwise selection to select only important varaiables, 94 variables out of 160 appeared to be important at predicting inflation.
* Use a GridSearchCV to search for optimal parameters.

##### 5.Results
* Catboost regressor yielded de lowest Mean Squarred Error. 


<img src="https://render.githubusercontent.com/render/math?math=MSE=26.89">. 

<img src="https://render.githubusercontent.com/render/math?math=MAE=3.29">.

and 

<img src="https://render.githubusercontent.com/render/math?math=R^2=12.29">.

![](/Images/mse.png)

![](/Images/results.png)

* Features Deflation i.e. peoples who expet an Deflation and thefeature College i.e. participants that with an educationnal background equal or higher than college appear to be most usefull features at predicting inflation.

![](/Images/features-importance.png)
