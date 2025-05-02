# Neural Network Fuzzy Electricity Demand Forecasts Based on Fuzzy Inputs

Recently, there has been a growing interest in studying both long-term and short-term forecasts of electricity demand using dynamic regression models with seasonal ARIMA (SARIMA) errors and neural network autoregressive (NNAR) models. Most of the electricity demand forecasting models investigated in the literature involved two features: temperature and day type (weekday, weekend, or holiday), and only the point forecasts of temperature are used to obtain forecasts of electricity demand. However, it is crucial to acknowledge that temperature fluctuates throughout the day, and it is more appropriate to incorporate the forecast error variability and use the fuzzy forecasts of the temperature as an input to forecast electricity demand. This work uses a novel fuzzy two-step approach to generate fuzzy forecasts of electricity demand.

The PDF copy of the paper can be downloaded from here: [Download Paper](https://ieeexplore.ieee.org/abstract/document/10633488) 

A preprint version of the paper is available in the repository.

Programming Language: [R](https://cran.r-project.org/bin/windows/base/) / [RStudio](https://posit.co/downloads/)

Data: The electricity demand and meteorological data used are available in the CSV file in the repository. The following are the sources of data:
1. Electricity Demand Data: [Independent Electricity System Operator](https://ieso.ca/en/)
2. Meteorological Data: [Renewables.ninja](https://www.renewables.ninja/)

### Methodology

We introduce a hierarchical modeling strategy to generate fuzzy forecasts of electricity demand. The proposed strategy can be summarized as a multi-step procedure:

#### 🔹 Step 1: Fuzzy Forecasting of Temperature

- **Step 1a:** Identify the most important covariate affecting temperature.
- **Step 1b:** Fit different models and identify the best forecasting model for temperature using forecast accuracy measures (RMSE, MAE, MPE, and MAPE).
- **Step 1c:** Model temperature as a nonlinear adaptive fuzzy number and generate fuzzy forecasts.

#### 🔹 Step 2: Fuzzy Forecasting of Electricity Demand

- **Step 2a:** Fit different models and identify the best forecasting model for electricity demand using forecast accuracy measures (RMSE, MAE, MPE, and MAPE).
- **Step 2b:** Use the selected model from Step 2a and the fuzzy temperature forecasts from Step 1c to generate fuzzy forecasts of electricity demand.

### Findings

This study uses a novel fuzzy two-step approach to generate fuzzy forecasts of electricity demand. In step 1, fuzzy forecasts of temperature are obtained by incorporating additional features such as precipitation, irradiance, snowfall, snow mass, cloud cover, and air density. Thirteen distinct models, including neural network regression models and Facebook industrial Prophet models, are fitted to temperature data, and the best forecasting model for temperature is selected based on forecast accuracy measures. In step 2, the fuzzy forecasts of the temperature are used as a feature with day type (weekday/weekend/holiday) to obtain fuzzy forecasts of electricity demand. The superior performance of neural network fuzzy forecasts of electricity demand in terms of forecast accuracy is demonstrated for Ontario electricity demand data.

### References

1. R. J. Hyndman and G. Athanasopoulos, Forecasting: principles and practice, 3rd edition, OTexts: Melbourne, Australia. OTexts.com/fpp3, 2021.
2. Liang, Y., & Thavaneswaran, A. (2022, June). Long Term Interval Forecasts of Demand using Data-Driven Dynamic Regression Models. In 2022 IEEE 46th Annual Computers, Software, and Applications Conference (COMPSAC) (pp. 250-259). IEEE.
3. Bowala, S., Makhan, M., Liang, Y., Thavaneswaran, A., \& Appadoo, S. S. (2022, September). Superiority of the Neural Network Dynamic Regression Models for Ontario Electricity Demand Forecasting. In 2022 IEEE Canadian Conference on Electrical and Computer Engineering (CCECE) (pp. 182-187). IEEE.


