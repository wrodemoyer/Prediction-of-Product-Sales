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

## Explaning Models with SHAP

### Bar Summary Plot
![image](https://github.com/wrodemoyer/Prediction-of-Product-Sales/assets/128072861/05b58509-fbe4-4e39-b702-415b99565411)

**Comparing our most important features according shap vs. orginal feature importance**

- SHAP top 5
    - item_mrp
    - outlet_type_grocery store
    - outlet_identifier_OUT027
    - outlet_type_supermarket type3
    - item_visibility 
- Orginal top 5
    - item_mrp
    - outlet_type_grocery store
    - item_visibility
    - item_weight
    - outlet_identifier_OUT027


- we see a some similarities.
- both have item_mrp & outlet_type_grocery store are the 1 & 2 most important features. 
- both have item_visibility and outlet_identifier_OUT027 in their top 5, but in different spots.
    - shap
        - outlet_identifier_OUT027 is 3rd
        - item_visibility is 5th
    - orginal
        - outlet_identifier_OUT027 is 5th
        - item_visibility is 3rd
- the differences is shap has outlet_type_supermarket type3 in its top 5, while the orginal has item_weight in its top 5.


### Dot Summary Plot

![image](https://github.com/wrodemoyer/Prediction-of-Product-Sales/assets/128072861/20594977-fdd4-4d2d-9595-1bd1bca04281)

**Top 3 Features Observations**

Red Dots= Higher Values

Blue Dots= Lower Values

- item_mrp
    - most important feature
    - the red dots(higher values) are on the positive side, so item_mrp helps in the increase of item outlet sales. 
    

- Outlet_Type_Grocery Store
    - the red dots for this feature are clearly on the negative side. This has a negative effect on our target. 
    - so grocery stores decrease our item outlet sales. 
    
    
- Outlet_Identifier_OUT027
    - We have positive red dots for this feature(positive effect). 
    - This store ID increases our item outlet sales. 

## Local Explanations

### Selected Examples
- Examples: **Outlet_Types**
    - Grocery Stores
    - Type3 Supermarkets

    
- Grocery Stores have our lowest sells while Type3 Supermarkets have the highest. 
- Lets see what other features contribute to these results.

### LIME


**Grocery Store**

<img width="899" alt="Outlet_Type-Grocery Store" src="https://github.com/wrodemoyer/Prediction-of-Product-Sales/assets/128072861/4e95b14f-5922-4392-bdc5-5c1d9ff2e9bd">

- Outlet_Type_Grocery Store most influenced by:
    - Outlet_Type_GroceryStore, Item_MRP,Outlet_Identifier_OUT027, Outlet_Type_SuperMarket Type3, and Item_Type_Seafood(All Negative).
    - We have 1 feature that is positive, but it is definitely outweighed by negatives.


**Supermarket Type3**

<img width="915" alt="Outlet_Type-Super Market" src="https://github.com/wrodemoyer/Prediction-of-Product-Sales/assets/128072861/c998ad49-c677-45d2-a003-fa7ca5edd05d">

- Outlet_Type_Supermarket Type3 most influenced by:
    - Outlet_type_Grocery Store, Outlet_Identifier_OUT027, Outlet_Type_Supermarket Type3, Item_MRP, and Item_Type_Starchy Foods.
    - We have 3 negative features, but are outweighed by the positives. 


### Individual Force Plot


**Grocery Store**

<img width="976" alt="Ind_Force_Plot- Grocery Store" src="https://github.com/wrodemoyer/Prediction-of-Product-Sales/assets/128072861/05a2db2c-5bf9-4b8a-9dd6-dabd2fc06f44">

- The Features, Outlet_Type_Grocery Store and Item_MRP most influence the predictions.


**Supermarket Type3**

<img width="993" alt="Ind_Force_Plot- Super Market" src="https://github.com/wrodemoyer/Prediction-of-Product-Sales/assets/128072861/6d8e47e1-a1a3-43e3-ac1c-836ffae51adf">

- The Features, Outlet_Establishment_Year,Outlet_Type_Grocery Store, Outlet_Type_Supermarket Type3, Outlet_Identifier_OUT027, and Item_MRP most influence the predictions.





### For Further Informtion
For any additional questions, please contact wrodemoyer@gmail.com
