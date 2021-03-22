# Housing Analysis

## Overview

This project analyzes the housing data from houses sold in King County for 2014 and 2015 and creates a model to predict sale price based on various variables.

## Business Problem

A real estate company is interested in current trends affecting housing sales, particularly among middle class homes. The company wants to know how to most effectively price their houses. 

## Data Understanding

This section focuses on exploring the data from King County House Sales for 2014 and 2015. The data includes a multitude of variables, including data sold, price, bedrooms, bathrooms, square footage of living area, lot, basement, above area, as well as average square foot for neighboring areas, grade, condition, renovation year, views, location, and waterfront.

The data is extensive and has various possible predictors available for price.

## Data Preparation

I drop the top 10% most expensive houses in order to focus on middle class and lower homes. I convert drop unnecessary variables, replace null values with the mode, and use one-hot encoding on categorical values (zipcode and waterfront). 

I check for linearity, apply log function to some of the data, and scale the data so that it's all on the same magnitude. 

## Model

I create several models, refine them, and decide on the most effective one. This model has a R2 value of .809, showing good fit.

The mean of the residuals graph is centered around 0, showing that the model does not have systematic bias.

The Train and Test mean squared errors are 0.19 and 0.188, which is good as they do not show a big difference between each other.

![picture](images/Normality.jpg)

## Correlations

Square foot of living area, grade, and bathrooms are 3 variables highly correlateted with price. This means that real estate agents could focus on this when pricing houses.  They could also recommend potential sellers to add a bathroom onto the house or improve the grade by improving construction/design. 

![picture](images/corr.jpg)
![picture](images/Grade.jpg)
![picture](images/bathrooms.jpg)
![picture](images/sqft_living.jpg)


## Conclusions

I chose the first model above as my model, rather than the refined version (model200) that was formed from removing outliers. I made this decision because the r2 value was higher in the top model, and the mean of the residuals was closer to 0. R2 describes how strong the relationship is between my model and the dependent variables. This model has a R2 value of .809, showing good fit.

The mean of the residuals graph is centered around 0, showing that the model does not have systematic bias.

The Train and Test mean squared errors are 0.19 and 0.188, which is good as they do not show a big difference between each other.

This model struggles with very high and very low values, meaning it should not be used to estimate sales price for those homes.

Square foot of living area, grade, and bathrooms are 3 variables highly correlateted with price. This means that real estate agents could focus on this when pricing houses. They could also recommend potential sellers to add a bathroom onto the house or improve the grade by improving construction/design.

## For More Information

Please review my full analysis in my [Jupyter Notebook](housing-analysis.ipynb) or my [presentation](Housing-Analysis-Presentation.pdf).

## Repository Structure
- README.md <- The top-level README for reviewers of this project. 
- housing-analysis.ipynb <- Narrative documentation of analysis in Jupyter Notebook
- Housing-Analysis-Presentation.pdf <- PDF version of project presentation 
- data <- Data used for the code
- Images <- images generated from the code 
