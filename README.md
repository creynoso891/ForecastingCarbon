# Modeling & Forecasting Atmospheric Carbon Dioxide Concentration
Forecasting carbon dioxide concentration in the atmosphere. 

Carbon dioxide is a greenhouse gas, it causes heat to remain trapped within the atmosphere of Earth. It is a naturally occurring gas, but human activities, such as the combustion of fossil fuels, disrupt the natural carbon cycle. Due to its greenhouse effect and the magnitude with which humans produce it, carbon dioxide is a crucial component in understanding climate change.

## Table of Contents
* [Installation](#Installation)
* [About the Data](#About)
* [File Description](#description)
* [Results and Insights](#Results)
* [Limitations and Further Questions](#Limitations)
* [Licensing, Authors, Acknowledgements](#licensing)

## Installation
To get started you will need a recent version of RStudio. Additionally, the packages used in the project can be downloaded running the following at the command line:
    
        install.packages(c("astsa", "forecast", "TSPred"))
        
## About the Data <a name="About"></a>
The data set that I look at in this document has the CO2 monthly means measured at Mauna Loa, Hawaii. Throughout this project I try to understand the trend and seasonality of the data, and I use this information to fit a Seasonal Autoregressive Integrated Moving Average (SARIMA) model to the data. The model is then used to forecast atmospheric carbon concentration. 

## File Description <a name="description"></a>
This project includes:
1. **'co2_mm_mlo.txt'** CSV file with the CO2 monthly means data used for this project. 
- Up to date carbon dioxide data can be obtain through the following link: [Mauna Loa CO2 monthly means data (CSV)](https://www.esrl.noaa.gov/gmd/webdata/ccgg/trends/co2/co2_mm_mlo.txt) 
2. **'Modeling and Forecasting Atmospheric Carbon Concetration.Rmd'** R Markdown with the code to analyze, model, and vizualize CO2 monthly means data.
3. **'Modeling & Forecasting Atmospheric Carbon Concetration.pdf'** PDF produced using the R Markdown above (for complete code please refer to the Rmarkdowm above) 

## Results and Insights <a name="Results"></a>

The model used to forecast carbon dioxide concentration in the atmosphere was a Seasonal ARIMA(1,1,1)(2,1,2)12

1. **Seasonality** is an important component to explaining the variation that is present in the CO2 ppm. This means that the CO2 ppm levels naturally fluctuate up and down during certain times of the year. 
2. **Trend** is also a very crucial component to modeling and understanding the variation in the CO2 atmospheric concentration. As we have seen throughout the data visualization and the final SARIMA model, there is a positive trend in the level of CO2 present in our atmosphere. As the years have gone by there is a constant, predictable increase in the CO2 concentration. 
3. **Forecasting & Forecasting Accuracy** I tested the accuracy of the model by using forecasting. 
- I used data from 1958 to 2018 train the model 
- The forecasts were made for CO2 values from January 2019 to April 2020.
- Forecasting Accuracy can be gauged by analyzing forecasting errors. These values are in the same scale of the data, and the CO2 ppm values range from 312.66 to  416.21 ppm. Error terms that are close to zero, either positive or negative, indicate that the forecasts are unbiased and accurate. The forecast errors for the SARIMA model I created, are printed below: **the errors are close to zero, indicating that my model is unbiased and accurately predicted the CO2 ppm values.**

## Licensing, Authors, Acknowledgements <a name="licensing"></a>
