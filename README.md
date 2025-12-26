# BITCOIN-BEHAVIUOUR-PREDICTION
This project investigates the short-term directional behavior of Bitcoin by integrating macroeconomic indicators  and applying a machine learning–based classification framework. 

# Bitcoin Behavior Prediction Using Macroeconomic Indicators and Machine Learning

This project investigates the short-term directional behavior of Bitcoin by integrating macroeconomic indicators with technical market features and applying a machine learning–based classification framework. The goal is not to predict Bitcoin prices directly, but to identify high-confidence trading opportunities while avoiding uncertain market conditions.
Bitcoin is often characterized as a highly volatile and speculative asset. Recent research, however, suggests that its price behavior is increasingly coupled with global financial markets. This project explores that hypothesis by modeling Bitcoin’s daily price direction using both internal market signals and external economic indicators.

A Random Forest Classifier is trained on engineered features derived from Bitcoin price data, equity indices, volatility measures, and currency strength indicators. To improve practical usability, the model is combined with a confidence-based execution strategy, referred to as the Sniper Method, which filters out low-conviction predictions.

# Key Features

Macroeconomic integration:

S&P 500 and NASDAQ-100 lagged returns

Volatility Index (VIX)

US Dollar Index (DXY)

US 10-Year Treasury Yield (TNX)

Technical and market features

Logarithmic returns and lagged returns

Relative Strength Index (RSI)

Volume change

Distance from 10-day and 50-day Simple Moving Averages

Rolling volatility measures

# Machine Learning Model

Random Forest Classifier (scikit-learn)

Time-series–aware train/test split (no shuffling)

Hyperparameter tuning to reduce overfitting

Sniper Method (Selective Prediction Framework)

Predictions executed only when:

Absolute daily return exceeds ±0.6%

Model confidence exceeds 55%

Designed to prioritize precision and capital preservation over frequent trading

# Methodology

Data Collection

Historical financial data retrieved via Yahoo Finance

Bitcoin and traditional markets aligned using forward-filling

Feature Engineering

Log-return transformations for stationarity

Lagged features to capture short-term dependencies

Technical indicators for momentum and trend detection

Model Training

Random Forest classifier trained on historical data

Evaluation performed on out-of-sample test data

Evaluation Strategy

Accuracy measured only on high-confidence predictions

Days with low model confidence are intentionally skipped

# Results

Achieved approximately 55% accuracy on high-confidence predictions

Performance consistently exceeded random baseline behavior however model tend to predict up movement most of the time

Results support the hypothesis that Bitcoin is influenced by broader economic conditions

Key Takeaways

Bitcoin price behavior is increasingly linked to macroeconomic indicators

Selective, confidence-based trading strategies can reduce exposure to noise

Machine learning models are more effective when paired with decision filters rather than forced daily predictions

# Technologies Used

Python

pandas, NumPy

scikit-learn

yfinance

matplotlib, seaborn

# Future Work

Replace Random Forest with LSTM-based architectures

Incorporate additional assets (Ethereum, oil, gas)

Integrate sentiment analysis from news and social media

Perform statistical significance testing and strategy backtesting
