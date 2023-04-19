

![WhatsApp Image 2023-04-19 at 21 29 24](https://user-images.githubusercontent.com/115760894/233174738-860bb2ea-765f-48c0-838e-0d22d9cb9c95.jpg)



Phase 2 Housing project.

# Business problem.

# $Authors:$
* Yussuf Hersi
* Bravin Mugangasia
* Pauline Wambui.
* Kibet Kemboi
* Brian Kisilu
* Ronald Nyagaka


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
King County House Data: a dataset that we were provided at the onset of the project. This file contains data for 21,597 homes built in King County from 1900 to 2015. Each home in the set contains information regarding features such as number of bedrooms/bathrooms, number of floors, square footage, zip code, condition, and more.

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
![image1](https://user-images.githubusercontent.com/123490766/233191153-686ebb14-7026-4d59-89ea-8cd28e548208.png)


# Modeling 
We used  three different models for predicting house prices based on various features such as square footage, number of bedrooms and bathrooms, location, etc. The models used are:

* Base Model- Multiple Regression
* Log Transformation Model
* Polynomial Model

# Conclusions 
* Base Model
This model has a lower R-squared value, which indicates that the model is not able to explain as much variance in the data as the other models. The R-squared value of ```0.60``` suggests that the model explains ```60%``` of the variance in the data, which is lower than the other two models.

The MAE values for both the train and test sets are around ```155,000```, which is higher than the other two models, indicating that this base model's predictions are, on average, off by a larger margin. The MSE values are also higher than the other models, indicating that the model's predictions may be quite far off for some instances. The RMSE values are also higher than the other models, indicating that the errors are larger.

The mean_diff value for this base model is around ```32%```, which is higher than the other two models, indicating that the model's predictions are off by a larger margin. The percentage difference for each individual instance is also higher, ranging from ```20%``` to ```44%.

In conclusion, this base model's performance is lower than the other two models, as indicated by the lower R-squared value, higher MAE, MSE, and RMSE values, and higher mean_diff. Therefore, there is room for improvement, and we should explore other models to improve the performance of our prediction model.

* Log Transformation Model
This is a log transformation model output, and it is difficult to compare it with the previous results as they are from a different type of model. However, we can analyze the performance of this log transformation model using the provided output.

The R-squared value of 0.58 suggests that the model explains 58% of the variance in the data, which is lower than the R-squared value of the previous model. It indicates that the model may not be able to capture all the underlying patterns in the data.

The Mean Absolute Error (MAE) for both the train and test sets is around ```0.27```, which means that on average, the model's predictions are off by ```0.27``` units. The Mean Squared Error (MSE) values for the train and test sets are in the order of 0.11, indicating that the model's predictions may be quite far off for some instances. The Root Mean Squared Error (RMSE) values are around 0.34 for both the train and test sets.

Looking at the mean_diff, which is the mean of the percentage difference between the actual and predicted values, it is around ```2%```, indicating that the model's predictions are off by ```2%``` on average. The percentage difference for each individual instance is also quite low, ranging from 1.5% to ```4.3%.```

In conclusion, the performance of this log transformation model is reasonable, but there is still room for improvement. The lower R-squared value suggests that the model may not be able to capture all the underlying patterns in the data. However, the lower mean_diff values suggest that this model may be better suited for this particular dataset, and further analysis is required to draw a definitive conclusion.

* Polynomial Model
Based on the given output, the model seems to have performed reasonably well in predicting the target variable. The R-squared value of ```0.67``` suggests that the model explains ```67%``` of the variance in the data, which is not bad, but there is still room for improvement.

The Mean Absolute Error (MAE) for both the train and test sets is around ```$140,000,``` which means that on average, the model's predictions are off by ```$140,000.``` The Mean Squared Error (MSE) values for the train and test sets are in the order of billions, indicating that the model's predictions may be farther off for some instances. The Root Mean Squared Error (RMSE) values are around ```$210,000``` and ```$212,000``` for the train and test sets, respectively.

Looking at the mean_diff, which is the mean of the percentage difference between the actual and predicted values, it is around ```30%,``` indicating that the model's predictions are off by ```30%``` on average. The percentage difference for each individual instance is also quite high, ranging from ```19%``` to ```39%.```

In conclusion, the model's performance is decent, but there is certainly room for improvement. The high MAE, MSE, and RMSE values indicate that the model's predictions may be quite far off for some instances. Additionally, the high percentage difference for each individual instance suggests that the model may benefit from more fine-tuning or feature engineering.

Based on the performance metrics reported, the Log Transformation Model and Polynomial Model outperformed the Base Model. However, further improvements can be made by exploring other models, feature engineering, or hyperparameter tuning.

# Reccomendations 
As a recommendation, it would be useful to perform further analysis to identify the features that are driving the model's predictions and consider incorporating new features that may improve the model's performance. It would also be worth experimenting with different machine learning algorithms or hyperparameter tuning to see if the model's performance can be improved. Finally, it may be useful to gather more data to train the model and increase the size of the training set to get more accurate predictions.

# Next Steps 
Discussing possible future steps for improving the models, such as incorporating new data, refining the feature set, or exploring new algorithms or ensembles.
