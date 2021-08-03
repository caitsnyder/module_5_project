# Predicting Dengue: Module 5 Project ReadMe


## Overview
Dengue is a mosquito-borne disease endemic to many tropical countries, including Puerto Rico and Peru.

## Research question
Given weekly dengue case counts in Puerto Rico and Peru, can we accurately predict future weekly case counts?

## Data
The non-profit site DrivenData has made this dengue case count dataset available as part of an ongoing challenge, DengAI. The data can be found at https://www.drivendata.org/competitions/44/dengai-predicting-disease-spread/ . Additional outside variables were introduced to the analysis: wet season and global warming phases.

## Methods
This project uses linear regression to predict case counts in the cities of San Juan, Puerto Rico, and Iquitos, Peru.

The data were cleaned per the following steps:
- A threshold of 3 standard deviations was used to drop outliers
- A threshold of 0.8 r was used to eliminate multicolinear variables
- Kertsosis analysis was used to eliminate variables that did not have a linear relationship with the outcome variable.

The anaylsis was then conducted using LinearRegression, GradientBoostingRegressor, and AdaBoostRegressor.
Model performance was measured using r^2, MSE, and MAE.

## Results
Station preciptitation (measured in mililiters) proved to be the most important predictor.
Of the three models compiled, our GradientBoostingRegressor model performed best, yielding the following statistics:
- r^2: 0.80121
- MSE: 5.79827
- MAE: 2.00905

## Take-aways
Our model indicates that moist, warm environmental conditions are more likely to co-occur with higher dengue case counts.
Travelers with the privilege to choose their time of travel should avoid tropical climates during wet season when possible.
Residents and travelers without flexibility should sleep under mosquito nets and seek a medical opinion at the first sign of dengue symptoms.

## Future avenues for exploration
Additional analysis might explore the following questions:
- What is the influence of population density on dengue case rates?
- What is the influence of mosquito net distributions on dengue case rates?
- What is the influence of water source and quality on dengue case rates?