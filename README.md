📊 Unemployment Analysis with Python


A data-driven analysis of unemployment trends in India, investigating the impact of COVID-19, regional disparities, and temporal patterns using Python.


🎯 Objectives

Quantify the impact of COVID-19 on unemployment rates across regions in India.

Identify key predictors of unemployment using labour participation and temporal trends.

Detect seasonal patterns and regional disparities in unemployment data.

Forecast short-term unemployment trends using time series modelling.

Present insights that could inform economic and social policy decisions.


🔬 Research Questions

What variables significantly affect unemployment rates?

Are there temporal or demographic patterns in the data?

Can we predict unemployment levels using statistical models?


🗂️ Dataset


### Dataset Description: Unemployment_in_India.csv

The dataset contains **768 rows** and **7 columns**.

| Column | Description |
| :--- | :--- |
| **Date** | Time period of observation |
| **Region** | Indian state or region |
| **Area** | Rural or Urban classification |
| **Estimated Unemployment Rate (%)** | Main target variable |
| **Estimated Employed** | Number of employed individuals |
| **Estimated Labour Participation (%)** | Workforce participation metric |


🛠️ Tools & Libraries


| Library | Purpose |
| :--- | :--- |
| **pandas** | Data loading, cleaning, and manipulation |
| **numpy** | Numerical computations |
| **matplotlib** | Data visualization |
| **seaborn** | Statistical visualizations |
| **scipy.stats** | Hypothesis testing (t-test, ANOVA) |
| **statsmodels** | OLS regression, ARIMA, ADF test, seasonal decomposition |



📁 Project Structure


 Unemployment-Analysis-with-Python/
 
│

├── Unemployment_Analysis_with_python.ipynb   # Main analysis notebook

├── Unemployment_in_India.csv                 # Dataset

├── README.md                                 # Project documentation

│

└── results/

    └── figures/                              # All saved visualizations
    
        ├── Unemployment Rate Trajectory: pre vs post COVID-19.png
        
        ├── Distribution of Unemployment Rate.png
        
        ├── Top 10 Regions Hardest Hit by Unemployment(COVID Period).png
        
        ├── Region Distribution of Unemployment.png
        
        ├── Unemployment Trend Over Time.png
        
        ├── Unemployment During COVID Period.png
        
        ├── Correlation Matrix.png
        
        └── Distribution of residuals.png
        
        
🔍 Methodology

1. Data Cleaning
Standardized column names and string values

Corrected date formatting (international dayfirst format)

Dropped missing and null records

Created a binary COVID_Impact flag (1 = on/after March 2020)

2. Exploratory Data Analysis (EDA)
   
Unemployment rate trajectory: Rural vs Urban

Distribution analysis (right-skewed — most regions have low unemployment)

Regional ranking by mean unemployment rate

Unemployment spike visualization during COVID period (2020)

3. Statistical Testing
   
Independent t-test — COVID vs non-COVID periods

One-way ANOVA — regional differences in unemployment rates

4. Regression Modelling (OLS)
   
Predictors: Labour Participation Rate, Year, COVID Impact

R² = 0.128; COVID Impact coefficient = 8.39 (p < 0.001)

5. Time Series Analysis
    
Augmented Dickey-Fuller (ADF) test for stationarity

Seasonal decomposition (Trend, Seasonality, Residuals)

Rolling mean (3-month window)

ARIMA(1,1,1) forecasting — 12-step ahead forecast


📈 Key Findings

COVID-19 significantly increased unemployment — T-statistic: 9.975, p-value << 0.05. The difference between COVID and non-COVID periods is statistically significant.

Urban areas were harder hit than rural areas during the lockdown period (March–May 2020).

Regional disparities are statistically significant — ANOVA confirms structural differences across Indian states (p < 0.05).

Labour participation rate is a significant predictor of unemployment (p = 0.008), suggesting structural labour market issues.

Seasonal patterns detected — Decomposition reveals recurring monthly fluctuations in unemployment rates.

ARIMA forecast suggests unemployment rates stabilizing at approximately 12.26% in the short term.


▶️ How to Run

Clone the repository:

     git clone https://github.com/ezrakomen693/Unemployment-Analysis-with-Python.git
     cd Unemployment-Analysis-with-Python

Install required libraries:

     pip install pandas numpy matplotlib seaborn scipy statsmodels

Launch the notebook:

     jupyter notebook Unemployment_Analysis_with_python.ipynb
     
Make sure Unemployment_in_India.csv is in the same directory as the notebook.

👤 Author

* GitHub: [@ezrakomen693](https://github.com/ezrakomen693)


📄 License

This project was completed as part of an internship program. 
# CodeAlpha_Unemployment-Analysis-with-Python
Python analysis of unemployment rate trends, exploring the impact of Covid-19, seasonal patterns, and insights to inform economic and social policy decisions.
