📈 Gold Price Prediction: A Multi-Factor Quant Strategy
🎯 OverviewThis project develops a robust machine learning framework to predict the daily direction of Gold prices ($GC=F$). By integrating technical momentum indicators, intermarket data (US Dollar Index), and NLP-based sentiment analysis, the model achieved an "Honest" Accuracy of 61.32% and a Sharpe Ratio of 2.14.

Key ResultsCumulative Return: 85.5% (Outperforming Buy-and-Hold by >2x).Average CV Accuracy: 57.64% (Verified via Time-Series Cross-Validation).Risk-Adjusted Return: Elite Sharpe Ratio of 2.14.🛠️ The Financial Engineering Pipeline1. Data Transformation & CleaningTo handle the volatility and non-stationarity of financial time series:Log Returns: Raw prices were transformed into stationarity:$$R_t = \ln\left(\frac{P_t}{P_{t-1}}\right)$$Winsorization: Extreme outliers (e.g., the 2017 anomaly) were clipped at the 1st and 99th percentiles to prevent gradient descent distortion.


2. Feature Engineering (The "Alpha" Drivers)
The model looks beyond price history to understand market context:

Technical Indicators: 14-day RSI and 20-day SMA to capture momentum and mean reversion.

Intermarket Logic: Inclusion of the US Dollar Index (DXY) to exploit the inverse correlation between USD and Gold.

Sentiment Analysis: A custom news scraper using BeautifulSoup and TextBlob to quantify global sentiment.

3. Preventing Data LeakageA critical component of this project was ensuring temporal integrity. All features were lagged by $t-1$ to ensure the model only uses information available before the market opens.

4. Metric,Model Strategy,Benchmark (Market)
Total Return,85.5%,~40.2%
Sharpe Ratio,2.14,0.85
Max Drawdown,Lower than Market,High


Backtest Visualization
The strategy demonstrates consistent alpha generation, particularly during high-volatility regimes where the AI-managed to "stay in cash" or dodge major downturns.




