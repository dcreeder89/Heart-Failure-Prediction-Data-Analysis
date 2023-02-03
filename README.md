# Heart Failure Prediction Data Analysis
## Analyzing a patients chance of developing a heart disease based on a variety of attributes

**Christina Reeder**: 

## Data Source:
https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction

For this dataset, there are 918 rows and 12 columns.

## Data Dictionary
![Attribut Information.png](https://github.com/dcreeder89/Heart-Failure-Prediction-Data-Analysis/blob/main/Attribute%20Information.png)


## Explanatory Data Analysis
  - The bargraphs explored the relationship between the food's MRP and visibility vs. the type of food it is. 

![age v heart disease by gender.png](https://github.com/dcreeder89/Heart-Failure-Prediction-Data-Analysis/blob/main/age%20v%20heart%20disease%20by%20gender.png)

The Items with the highest MRPs are of the type
  - Household: $149.42
  - Dairy: $148.59
  - Starchy Foods: $147.84

The Items with the lowest MRPs are of the type
  - Baking Goods: $126.39
  - Health and Hygiene: $130.82
  - Soft Drinks: $131.49


### Machine Learning using the following models:
  - Linear Regression Model
  - Decision Tree Regressor
  - Bagged Tree Regressor
  - Random Forest Regressor


### Models Evaluated and Results:
  - Linear Regression Model (Test Set)
    - R^2: -1.6575880497968222e+19
    - MAE: 558742259972.5935
    - MSE: 4.5732477819291586e+25
    - RMSE: 6762579228318.999
    
  - Decision Tree Regressor (Test Set)
    - R^2: 0.5960564372160062
    - MAE: 736.8796499354125
    - MSE: 1114471.1152767404
    - RMSE: 1055.6851402178304
    
  - Bagged Tree Regressor (Test Set)
    - R^2: 0.5511382977051897
    - MAE: 773.4183585708117
    - MSE: 1238399.2419976136
    - RMSE: 1112.833878886518
    
  - Random Forest Regressor (Test Set)
    - R^2: 0.6045439943790407
    - MAE: 726.928051236731
    - MSE: 1091054.1378349673
    - RMSE: 1044.535369355661


  - The final model chosen was a Random Forest Regressor Model with max_depth of 6 and n_estimators tuned to 250.
  - Mean Absolute Error was $726.93.
  - Mean Squared Error was $1,091,054.14
  - Root Mean Squared Error was $1,044.54

Using this model to make predictions on food sales would not be very reliable, considering the median outlet sales is $1,794.33 (the RMSE is almost as high as the median). 


## Recommendations
Data Science Insights
  - Our item oulest sales are slightly linked to the item MRP. However, there is not strong correlation with how much the item weighs or how visible it is on the shelfs. 
  - There also seems to be little change in the median sales when looking at fat content, outlet size, or outlet type. 

Model Performance
  - Overall, the best performing model was the tuned Random Forest Regressor Model. There is still some bias in the model, but it far outperforms the Linear Regression Model, and slightly outperforms the Decision Tree Regressor Model and the Bagged Tree Regressor Model. 


## Limitations and Next Steps
It is my recommendation that more datapoints be collected regarding these items and the outlets in which they are located. Locations in rural vs. urban areas will experience different sale amounts, and having that datapoint would assist in better tuning a machine learning algorithm to make predictions. 

### For further information
For any additional questions, please contact dcbailo89@gmail.com
