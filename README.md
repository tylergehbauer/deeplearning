# LSTM Stock Predictor
*Deep Learning*

## Background 
I have been asked to help build and evaluate deep learning models using both the FNG values and simple closing prices to determine if the FNG indicator provides a better signal for cryptocurrencies than the normal closing price data.

In this assignment, I used deep learning recurrent neural networks to model bitcoin closing prices. One model will use the FNG indicators to predict the closing price while the second model will use a window of closing prices to predict the nth closing price.

---
## Method: 
 
For the Fear and Greed model, I ued the FNG values to try and predict the closing price. 

For the closing price model, I used previous closing prices to try and predict the next closing price. 

Each model will need to use 70% of the data for training and 30% of the data for testing.

I applied a MinMaxScaler to the X and y values to scale the data for the model.

Finally, I reshaped the X_train and X_test values to fit the model's requirement of samples, time steps, and features. 

 *Most functions are included in starter notebook* 

---
## LSTM Stock Predictor Using Fear and Greed Index 
![lstm_greed.png](Images/lstm_greed.png)

## LSTM Stock Predictor Using Closing Prices
![lstm_close.png](Images/lstm_close.png)

# Evaluate the performance of each model
Which model has a lower loss? - Overall, the LSTM Stock Predictor using Closing Prices had a much lower loss. (Can see above)

Which model tracks the actual values better over time? - The LSTM Stock Predictor using Closing Prices tracks actual values way better. You can visually see how close the predictions were to the actual data.

Which window size works best for the model? 

- For LSTM using Closing Prices I found that a window size of 1 resulted in the least amount of loss and was very accurate. (Window Size = 1 is what is being plotted above)
-For LSTM using Fear and Greed Index, I found that a window size of 5 resulted in the least amount of loss and was more accurate than the other sizes. 
