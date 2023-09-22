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

## Model Insights 

### LinearRegression coefficients plot: 

![Linear_Regression_coefficient_plot](https://github.com/nenarossbce/Prediction-of-Product-Sales/blob/main/top_15_coeffs.png)

* Outlet_Type_Supermarket Type 3 positively influence the model. Type 3 stores show to bring in the most revenue. These stores increase revnue by $1624.81.

* Item_MRP positively influences the model. Item_MRP increases value by $984.32.  

* Outlet_Type_Grocery Store negatively impacts the model. The grocery store seems to bring in the least amount of revnue. Grocery store decrease the revnue by $1741.07

### Random Forest Feature Importances: 

![RF_Feature_Importances_plot](https://github.com/nenarossbce/Prediction-of-Product-Sales/blob/main/rf_importances.png)


Top 5 Important Features from our Random Forest model 

* Item MRP is the most important feature 

* Outlet Type Grocery Store second most important 

* Item Visibility 

* Outlet Type Supermarket Type 3  

* Item Weight 


### Explaining Models with Shap


#### Global Explanations

![SHAP_Summary_Bar_plot](https://github.com/nenarossbce/Prediction-of-Product-Sales/blob/main/shap_summary_bar.png)

* The shap summary is showing the same 5 but the order for Item Visibility and Supermarket Type 3 are in ranking differently. The Tree model has Supermarket Type 3 in 4 and Item Visibility in 3, while the SHAP summary has Supermarket Type 3 in 3 and Item visibility in 4. 

![SHAP_Summary_dot_plot](https://github.com/nenarossbce/Prediction-of-Product-Sales/blob/main/shap_summary_dot.png)

* Item MRP is increasing as the SHAP value increases. This seems to have a positive effect on our model. 

* Outlet Type Grocery Store is a one hot-encoded, the blue is positively effecting the model and the red is negatively decreasing the models predictions. The blue seems to be more impactful in the model predictions of revnue. 

* Supermarket Type 3 is one hot encoded and the blue is negatively impacting the models predictions and the red is postively impacting the predicions. 

### Local Explanations:
![lr_exp_plot](https://github.com/nenarossbce/Prediction-of-Product-Sales/blob/main/linreg_explainer.png)

* The model shows that grocery type and supermarket type heavily impact our model in a positive way. Grocery store type shows to improve the model by $1,670. Item MRP impacts the model in a negative way by $680.62. 

![lr_exp_plot](https://github.com/nenarossbce/Prediction-of-Product-Sales/blob/main/lr_force_plot.png)

* This force plot is showing that our linear regression model is supermarket type 3 our red values are increasing the value of our model. The Item MRP is reducing the value of our model. 


## Recommendations:
* Look into closing stores that are underperforming.


## Limitations & Next Steps

This information can be useful to determine how to generate more sales in the outlet stores by looking at trends and performance. 


### For further information

For any additional questions, please contact:
**nenarossbce@gmail.com**
