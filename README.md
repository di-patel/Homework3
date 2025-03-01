# Homework3
Running Forecasting Models on my Time Series

# Exploratory Analysis 

TIME SERIES PLOT

House prices fluctuate significantly over time, with noticeable spikes in specific periods. The volatility suggests potential external factors influencing house prices, such as economic events, interest rates, or policy changes. There is no clear upward or downward trend indicating that. The data exhibits high variability with periodic spikes, meaning traditional linear models may not perform well. 

ACF 

The autocorrelation function (ACF) plot indicates weak autocorrelation at various lags, with no strong seasonal patterns visible, as there are no significant spikes at regular intervals. This suggests the data may be noisy and non-stationary, requiring differencing or decomposition to stabilize it.

DECOMPOSITION

The decomposition of the time series data reveals that the observed data has a level component but lacks a strong seasonal trend. Sharp jumps in certain periods indicate possible outliers or irregular events that impact house prices. 

# Forecast Outputs

MEAN FORECAST

The mean forecast is flat, meaning it predicts future values as the average of past values. Given the sharp spikes in house prices, this method does not adjust well to variability. The mean model is not a good fit since it ignores volatility and fluctuations. It is too simplistic for a dataset with large variations.

NAïVE FORECAST

The Naïve model projects the most recent price as the future forecast. This might work well with a consistent trend, but since house prices are volatile, this method fails to capture long-term behavior. The Naïve model is weak for this dataset since prices fluctuate too much for a simple "repeat last value" approach.

RANDOM WALK FORECAST

The Random Walk model produces extreme values, making it unreliable for forecasting in my case.

SEASONAL NAïVE FORECAST

The seasonal naïve model, as seen in the corresponding plot, repeats the last observed seasonal values. It attempts to mimic past trends, which works well when patterns are stable. However, in this dataset, the decomposition plot showed no strong seasonal trend, meaning that while the seasonal naïve model captures short-term patterns, it may not be the most effective long-term predictor.

HOLTS-WINTERS FORECAST

The Holt-Winters model adjusts to trends and fluctuations, producing a smooth forecast while still capturing price variations. The alpha value in this model determines the weighting of recent data—a higher alpha means recent observations have a stronger influence. In comparison, a lower alpha smooths the trend more gradually. In my Holt-Winters forecast plot, the model successfully follows fluctuations in the time series without overreacting to short-term noise, making it one of the best forecasting choices.

MOVING AVERAGES (MA5, MA9)

The moving average models (MA5 & MA9) smooth out noise in the dataset, as seen in their plots. MA5 reacts more quickly to recent price changes, while MA9 provides a more stable trend by averaging over a longer period. While these models help understand the overall trend, they do not predict sudden shifts well, making them less useful for precise forecasting.

# Accuracy Measures
Mean Absolute Error is the most suitable accuracy measure for this dataset due to its interpretability, resilience to outliers, and effectiveness in handling volatile data such as house prices. It facilitates fair model comparisons and supports practical decision-making, making it the most reliable metric for evaluating forecast performance in this context.

The Holt-Winters model is effective for forecasting house prices as it dynamically adjusts to trends and fluctuations in the data. Unlike simpler models, it applies exponential smoothing to capture both short-term variations and long-term movements, ensuring more stable predictions. The model's alpha value determines how much weight is given to recent data, allowing it to be responsive without overreacting to temporary spikes. Given the volatility in house prices, Holt-Winters provides a balanced approach, making it the most reliable forecasting method for this dataset.



