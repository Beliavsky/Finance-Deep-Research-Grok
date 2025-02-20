# Survey of Research on Predicting Volatility of Asset Returns Using Intraday Data

## Key Points
- Intraday data at frequencies like 1, 5, or 15 minutes improves volatility prediction for asset returns.
- Realized volatility (RV), calculated from intraday returns, is a key method for forecasting.
- Machine learning, especially deep learning, enhances forecast accuracy with high-frequency data.

## Overview
Predicting the volatility of asset returns using intraday data at high frequencies (e.g., 1, 5, or 15 minutes) is crucial for financial risk management and trading strategies. This approach leverages detailed price movements within a day to forecast volatility, often outperforming traditional daily data models. A surprising detail is that for longer forecast horizons (up to a month), the advantage of high-frequency data may diminish, making daily models competitive.

## Methods and Findings
**Realized Volatility (RV):** RV is calculated by summing squared intraday returns, providing a better estimate of daily variance than daily returns alone. This method is widely used due to its accuracy in capturing short-term volatility.

**Popular Models:** The Heterogeneous Autoregressive (HAR) model is popular for its ability to handle long memory in volatility, often outperforming GARCH models. Recent advancements include machine learning techniques like Long Short-Term Memory (LSTM) and neural networks, which excel with complex, high-dimensional data.

**Improvement with Intraday Data:** Studies show that using intraday data, especially at 5 or 15-minute intervals, improves short-term forecast accuracy. However, for forecasts beyond a month, the benefit may lessen, as seen in studies comparing high-frequency and low-frequency models.

---

## Detailed Survey Note

The research on predicting the volatility of asset returns using intraday data at frequencies such as 1, 5, or 15 minutes has evolved significantly, driven by the availability of high-frequency financial data and advancements in econometric and machine learning models. This note provides a comprehensive overview, detailing methodologies, key findings, and influential studies, ensuring a thorough understanding for both academics and practitioners.

### Background and Importance
Volatility forecasting is essential for risk management, portfolio allocation, and option pricing in financial markets. Traditionally, models like Generalized Autoregressive Conditional Heteroskedasticity (GARCH) and stochastic volatility (SV) models relied on daily return data. However, the advent of high-frequency intraday data, recorded at intervals like 1, 5, or 15 minutes, has enabled more granular analysis, capturing intraday price dynamics that daily data might miss.

### Methodologies
The primary approach involves calculating realized volatility (RV), defined as the sum of squared intraday returns over a day, which serves as an estimate of daily variance. This method, rooted in the theory of quadratic variation from continuous-time finance, reduces noise compared to daily squared returns, as noted by Andersen and Bollerslev (1998b) [Forecasting daily exchange rate volatility using intraday returns](https://www.sciencedirect.com/science/article/abs/pii/S0261560600000474).

- **Realized Volatility Models:** RV is often modeled using time series techniques. The Heterogeneous Autoregressive (HAR) model, proposed by Corsi (2009), is particularly effective, capturing long memory by decomposing volatility into short, medium, and long-term components. This model has been shown to outperform GARCH models, especially for high-frequency data, as evidenced in studies like "Forecasting volatility of Bitcoin" (2021) [Forecasting volatility of Bitcoin](https://www.sciencedirect.com/science/article/pii/S0275531921001616), which used RV estimated from high-frequency data.

- **Machine Learning Approaches:** Recent research has shifted towards machine learning, leveraging models like Long Short-Term Memory (LSTM) and neural networks. For instance, "Volatility Forecasting with Machine Learning and Intraday Commonality" (2023) [Volatility Forecasting with Machine Learning and Intraday Commonality](https://academic.oup.com/jfec/article/22/2/492/7081291) demonstrates that neural networks improve forecasting by exploiting commonality in intraday volatility, particularly for stocks with lower market capitalization. These models handle non-linear patterns and high-dimensional data effectively, often outperforming traditional econometric models.

- **Specific Frequencies:** Studies often use data at 5-minute or 15-minute intervals, as seen in "Volatility forecast for 5-minute frequency data" discussions on Quantitative Finance Stack Exchange [Volatility forecast for 5-minute frequency data](https://quant.stackexchange.com/questions/71739/volatility-forecast-for-5-minute-frequency-data) and "The Layman’s Guide to Volatility Forecasting" (2024), which analyzed 15-minute bars for the SPDR S&P 500 ETF [The Layman’s Guide to Volatility Forecasting](https://caia.org/blog/2024/11/02/laymans-guide-volatility-forecasting-predicting-future-one-day-time). These frequencies balance granularity with manageability, addressing microstructure noise through techniques like subsampling or realized kernels.

### Key Findings
Research consistently shows that intraday data enhances volatility forecast accuracy, particularly for short-term horizons. For example, Martens (2002) [Forecasting Daily Volatility with Intraday Data](https://www.researchgate.net/publication/24080610_Forecasting_Daily_Volatility_with_Intraday_Data) found that the first hour of trading contains sufficient information to predict daily volatility, with explanatory power up to 68%. However, a notable finding is that for longer forecast horizons (up to one month), the superiority of high-frequency models diminishes, as reported in "Stock market volatility forecasting: Do we need high-frequency data?" (2020) [Stock market volatility forecasting: Do we need high-frequency data?](https://www.sciencedirect.com/science/article/abs/pii/S0169207020301874), where high-frequency models only outperform low-frequency models for short-term forecasts.

Additional factors like trading volume, investor attention (e.g., Google search volume), and market conditions further improve forecasts. For instance, "Volatility Forecasting for High-Frequency Financial Data Based on Web Search Index and Deep Learning Model" (2021) [Volatility Forecasting for High-Frequency Financial Data Based on Web Search Index and Deep Learning Model](https://www.mdpi.com/2227-7390/9/4/320) found that incorporating investor attention via Baidu search indices enhances prediction accuracy using temporal convolutional networks (TCN).

### Comparative Performance
Comparative studies reveal that HAR models often outperform GARCH models, especially for short-term forecasts, as seen in Bitcoin volatility studies. Machine learning models, particularly those with memory like LSTM, rank among the top performers, as noted in "Prediction of realized volatility and implied volatility indices using AI and machine learning: A review" (2024) [Prediction of realized volatility and implied volatility indices using AI and machine learning: A review](https://www.sciencedirect.com/science/article/pii/S1057521924001534). However, traditional econometric models remain relevant, often yielding similar results, suggesting a hybrid approach combining both could be promising.

### Challenges and Considerations
Challenges include handling microstructure noise at high frequencies, addressed by methods like realized kernels or subsampling, as discussed in "Realized Vol for 15 min interval using second Data" on Quantitative Finance Stack Exchange [Realized Vol for 15 min interval using second Data](https://quant.stackexchange.com/questions/26370/realized-vol-for-15-min-interval-using-second-data). Market conditions also affect performance, with intraday models performing better in bull markets but less so in bear markets, as found in "On forecasting daily stock volatility: The role of intraday information and market conditions" (2009) [On forecasting daily stock volatility: The role of intraday information and market conditions](https://www.sciencedirect.com/science/article/abs/pii/S0169207009000077).

### Table of Key Studies

| Study Title                                                                 | Year | Focus Area                                      | Key Finding                                                                 |
|-----------------------------------------------------------------------------|------|------------------------------------------------|-----------------------------------------------------------------------------|
| [Modeling and Forecasting Realized Volatility](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=267792) | 2003 | RV and high-frequency data                     | Vector autoregression on RV outperforms GARCH models                        |
| [Volatility Forecasting](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=684714) | 2005 | Survey of volatility models                    | Covers GARCH, SV, and RV paradigms, emphasizing high-frequency applications |
| [Forecasting Daily Volatility with Intraday Data](https://www.researchgate.net/publication/24080610_Forecasting_Daily_Volatility_with_Intraday_Data) | 2002 | Intraday data for daily volatility             | First hour trading predicts daily volatility with 68% accuracy              |
| [Volatility Forecasting with Machine Learning and Intraday Commonality](https://academic.oup.com/jfec/article/22/2/492/7081291) | 2023 | Machine learning for intraday RV               | Neural networks improve forecasts by exploiting commonality                 |
| [Forecasting volatility of Bitcoin](https://www.sciencedirect.com/science/article/pii/S0275531921001616) | 2021 | Bitcoin volatility with high-frequency data    | HAR models outperform GARCH for short-term forecasts                        |
| [Stock market volatility forecasting: Do we need high-frequency data?](https://www.sciencedirect.com/science/article/abs/pii/S0169207020301874) | 2020 | High vs. low-frequency models                  | High-frequency models better for short-term, not long-term forecasts        |

### Conclusion
The research underscores the value of intraday data at frequencies like 1, 5, or 15 minutes for volatility forecasting, with RV and HAR models as foundational, and machine learning offering cutting-edge improvements. While short-term forecasts benefit significantly, longer horizons see diminishing returns, highlighting the need for context-specific model selection. This field continues to evolve, with hybrid models and explainable AI as promising future directions.

## Key Citations
- [Forecasting daily exchange rate volatility using intraday returns](https://www.sciencedirect.com/science/article/abs/pii/S0261560600000474)
- [Forecasting Daily Volatility with Intraday Data](https://www.researchgate.net/publication/24080610_Forecasting_Daily_Volatility_with_Intraday_Data)
- [Volatility Forecasting with Machine Learning and Intraday Commonality](https://academic.oup.com/jfec/article/22/2/492/7081291)
- [On forecasting daily stock volatility: The role of intraday information and market conditions](https://www.sciencedirect.com/science/article/abs/pii/S0169207009000077)
- [A practical model for prediction of intraday volatility](https://www.bloomberg.com/professional/insights/data/a-practical-model-for-prediction-of-intraday-volatility/)
- [Forecasting value at risk with intra-day return curves](https://www.sciencedirect.com/science/article/abs/pii/S0169207019302626)
- [Forecasting risk measures using intraday and overnight information](https://www.sciencedirect.com/science/article/abs/pii/S1062940822000250)
- [Intraday return predictability: Evidence from commodity ETFs and their related volatility indices](https://pmc.ncbi.nlm.nih.gov/articles/PMC7480318/)
- [The contribution of intraday jumps to forecasting the density of returns](https://www.sciencedirect.com/science/article/abs/pii/S0165188920300233)
- [Volatility forecast for 5-minute frequency data](https://quant.stackexchange.com/questions/71739/volatility-forecast-for-5-minute-frequency-data)
- [Forecasting volatility of Bitcoin](https://www.sciencedirect.com/science/article/pii/S0275531921001616)
- [The Layman’s Guide to Volatility Forecasting](https://caia.org/blog/2024/11/02/laymans-guide-volatility-forecasting-predicting-future-one-day-time)
- [Realized Vol for 15 min interval using second Data](https://quant.stackexchange.com/questions/26370/realized-vol-for-15-min-interval-using-second-data)
- [Stock market volatility forecasting: Do we need high-frequency data?](https://www.sciencedirect.com/science/article/abs/pii/S0169207020301874)
- [Forecasting Volatility Using High-Frequency Data](https://www.researchgate.net/publication/286131346_Forecasting_Volatility_Using_High-Frequency_Data)
- [Volatility Forecasting for High-Frequency Financial Data Based on Web Search Index and Deep Learning Model](https://www.mdpi.com/2227-7390/9/4/320)
- [Prediction of realized volatility and implied volatility indices using AI and machine learning: A review](https://www.sciencedirect.com/science/article/pii/S1057521924001534)
- [Modeling and Forecasting Realized Volatility](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=267792)
- [Volatility Forecasting](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=684714)
