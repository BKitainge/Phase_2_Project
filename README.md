
<img src="https://user-images.githubusercontent.com/115760894/233174738-860bb2ea-765f-48c0-838e-0d22d9cb9c95.jpg" alt="example image" width="1920" height="500">

Moringa School
Phase 2 Housing project

# Business problem.

# $Authors$ 
* *Yussuf Hersi | Bravin Mugangasia | Pauline Wambui | Kibet Kemboi | Brian Kisilu | Ronald Nyagaka*

# Problem Statement
The business problem the client is facing is how to create a successful platform for buying and selling houses in King County. To achieve this goal, the platform needs to provide accurate estimates of house prices, which is crucial for both buyers and sellers.

To accomplish this, the client wants to use a model that can infer the most important features that determine house prices in King County. These features might include factors such as the location of the house, the number of bedrooms and bathrooms, the size of the house, and other relevant factors.

The model needs to be trained on data that accurately represents the real estate market in King County, including historical sales data, current property listings, and other relevant data sources. By using this data, the model can learn to accurately estimate the value of a house based on its features.

Once the model is trained, it can be integrated into the platform to provide buyers and sellers with accurate estimates of house prices, which can help them make informed decisions about buying or selling a property. By providing a reliable and accurate platform for buying and selling houses in King County, the client can establish themselves as a leader in the local real estate market and attract a large and loyal customer base. 


### Project Objectives 
* To identify the key features that significantly influence house prices in King County.
* To develop a model that accurately estimates house prices based on the identified features.
* To evaluate the performance of the developed model in estimating house prices in King County.

# Data Understanding 
* Data
We utilized the following dataset to help make predictions of house prices in Kings County 
King County House Data: a dataset that we were provided at the onset of the project. This file contains data for 21,597 homes built in King County, Seattle from 1900 to 2015. Each home in the set contains information regarding features such as number of bedrooms/bathrooms, number of floors, square footage, zip code, condition, and more.

### Data Attribute Information;
* id
* date
* price 
* bedrooms 
* bathrooms 
* sqft_living 
* sqft_lot
* floors
* waterfront
* view
* condition
* grade
* sqft_above
* sqft_basement
* yr_built
* yr_renovated
* zipcode
* lat
* long
* sqft_living15
* sqft_lot15

# Results
### Explaratory Analysis

    1. <strong> Average Price Per View <\strong> <br>
<img src="https://user-images.githubusercontent.com/98708792/233442101-f0ee74a5-0071-49ce-b0be-66c94e1cbe88.png" alt="example image" width="500" height="250">
<br>
* The price increases as the view increases, however it seems houses with a fair view 2 are priced higher than houses with a good view 3, despite fair being higher on our scale right after excellent.
<br>
    2. Waterfront Vs Price <br>
<img src="https://user-images.githubusercontent.com/98708792/233443296-6aa98fb9-165b-4e5f-b183-1bc3740db87c.png" alt="example image" width="500" height="250">* 
From this we can see that houses with waterfronts are expensive by a wide range
<br>
    3. Average Price by Grade <br>
<img src="https://user-images.githubusercontent.com/98708792/233443659-6516a204-7700-455e-8663-10630c2b1e5a.png" alt="example image" width="500" height="250">
We can observe that as the grade increases so does the average price of each grouped category, and rise of price from 3 to 9 is gradual then rises sharply 9 to 13

<br>

    4. Price Vs Conditions <br>
<img src="https://user-images.githubusercontent.com/98708792/233443894-c4c6053e-11cc-4b2a-aee0-73e80a774126.png" alt="example image" width="500" height="250">
* From this we can see that price increases as the condition of the house increases
* However it appears that houses in poor condition are priced higher than those with fair condition
<br>
  
# Modeling 
We used  three different models for predicting house prices based on various features such as square footage, number of bedrooms and bathrooms, location, etc. The models used are:

### Base Model- Multiple Regression
![download (2)](https://user-images.githubusercontent.com/98708792/233449439-52a75a58-b180-4b9e-86fc-09c9afa262c1.png) <br>
    
 *The R-squared value (r2_score) is a measure of how well the model fits the data, with values closer to 1 indicating a better fit. In this case, the r2_score is 0.54927 which suggests that the model explains 55% of the variability in the target variable.*

*The mean absolute error (MAE) is a measure of the average magnitude of errors in the predictions made by the model. The lower the MAE, the better the model. The train MAE and test MAE are 163711.64 and 164276, respectively, which are quite large values, indicating that the model is not performing well.*

 *The root mean squared error (RMSE) is the square root of the MSE, and it measures the average magnitude of the error in the model's predictions. The train RMSE and test RMSE are 250,789 and 247,992, respectively, which are also quite large.*

Overall, these metrics suggest that the linear regression model is not performing very well in making accurate predictions on the dataset.

### Log Transformation Model
![download (1)](https://user-images.githubusercontent.com/98708792/233449163-80ded47b-9876-4e25-9822-84fef0f51755.png) <br>
*An R2 score of 0.55 indicates that the model explains 557% of the variance in the logarithmic actual values.*
*An MAE value of 0.282 for train data and 0.284 for test data suggest that, on average, the model's logarithmic predictions are off by about 28.2%and 28.4 respectively from the logarithmic actual values.*
*An MSE value of0.1228 for train data and an MSE of 0.1256 for test data suggest that, on average, the model's logarithmic predictions are off by the squared value of about 12.28% and 12.56% respectively from the logarithmic actual values.*
*An RMSE value of 0.3504 for train data and 0.3544 for test data suggest that, on average, the model's logarithmic predictions are off by the squared root value of about 35.04% and 35.44% respectively from the logarithmic actual values*
  
### Polynomial Model
![download](https://user-images.githubusercontent.com/98708792/233448982-551b530c-586a-49c6-90a4-262e7bbb603a.png)
 *The r2_score is 0.64, indicating that the model explains about 64% of the variation in the target variable.*

*The train MAE is 147506.65 and the test MAE is 149612. This means that, on average, the model's predictions are off by about $147,506 in the training data and $149,612 in the test data.*

*The train RMSE is 221366.59 and the test RMSE is 220257.06. The RMSE is in the same units as the target variable, and it can be interpreted as the average absolute difference between the actual and predicted values, after taking into account the scale of the target variable.*

In summary, these metrics can be used to evaluate the performance of the model. In this case, the model has a decent r2_score, but its MAE and RMSE indicate that there is still room for improvement in the model's predictive accuracy.

# Conclusions 
###  Polynomial Model

The pylonomial model in the given output performed reasonably well in predicting house prices, but there is room for improvement.

The R-squared value indicates that the model explains 64% of the variance in the data, while the Mean Absolute Error is around 
147,000.

The high values of MSE, RMSE, and MAE suggest that the model's predictions may be quite far off for some instances. The Log Transformation Model and base Model were outperformed by this model, but further improvements can be made by exploring other models or feature engineering.

# Recomendations 
As a recommendation, it would be useful to perform further analysis to identify the features that are driving the model's predictions and consider incorporating new features that may improve the model's performance.

Some features can also be considered when determining house prices. These features such as higher house grades, houses with better views, better condition, and the presence of a waterfront increase the value of the house.

Finally, it may be useful to gather more data to train the model and increase the size of the training set to get more accurate predictions
