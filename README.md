# Project Name
> House Price Predictore


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)


<!-- You can include any other section that is pertinent to your problem -->

## General Information
- A US-based housing company named Surprise Housing has decided to enter the Australian market.
- The company is looking at prospective properties to buy to enter the market. 
- This project analyses the data to model the house prices and the factors which affects the house prices in Australia.
- train.csv data is used which holds the house prices data and various attributes of the house

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Conclusions
- Simple Linear regression was attempted and it was found that due to complexity of data set the model was overfitting
- Initial attempts to reduce the complexity was made using RFE (Recursive feature elimination), which improved the model a bit but overfitting was still present
**Ridge Regression** 
  - With ridge regression [GrLivArea, OverallQual, LotArea, Condition2_PosN, YearBuilt, TotalBsmtSF, TotalBsmtSF, TotalBsmtSF, PoolArea_Yes, BsmtFullBath] were found to be top 10 parameters impacting house price
  - There were total 60 parameters (limited by RFE) which impacted the house price
  - R2 of 86% and Adjusted R2 of 83% was observed on test data which was class to 88% R2 found on training data
  - RMSE of ~23K was observed which is good considering house prices are in millions
  - Hyper parameter value: Best alpha for Ridge Regression: {'alpha': 2.1}
**Lasso Regression**
  - With Lasso regression only 29 parameter were found to have non-zero coefficient, which improved the interpretability of the model
  - [GrLivArea, OverallQual, LotArea, Condition2_PosN, YearBuilt, OverallCond, GarageCars, BsmtFullBath, TotalBsmtSF, PoolArea_Yes] were found to be top 5 parameters impacting house price
  - Condition2_PosN is in top 5 parameters but with negative coefficient implying inverse proportionality with sale price
  - R2 and Adjusted R2 were observed similar to Ridge model i.e 86% and 83% respectively
  - RMSE observed is also similare to Ridge model i.e. 23k
  - Hyper parameter value: Lasso(alpha=0.00075)

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->


## Technologies Used
- Pandas
- scikit learn
- matplotlib
- sns

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->




## Contact
Created by [@githubusername] - feel free to contact me!

