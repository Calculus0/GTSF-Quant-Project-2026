# High-Frequency Mid-Price Prediction Using CNN–LSTM Models with Order Flow Features
## Abstract
In this [notebook](https://github.com/ajcutuli/OFI_NN_Project/blob/main/DeepOFI.ipynb), we implement an artificial neural network based on the model proposed by Zhang et al., which combines convolutional neural networks (CNNs) with a long short-term memory (LSTM) network to classify short-term movements in a limit order book. Using Coinbase Bitcoin order book data, the goal is to predict whether the mid-price will increase, decrease, or remain unchanged at the next time step.

Unlike the original work by Zhang et al., which uses non-stationary order book states as inputs, our implementation trains the model on order flow and order flow imbalance—stationary features derived from the limit order book. This approach is also informed by Kolm et al. (2021), who show that order flow–based inputs can outperform raw order book data in forecasting tasks.

We extend this line of work by examining how transforming order flow into order flow imbalance affects model performance. In addition, we incorporate a time series perspective by analyzing the lag structure of the data, a step not explicitly addressed in the prior studies.

Our results indicate that both models struggle to predict downward price movements, particularly given the sparsity of the dataset. However, the model trained on order flow performs notably better in predicting upward movements. In a trading context, this limitation, especially the poor detection of downward trends, poses a significant challenge for intraday strategies in bearish markets.
