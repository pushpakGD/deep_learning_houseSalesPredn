# House Prices Prediction using Deep Learning

- Developing a deep learning regression model for house price prediction involves utilizing  neural network architectures to analyze diverse features and patterns within real estate datasets. 
- Unlike classification tasks, regression focuses on predicting numerical values, making it particularly suitable for estimating property prices. 
- This advanced approach allows the model to recognize complex relationships among various factors influencing house values, providing a robust tool for accurate and data-driven pricing predictions in the dynamic real estate market.
- Dataset from kaggle: https://www.kaggle.com/datasets/harlfoxem/housesalesprediction

## EDA and results:

1. Dataframe consists of 21 features total of some features will be dropped for first model and later included in the final evaluation to compare results

![ss8](https://github.com/pushpakGD/deep_learning_houseSalesPredn/blob/main/images/ss8.png)

2. Ofcourse as the sqft tends to increase, the price increases as well

![ss1](https://github.com/pushpakGD/deep_learning_houseSalesPredn/blob/main/images/ss1.png)

3. The histogram of all the features present in the data.
We can see some relation between the rpice and sq-foot, no. of bedrooms and bathrooms of houses

![ss2](https://github.com/pushpakGD/deep_learning_houseSalesPredn/blob/main/images/ss2.png)

4. Theres a positive correlation between price and sqft of house, also we positice correlatione between number of bathrroms and the house price as well.

![ss3](https://github.com/pushpakGD/deep_learning_houseSalesPredn/blob/main/images/ss3.png)

#### Progress during testing:

1. The model seems to doing well on the training however on the validation set, it seems to overfit on, But overall the model is performing good ovet the hundred epochs we had.

![ss4](https://github.com/pushpakGD/deep_learning_houseSalesPredn/blob/main/images/ss4.png)

- Evaluation result of this initial model with dropped features:
RMSE = 222630.429 
MSE = 49564308006.602356 
MAE = 155014.18236925194 
##### R2 = 0.57491486070234 
Adjusted R2 = 0.574363415933051

The values are more scatered, we can further refine the model.

![ss5](https://github.com/pushpakGD/deep_learning_houseSalesPredn/blob/main/images/ss5.png)

### After training and evaluating the model by including all the features (all the independent features, only dropping the id and date column which are redendant for our analysis). It can be seen that the model has better accuracy. 

![ss6](https://github.com/pushpakGD/deep_learning_houseSalesPredn/blob/main/images/ss6.png)

The graph here is a little bit narrower compared to before which means that model is performing better than the previous model.

![ss7](https://github.com/pushpakGD/deep_learning_houseSalesPredn/blob/main/images/ss7.png)

- Final evaluation results:
RMSE = 142961.185 
MSE = 20437900317.405914 
MAE = 89196.63530631246 
#### R2 = 0.8412776796986254 
Adjusted R2 = 0.8410717760214368

The performance of the model achieved is much better than the previous trained model, this can be seen from the coeffecient of determination which is 0.84 compared to previous score of 0.55.
