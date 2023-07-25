# Prediction of Product Sales
## Analyzing and Predicting Item Outlet Sales
William Rodemoyer

Usung multiple variables, we are predicting the product sales. 

## Data
https://docs.google.com/spreadsheets/d/1J_xoCf9kXAQ6vPPmucROPlL2UUBkEgI6CbTzIr4Quw8/edit#gid=463301662
## Data Dictionary
![Project1 Data Dict](https://user-images.githubusercontent.com/128072861/236295067-9cf684ce-767d-4e56-a865-20e40e5b08c4.png)

## Exploratory Data Analysis
![image](https://user-images.githubusercontent.com/128072861/236299553-32ba21e3-0a8c-4a69-bb80-d62b0dacb965.png)


This Boxplot is comparing the 'Item_Outlet_Sales' by the Outlets size 

## Explanatory Visual Analysis
### Does visibility of items increase the item outlet sales?
![image](https://user-images.githubusercontent.com/128072861/236298892-3a465787-e443-4e8f-9bc3-91464e6220b1.png)


Item visibility does not increase outlet sales.
### What item type has the highest item outlet sales?

![image](https://user-images.githubusercontent.com/128072861/236299128-a68d07a4-54a0-4def-86f7-cbbee15330bf.png)

On average, Starchy Food items have the highest item outlet sales.
## Models
I used 2 mdoels to predict the product sales. 
  - Linear Regression Model
  - Decision Tree Model
## Final Model Results
After comapring the models, my recommended model is:
- Decision Tree Model

  - Decision Tree had the lower MAE (738.3173). Which means our models predictions were off by about 738.32.
  - The RMSE for our Decision Tree Model is lower as well. This means there are less outliers interfering with our model.

## LinearRegression

![image](https://github.com/wrodemoyer/Prediction-of-Product-Sales/assets/128072861/38f03de5-6ed3-44e0-bfcb-888272902d74)

- Coefficients that Positively Influence Final Grade:
    - **Outlet_Type_Supermarket Type3:** Type 3 Supermarkets increase item outlet sales by $585.45. 
    
    - **Outlet_Identifier_OUT027:** OUT027 outlets increases item outlet sales also by $585.45.
    

- Coefficient(s) that Negatively Influence Final Grade:

    - **Outlet_Type_Grocery Store:** Grocery stores decreased item outlet sales by $884.69.

## RandomTree Regressor

![image](https://github.com/wrodemoyer/Prediction-of-Product-Sales/assets/128072861/addb1012-b244-4d09-b697-800f7857ced3)

- Item_MRP is easily the single most important feature for predicting item outlet sales.


### For Further Informtion
For any additional questions, please contact wrodemoyer@gmail.com
