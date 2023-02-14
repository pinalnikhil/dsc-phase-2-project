## King County House Prices 
Author: Pinalben Patel

![image](https://user-images.githubusercontent.com/119024066/218669940-36bf22f8-3670-46ab-9688-6f2baeb17653.png)


## The Data
The King County Housing Data Set contains information about the size, location, condition, and other features of houses. Let's check the columns of the data set.

* date - Date house was sold
* price - Sale price (prediction target)
* bedrooms - Number of bedrooms
* bathrooms - Number of bathrooms
* sqft_living - Square footage of living space in the home
* sqft_lot - Square footage of the lot
* floors - Number of floors (levels) in house
* waterfront - Whether the house is on a waterfront
* view - Quality of view from house
* condition - How good the overall condition of the house is. Related to maintenance of house
* grade - Overall grade of the house. Related to the construction and design of the house
* sqft_above - Square footage of house apart from basement
* sqft_basement - Square footage of the basement
* yr_built - Year when house was built
* yr_renovated - Year when house was renovated
* zipcode - ZIP Code used by the United States Postal Service

## Business Problem:
RGB need to provide prospective home sellers with guidance on how to improve the value of their home prior to listing, including the predicted increase in value expected based on improvements to features. The results can inform home owners interested in selling their homes about the most important factors to consider for improving sale prices.

## Methods
* The Data
* Data cleaning and pre-processing.
* Exploring the data
* Building regression models 
* Validation of the model
* Result

All that remains in Phase 2 is to put our newfound data science skills to use with a large project! This project should take 20 to 30 hours to complete.

## Project Overview

For this project, you will use regression modeling to analyze house sales in a northwestern county.

## The Data

This project uses the King County House Sales dataset, which can be found in  `kc_house_data.csv` in the data folder in this repo. The description of the column names can be found in `column_names.md` in the same folder. As with most real world data sets, the column names are not perfectly described, so you'll have to do some research or use your best judgment if you have questions about what the data means.

It is up to you to decide what data from this dataset to use and how to use it. If you are feeling overwhelmed or behind, we recommend you ignore some or all of the following features:

* date
* view
* sqft_above
* sqft_basement
* yr_renovated
* zipcode
* lat
* long
* sqft_living15
* sqft_lot15

## Data Processing

To assist with creating good models, we completed some data cleaning including:
* Dropping unrelated features to our model.
* Creating dummy variable, log transfer and features skilling.
* Checking correlation in between the variable.

## Histogram!

![image](https://user-images.githubusercontent.com/119024066/218675966-79986aa3-dc5d-422c-a22d-81c7c69d8c6c.png)


Many of the variables do not follow a normal distribution, and the scales are dramatically different for some variables. This may create issues with satisfying all regression assumptions, but we'll address those issues as they arise. Regression does not require features to be normally distributed.

## Checking correlations

![image](https://user-images.githubusercontent.com/119024066/218676154-5fcc8fcf-0772-4332-b970-2a3e54140499.png)

The three factors that together best predict a home's price in King County are square footage, grade, and bathrooms. The final multiple regression model includes these features. There is no clear linear relationship between a home's "floors," "bedrooms," and "waterfront." The multiple regression model will include sqft living because it has a stronger linear correlation with price than sqft lot.

## Multicollinearity

![image](https://user-images.githubusercontent.com/119024066/218676288-4cba4930-c068-4eb2-a697-bb3aa3f73f99.png)

price          1.000000
grade          0.635934
sqft_living    0.627438
bathrooms      0.460266
bedrooms       0.298955
floors         0.273616
sqft_lot       0.097296
yr_built       0.063956
waterfront     0.055232
condition      0.035714

Here we can clerly see that which variable have good reletionship with independed variable price.

## Model 

We are showing correlation and using regression coefficients in this analysis to be able to show the relationship between one or more features with sale price.

Using regression and interpreting correlation coefficients is effective for this business problem because it will allow for us to determine how sale price is impacted by different features and to what degree.

Buildng complex models with multiple features allows for us to be able to make more accurate, data-driven predictions.

## Recommendations
 
Homeowners interested in selling their homes should focus on improving the design and quality of construction of their homes, which may in turn improve their home grade. They should try to increase the amount of living space on the land, perhaps by adding more bathrooms. Although homeowners probably have less control over it, the square footage of peoples' homes is also a very good predictor of price. Encourage your colleagues to increase the square footage of their homes to further raise the selling price of your house.

## Limitations and Next Steps

The model does have some limitations: any new data used with the model would need to go through a similar pretreatment step because some of the variables needed to be log-transformed to satisfy regression assumptions. Additionally, the model's applicability to data from other counties may be constrained due to regional variations in home prices. Because outliers were eliminated, the model might also be unable to predict extreme values. Future research should examine both homes with high price values and the best indicators of home prices outside of King County.

