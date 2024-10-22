# stock_prediction
Abstract:

This project focuses on analyzing and predicting the stock prices of major technology companies—Apple, Google, Microsoft, and Amazon—using historical data retrieved from Yahoo Finance. The analysis involves descriptive statistics, visualizations of stock performance, and calculation of moving averages, daily returns, and correlations between stocks. Additionally, a Long Short-Term Memory (LSTM) neural network is used to predict the future closing price of Apple Inc. stock based on historical data. The predictive model is built using a time-series approach, and its performance is evaluated using metrics such as Root Mean Squared Error (RMSE).


Methodology:

    Data Collection:
        Stock data for Apple, Google, Microsoft, and Amazon is collected from Yahoo Finance using the yfinance library. The data includes daily stock prices, volume, and adjusted closing prices over a one-year period.

    Exploratory Data Analysis (EDA):
        Descriptive statistics for each stock are generated using .describe() to summarize central tendencies, dispersion, and distribution.
        Visualization of stock price trends and sales volume is conducted using Matplotlib and Seaborn.
        Moving averages (10-day, 20-day, and 50-day) are computed for smoothing stock prices to identify trends.
        Daily returns are calculated to assess stock volatility, and histograms are created to visualize the distribution of returns.
        Correlation analysis is performed to evaluate the relationships between the returns of different stocks.

    Predictive Modeling:
        An LSTM neural network model is built to predict Apple Inc.'s future stock prices using a time-series approach.
        Data is scaled using MinMaxScaler to normalize the stock prices before feeding them into the LSTM model.
        The dataset is split into training (95%) and testing (5%) sets, and the LSTM model is trained on historical closing prices with 60 previous days used as input features for predicting the next day’s price.
        The model architecture includes two LSTM layers followed by Dense layers, and it is trained using the Adam optimizer with mean squared error as the loss function.

    Model Evaluation:
        The model’s performance is evaluated by comparing predicted prices with actual prices from the testing dataset.
        The Root Mean Squared Error (RMSE) is calculated to measure the model's accuracy.
        Visualizations of the predicted vs. actual stock prices are generated to assess the model's performance visually.

Results:

The LSTM model successfully predicted future stock prices for Apple Inc. based on historical data, with a reasonable accuracy level. The predicted prices followed the actual trends with minor deviations, and the model was able to capture the overall pattern of stock price movements. The RMSE value provided a quantifiable measure of the model’s performance, indicating the average difference between predicted and actual prices. The visual comparison between training, validation, and predicted prices demonstrated that the model could effectively generalize stock price trends.
