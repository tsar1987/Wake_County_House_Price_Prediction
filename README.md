# Wake_County_House_Price_Prediction

## Introduction

1. The residential house market in Wake County, NC is highly competitive, with properties receiving an average of 5 offers and selling in just 37 days. 
2. Use historical sale data, property features and economic indicators.
3. Aim to provide accurate and actionable pricing and remodeling recommendations to buyers and sellers.
   
## Audience

1. House buyers, sellers and real estate agents in Wake County, NC 
2. Example question1: What is a reasonable price for the property I am interested in buying? 
3. Example question2: What is the optimal listing price for my property? 
4. Example question3: What are the key factors influencing the predicted prices?
   
## Data

1. Historical Sale Data
one csv file from Wake County, North Carolina real estate website
441328 rows and 87 columns, including information about owner, mail address, real estate id, street, sale, deed, heated area, utility, exterior wall, design style, city etc.
https://www.wake.gov/departments-government/tax-administration/data-files-statistics-and-reports/real-estate-property-data-files
2. Economic Indicators
1 csv file from U.S. BUREAU OF LABOR STATISTICS
51 rows and 3 columns, including population density and unemployment data from 1973 to 2023.
https://data.bls.gov/timeseries/LASST370000000000003?amp%253bdata_tool=XGtable&output_view=data&include_graphs=true

## Exploratory data analysis (EDA)

Top 4 city in dataset: Raleigh, Cary, Apex, Wake Forest.

![image](https://github.com/tsar1987/Wake_County_House_Price_Prediction/blob/586497d74876f85c1dffcfc8bced7d6dc16740ef/Figures/house%20dist%20by%20city.png)

Top 4 sale year in dataset: 2021, 2020, 2022, 2019. Obvious dip around 2018-2012 because of economic crisis.

![image](https://github.com/tsar1987/Wake_County_House_Price_Prediction/blob/586497d74876f85c1dffcfc8bced7d6dc16740ef/Figures/house%20dist%20by%20year.png)

House price for each city with outliers.

![image](https://github.com/tsar1987/Wake_County_House_Price_Prediction/blob/586497d74876f85c1dffcfc8bced7d6dc16740ef/Figures/boxplot_1.png)

House price for each city without outliers. Remove outliers larger than 75 percentile +1.5*IQR

![image](https://github.com/tsar1987/Wake_County_House_Price_Prediction/blob/586497d74876f85c1dffcfc8bced7d6dc16740ef/Figures/boxplot_2.png)

Heatmap

![image](https://github.com/tsar1987/Wake_County_House_Price_Prediction/blob/586497d74876f85c1dffcfc8bced7d6dc16740ef/Figures/heatmap.png)

## Data Training and Modeling

![image](https://github.com/tsar1987/Wake_County_House_Price_Prediction/blob/a17dfc8de4974d615997f3e850146ca0a54c60f4/Figures/variable%20importance.png)

## Conclusion

Gradient boost regression model performs best in all four models I tested. The model performs very well for house price less than 3 million, for house price higher than 3 million, the predictive ability is weak, which means the model still not very good at handling high value outliers.

## Future Work

1. Collect more recent data into the training set could be beneficial, as it may capture evolving trends and market dynamics that impact house prices. 
2. Explore feature engineering techniques or introducing new relevant features, such as neighborhood developments, or seasonality factors, could improve the model's ability to adapt to changing conditions. 
3. Fine-tuning more hyperparameters of the Gradient Boosting Regressor or experimenting with alternative algorithms might also be considered to optimize predictive accuracy. 
4. Combine predictions from multiple models may provide a more robust and accurate prediction for house sales.














