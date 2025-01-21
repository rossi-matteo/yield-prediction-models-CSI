# CSI 4th Challenge - ML Models to Predict Yields of Crops in a Climate-Change Scenario

## Authors
Michele Baggi, Léandre Le Bizec, Matteo Rossi

## Why
Predicting crop yields under a high-emissions climate change scenario over the next 30 years addresses two critical global challenges: **climate change** and **food security**. 

Rising temperatures, increased CO₂ concentrations, and shifting weather patterns already impact agriculture. By 2050, the world will need to produce 70% more food to feed 9.8 billion people, while climate change threatens food production systems. Meeting global food demands under these conditions requires careful planning and adaptation.

Accurate crop yield predictions are essential for informed decision-making, enabling policymakers and farmers to develop sustainable food production strategies. This project explores yield projections under a high-emissions scenario, identifying key productivity factors and potential predictors to mitigate the impact of climate change on agriculture.

## The Domain
We focused on **wheat** and **maize** as benchmark crops due to their well-documented input data, sourced from the Kaggle competition **The Future Crop Challenge**.

The challenge involved predicting yields under changing climate conditions, incorporating daily shortwave radiation, temperature, and precipitation data for 30 days before sowing and 210 days after sowing. Rising CO₂ levels were considered for their potential fertilization effect, depending on the crop’s photosynthesis pathway.

The dataset was restricted to significant agricultural regions with at least 2,000 hectares harvested and simplified to focus on **rainfed** and uniformly fertilized yields. This setup allowed for exploring yield variations due to weather, fertilization, and soil type, under the worst-case climate scenario regarding CO2 concentration levels. 

This challenge, organized by AgML, under the Agricultural Model Intercomparison and Improvement Project (AgMIP), emphasized intercomparison studies and benchmark datasets, enabling advancements in agricultural research.

## Metrics and Results
Model performance was evaluated using the **Root Mean Square Error (RMSE)**, calculated as:

\[
RMSE = \sqrt{\frac{1}{n}\sum_{i=1}^{n}(y_i - \hat{y}_i)^2}
\]

where \( y_i \) are actual values, \( \hat{y}_i \) are predicted values, and \( n \) is the number of observations. A lower RMSE indicates better accuracy.

### Results Table
| Model            | Prediction (2020–2050) | Prediction (2051–2098) |
|-------------------|------------------------|------------------------|
| Linear Regression | 1.41                  | 3.07                  |
| LightGBM          | 1.33                  | 1.44                  |
| CNN               | 1.30                  | 1.51                  |
| LSTM              | **1.20**              | **1.42**              |
| Top Kaggle Leaderboard | 0.72             | 0.91                  |

The **LSTM model** achieved the best results, LightGBM followed closely.

## Competition - Dataset

[Kaggle: The Future Crop Challenge](https://www.kaggle.com/competitions/the-future-crop-challenge)

