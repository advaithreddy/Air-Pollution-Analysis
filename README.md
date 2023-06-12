# Air Quality Analysis Project

In this experiment, the answers from a gas multisensor device that was placed in the field in an Italian city are analysed. For this research, Python is used to do some exploratory data analysis, a regression analysis, and model selection using Pandas, Numpy, Sesborn, and Scikit-learn. Each Python notebook has markdown that explains the various components of my investigation.


## About the Dataset

This dataset includes 9358 examples of hourly averaged responses from a group of five metal oxide chemical sensors that are built into an air quality chemical multisensor device. The gadget was situated on a field at road level in a heavily polluted part of an Italian city. Data were collected from March 2004 to February 2005 (a period of one year), making it the longest free recording of responses from on-field installed chemical air quality sensor devices. More about this [dataset](https://archive.ics.uci.edu/ml/datasets/Air+Quality)

### Dataset Features
Date (DD/MM/YYYY)
Time (HH.MM.SS)
CO(GT) - True hourly averaged concentration CO in mg/m^3 (reference analyzer)
PT08.S1 (tin oxide) hourly averaged sensor response (nominally CO targeted)
NMHC(GT) - True hourly averaged overall Non Metanic HydroCarbons concentration in microg/m^3 (reference analyzer)
C6H6(GT) - True hourly averaged Benzene concentration in microg/m^3 (reference analyzer)
PT08.S2 (titania) hourly averaged sensor response (nominally NMHC targeted)
NOx(GT) - True hourly averaged NOx concentration in ppb (reference analyzer)
PT08.S3 (tungsten oxide) hourly averaged sensor response (nominally NOx targeted)
NO2(GT) - True hourly averaged NO2 concentration in microg/m^3 (reference analyzer)
PT08.S4 (tungsten oxide) hourly averaged sensor response (nominally NO2 targeted)
PT08.S5 (indium oxide) hourly averaged sensor response (nominally O3 targeted)
T - Temperature in Â°C
RH - Relative Humidity (%)
AH - Absolute Humidity

## Regression Task

The task is to predict the Air Quality given the other measurements in the dataset.

The dataset has columns Date, Time, CO(GT), PT08.S1(CO), NMHC(GT), C6H6(GT), PT08.S2(NMHC), NOx(GT), PT08.S3(NOx), NO2(GT), PT08.S4(NO2), PT08.S5(O3), T, RH, and AH. The desired target variable is the temperature (T).

## Why Predict Air Quality

Being able to model, predict, and monitor air quality is becoming more and more relevant, especially in urban areas, due to the critical impact of air pollution on citizens’ health and the environment. Accurate forecasting helps people plan ahead, decreasing the effects on health and the costs associated.

## Findings

The regression model's R2 (coefficient of determination) value is 0.9299834598762752. or 93 percent, which indicates that 93 percent of the data points lie on the regression line and 93 percent of the independent/predictor variables in this model account for all the variance in y (temperature).

The residuals demonstrate that the residuals are dispersed yet relatively near the regression line.

The correlation between the temperature and the other characteristics is revealed by the coefficients. C6H6 falls by 0.41, PT08.S2(NMHC) increases by 0.009, NOx increases by 0.001, PT08.S3(NOx) lowers by 0.003, NO2 decreases by 0.003, PT08.S4(NO2) increases by 0.005, RH decreases by 0.349, and AH rises by 14.39 as the temperature rises by one degree.
The MSE is 5.18. In other words, the average squared difference between the observed and predicted values is 5.18.

The predictors aren't perfect but it is a good fit, given that ~93% of the independent/predictor variables in this model explain all the variation in y and the amount of error in a model isn't extreme. Therefore, the model fits the data well.

This model would be pretty accurate at predicting air quality, allowing people to plan ahead, decreasing the effects on health and the costs associated.
