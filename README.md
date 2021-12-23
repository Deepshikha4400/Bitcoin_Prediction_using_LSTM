Bitcoin, the most famous decentralised digital currency, is the largest cryptocurrency globally in market capitalisation. It was introduced to the world for the first time in January 2009 and has had a volatile trading history ever since. The transactions occur via a Peer-to-Peer (P2P) network and are recorded in the blockchain, a public ledger. Here, an attempt has been made to predict, using regression (particularly LSTM), the closing price of Bitcoin at the end of each hour from 1st March 2016 to 24th November 2018 based on the available hourly data. It is multivariate because the closing price depends on the different prices, the volume traded, as well as trend, i.e. the popularity of the terms associated and time series as the values vary across time.

DATASET

The data was chosen to cover the first major boom in the price of Bitcoin, which occurred towards the beginning of 2018. The data uses 23976 hourly data points, each denoting the values of the various parameters at the end of a one-hour long interval starting from 1st March 2016 (first interval ending at 12:58 am) and ending on 24th November 2018 11:59 pm.
The data used provides the following information:
Date: Date and end time of that particular one-hour duration.
Open: Opening price, i.e. the price (in USD) of Bitcoin at the beginning of that one-hour interval.
Close: Closing price, i.e. the price (in USD) of Bitcoin at the end of that one-hour interval.
High: Highest price (in USD) of Bitcoin in that one-hour interval.
Low: Lowest price (in USD) of Bitcoin in that one-hour interval.
Volume: Volume traded, i.e. the total price (in USD) of Bitcoins traded in that one-hour interval.
Bitcoin: Google trend of ‘Bitcoin’, i.e. the relative number of searches about the term ‘Bitcoin’ in that one-hour interval compared to the highest (assigned the value 100) number of searches in any one-hour interval in the entire dataset.
BTC: Google trend for ‘BTC’ (BTC is the abbreviation of Bitcoin).
Cryptocurrency: Google trend for ‘Cryptocurrency’.
Blockchain: Google trend for ‘Blockchain’.
Iota: Google trend for ‘Iota’ (Iota is an open-source distributed ledger and cryptocurrency such that a positive correlation of 0.84 has been established by researchers between the prices of Iota and Bitcoin).


IMPLEMENTATION

Python packages/libraries needed- Pandas, math, numpy, sklearn, keras and TensorFlow.
After importing all the necessary libraries, the dataset was loaded using pandas library, and all the data of columns was plotted separately with respect to time for visualising. After that, the time-series data were converted into data appropriate for supervised learning. The dataset values were then normalised using the MinMax method and the normalised values thus obtained are converted to be used for supervised learning. The dataset was split into two groups in the ratio of 7:3 for training and testing and then reshaped into 3D size to be used in LSTM. The LSTM model was then created, and the neuron structure was adjusted. The dataset was trained in 10 epochs with a batch size of 25. Loss values were calculated for every training epoch and visualised using a plot. A prediction process was performed for the training dataset as well as the test dataset. Performance measure was calculated using root mean squared error for train and test prediction. Finally, after concatenating the train and test predictions, a final plot of training and prediction was obtained and compared with the actual dataset in the same plot.

