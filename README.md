# Prediction of Product Sales
## Analyzing sales based on products and store outlets.  

**Nena Esaw**: 

The goal is to help the retailer understand the properties of products and outlets that play crucial roles in increasing sales.


### Data:
Big Mart Sales [https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/](https://)

For this dataset, there were 8523 rows and 12 columns.

![Data_Dictionary](https://github.com/nenarossbce/Prediction-of-Product-Sales/assets/134180290/f2d7ff6d-2a2f-448c-a6d8-6aa2924965f3)


## To perpare this data, the data was cleaned, and the following processes were performed:

### Exploratory Data Analysis
- During the exploratory data analysis, a boxplot and histogram were visualized for each numeric datatype column. 
- Also, a barplot was visualized for each categorical column. 
- This gave a good baseline for all of the numeric and categorical columns for univariate EDA.

#### Distribution of Item Outlet Sales
![item_outlet_sales](https://github.com/nenarossbce/Prediction-of-Product-Sales/assets/134180290/e41d6e89-86cd-4cff-9dfe-672aff8cb34a)

> This histogram shows the total outlet sales. 

#### Explanatory Data Analysis 
- To visualize the data for explantory purposes, three bargraphs were chosen and one linegraph was chosen.
- The bargraphs were chosen to show how the categories compare to each other. 
- Finally, a linegraph was chosen to show the trend of salaries over the past three years. 

## Model
![outlet_type_vs_item_outlet_sales](https://github.com/nenarossbce/Prediction-of-Product-Sales/assets/134180290/c549a424-a874-4d1e-a199-5bfc3cd44d5a)

- This bargraph is showing sales based on outlet type.
- We can see that Supermarket Type3 produces the most sales.
- Supermarket Type3 has had sales as high as $12,000. 
  
![outlet_type_vs_item_outlet_sales](https://github.com/nenarossbce/Prediction-of-Product-Sales/assets/134180290/2018cf23-6906-4717-8dbc-2aaed1bf880b)

- This bargraph shows that majority of the products bring in an average of $2,000 in sales.

![outlet_identifier_vs_item_outlet_sales](https://github.com/nenarossbce/Prediction-of-Product-Sales/assets/134180290/cbbc4c74-9ffd-4c53-8ac9-00e0724a0902)

- we can see from the is bargraph that Out027 brings in the most sales.
- OUT019 and OUT010 has the least amount of sales.

![item_mrp_vs_item_outlet_sales](https://github.com/nenarossbce/Prediction-of-Product-Sales/assets/134180290/73cf7dfa-87fd-4cc7-8a3e-b409c12e6d6b)


###Machine Learning Using the Following models:
-Linear Regression Model
-Random Forest Regressor Model
-Tuned with GridSearchCV

###Models Evaluated & Results 
* Linear Regression Model (Testing Set):
  *  R^2 = 0.566
  *  MAE = 806.585
  *  MSE = 1198207.745
  *  RMSE = 1094.627
 
* Random Forest Regression Model (Testing Set):
  *  R^2 = 0.514
  *  MAE = 800.701
  *  MSE = 1341616.263
  *  RMSE = 1158.282

* Tuned with GridSearchCV (Testing Set):
  *  R^2 = 0.591
  *  MAE = 735.319
  *  MSE = 1,128,461.481
  *  RMSE = 1,062.291
 
* The final model that was chosen was the GridSearchCV Model with an estimator tuned to 50.
* The Mean Absolute Error was off by $735.32.
* The Mean Squared Erro was $1,128,461.48.
* The Root Mean Squared had a calculation of $1,062.29

The model can be used to determine which outlet produces the most sales and which store are not doing so well. 

## Recommendations:
* Look into closing stores that are underperforming.


## Limitations & Next Steps

This information can be useful to determine how to generate more sales in the outlet stores by looking at trends and performance. 


### For further information

For any additional questions, please contact:
**nenarossbce@gmail.com**
