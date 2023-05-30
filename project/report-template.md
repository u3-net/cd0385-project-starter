# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Toumi Mohamed

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
I had  to eliminate any negative values present in the dataset and replace them with zero. Furthermore, I needed to assign the predictions to the submission dataframe.

### What was the top ranked model that performed?
WeightedEnsemble_L3

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?

There are no outliers in the data since the minimum and maximum values are within a reasonable range of the mean. By visualizing the histogram for each feature, we observe that the distributions of temp, atemp, and windspeed follow a normal pattern. The working and holiday features are binary and can be classified accordingly. Both the season and weather features can be categorized as well.

### How much better did your model preform after adding additional features and why do you think that is?
After incorporating additional features, the score significantly improved from 1.80659 to 0.53929. In my opinion, the month, day, and hour are three impactful features that contribute to the bike sharing demand. By including these additional features, we are able to capture and utilize this information during training, leading to enhanced predictions on the test data.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
The scores obtained from the improved model are considerably better compared to the initial model. Interestingly, the score are  similar to the results achieved when additional features were added.

### If you were given more time with this dataset, where do you think you would spend more time?
 I believe it is essential to allocate more time towards data cleansing and feature engineering. These steps involve carefully preparing the data and extracting meaningful information that can enhance the model's predictive capabilities. Additionally, hyperparameter tuning plays a crucial role in optimizing the model's performance. Autogluon provides presets that are specifically designed to automatically search for the best hyperparameters, resulting in improved outcomes. By combining meticulous data preprocessing, effective feature engineering, and leveraging Autogluon's hyperparameter optimization capabilities, we can strive for superior model performance.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|time_limit|num_bag_folds|num_trials|score|
|--|--|--|--|--|
|initial|	600	|8|1|1.80659|
|add_features|	600	|8|1|0.53929|
|hpo|1200|16|5|0.64194|



### Create a line plot showing the top model score for the three (or more) training runs during the project.

![image](https://github.com/u3-net/cd0385-project-starter/assets/92238267/4ec9d2d0-7cbc-415e-9ab9-ded2546ca15a)




### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

![image](https://github.com/u3-net/cd0385-project-starter/assets/92238267/733115c8-894e-497f-934b-fdef0e0dcf57)

## Summary
TODO: Add your explanation



















