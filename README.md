# Stock Price Prediction using Neural Networks

This repository contains code for training a neural network model to predict stock prices using historical stock data. The goal of the project is to build a model that can accurately forecast stock prices based on various features.

## Dataset

The dataset used for training the model is sourced from the [Individual Stocks Price](https://www.kaggle.com/camnugent/sandp500) dataset on Kaggle. It contains historical stock data for various companies over a period of 5 years.

## Preprocessing

Before training the model, the data is preprocessed as follows:

- Date column is converted to datetime format.
- Irrelevant columns such as 'Name' and 'date' are dropped.
- Data is split into features (X) and target (y).
- Features are normalized using Min-Max scaling.

## Model Architecture

The neural network model is built using TensorFlow's Keras API with the following architecture:

- Input layer: Dense layer with 64 units and ReLU activation function.
- Hidden layers: Two Dense layers with 32 and 16 units respectively, both with ReLU activation.
- Output layer: Dense layer with 1 unit and linear activation function.

The model is compiled using the Adam optimizer and Mean Squared Error (MSE) loss function.

## Training

The dataset is split into training sets(70%)(80% of which are for training and 20% for validation), testing sets (30% which we are not using at this moment). Currently, only the training and validation sets are used for training and testing respectively. The actual testing data will be used in the last stage.

During training, both training and validation losses are monitored. The goal is to minimize these losses over epochs, indicating that the model is learning and improving its predictions.

## Evaluation

After training, the model is evaluated on the validation set using Mean Squared Error (MSE). Additionally, predictions are made on the validation set, allowing qualitative assessment of the model's performance.

## Future Work

Currently, only the stock data for one company (AAP) is used for prediction. In future iterations, data for all companies will be incorporated to build a more comprehensive model.

## Contributing

Group members are encouraged to contribute to the project. Feel free to ask any doubt or contribute with your expertise to enhance the model's performance or expand its capabilities.
