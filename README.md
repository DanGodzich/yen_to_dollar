# Yen to Dollar Analysis 

In this analysis I looked at how time series analysis and linear regression would work in predicting foreign currency exchange rates. 

## *Time Series Analysis*

I started out with daily exchange data from August of 1976 to October of 2019. I trimmed this data down start on January 1, 1990 until October 15, 2019. This gave us a more manageable timeframe of approximately thirty years. 

The data was then plotted to look for trends. There are some short term spikes for the yen price in the mid 1990's and around 2012, but they did not last too long. Over the thirty year period there is a small but steady increase in the yen price. 

Next, we used a Hodrick-Prescott Filter to plot the trend and noise for the years from 2015 to 2019. Both plots indicated a fairly flat trajectory for the yen price.

After that, the 2015 to 2019 data was inserted into an ARMA model and a five day forecast of the settle price was plotted based upon that model. The ARMA model predicted a rather significant drop for the yen settle price. 

The 2015 to 2019 data was then inserted into an ARIMA model and also ploteed for a five day forecast of the settle price. The ARIMA model predicted a quick dip in the settle price but then a sharp rise. 

The same data was inserted into a GARCH model to predict the settle price volatility over the next five days. The GARCH model predicted a sharp rise in volatility over the five day period.

Based on this information, I would not invest at that moment in yen futures; two models showed divergent directions for the settle price and the GARCH model predicted increased risk. Based on the metrics of all three models, the ARIMA model had the lowest AIC score of the three models, showing it was a better model, but overall I did not feel the models were very accurate. 

## *Linear Regression*

The same data was used to perform a linear regression analysis. When the predicted returns was plotted against the actual returns for the first twenty predictions the graphs resembled each other fairly closely. Conducting a Root Mean Squared calculation on both the Out-of-Sample data and on In-sample date, showed the linear regression model performed even better on the Out-of-sample, or test data, than on the In-sample or training data. The linear regression model held up rather well.  

