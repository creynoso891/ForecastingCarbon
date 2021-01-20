# ForecastingCarbon
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
1. one csv file with all the necessary data
2. R Markdown with all the code to clean and analyze the data titled co2_mm_mlo.txt
3. the pdf produced using the R Markdown titled 'Modeling & Forecasting Atmospheric Carbon Concetration.pdf'

