# Stock Price Prediction using Neural Networks

This repository contains code for training a neural network model to predict stock prices using historical stock data. The goal of the project is to build a model that can accurately forecast stock prices based on various features. All models utilize a sliding-window based approach where a fixed number of previous days generate a prediction of the next day's price.

# Stakeholders
Shareholders: Predict the direction of their investment.  

Individual clients: Use stock price prediction tools to manage their own stocks and make a decision on stock selection.

# Dataset
The dataset used for training the model is sourced from the Individual Stocks Price dataset on [Kaggle](https://www.kaggle.com/datasets/camnugent/sandp500?resource=download). It contains historical stock data for all S&P 500 companies over a period of 5 years. S&P 500 include some of the top U.S.-listed companies that are leaders within their industries and represent a bellwether for the U.S. economy. Companies must meet certain criteria, which are determined by the publishers of the index, before being added to the S&P.  The top ten S&P 500 companies with a percentage of the market they control in 2023 include;
Apple (AAPL): 7.61%
Microsoft (MSFT): 6.80%
Amazon (AMZN): 3.15%
NVIDIA (NVDA): 2.83%
Alphabet Class A (GOOGL): 1.92%
Tesla (TSLA): 1.84%
Meta Platforms (META), formerly Facebook, Class A: 1.74%
Alphabet Class C (GOOG): 1.66%
Berkshire Hathaway (BRK.B): 1.64%
UnitedHealth Group (UNH): 1.23%

The data include the following details
Date - in format: yy-mm-dd 
Open - price of the stock at market open (this is NYSE data so all in USD)
High - Highest price reached in the day
Low Close - Lowest price reached in the day
Volume - Number of shares traded
Name - the stock's ticker name


## Preprocessing

Before training the model, the data is preprocessed as follows:

- Date column is converted to datetime format.
- Irrelevant columns such as 'Name' and 'date' are dropped.
- Data is split into features (X) and target (y).
- Features are normalized using Min-Max scaling.


## Training

The dataset is split into training (70%) and testing sets (30%), with the testing set reserved for final evaluation. The training set is further divided into training (80%) and validation (20%) subsets. The model's performance is monitored using training and validation losses, aiming to minimize these losses over epochs.
## Evaluation

After training, the model is evaluated on the validation set using Mean Squared Error (MSE). Additionally, predictions are made on the validation set, allowing qualitative assessment of the model's performance. It was found that compared to sliding window linear regression and LSTM models, the simple naive prediction performed the best in our analysis.

## Future Work

Currently, only the stock data for one company (AAP) is used for prediction. In future iterations, data for all companies will be incorporated to build a more comprehensive model. As well, it is likely this project will be updated with various models to compare their success against the naive prediction.

## Contributing

Group members are encouraged to contribute to the project. Feel free to ask any doubt or contribute with your expertise to enhance the model's performance or expand its capabilities.
