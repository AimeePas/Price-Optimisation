# Price-Optimisation

# Price Optimisation

## Table of Contents

- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools](#tools)
- [Data Cleaning and Pre-processing](#data-cleaning-and-pre-processing)
- [Analysis](#analysis)
- [Results/Findings](#resultsfindings)
- [Recommendations](#recommendations)
- [Limitations](#limitations)
- [REFERENCES](#references)

---

## Project Overview

The **Price Optimisation** project aims to assist Hope Freight in determining the most effective pricing strategies to maximise revenue while ensuring customer satisfaction. By leveraging historical sales data, competitor pricing insights, and machine learning-based demand forecasting techniques, the project aims to identify price points that both maximise profitability and cater to customer demand.

### Key Focus Areas:
- **Exploratory Data Analysis (EDA)** to uncover trends and relationships between price changes and sales volume.
- **Data Visualisation** to better understand the relationships between price and demand.
- **Demand Forecasting** to predict future sales based on historical data.
- **Price Optimisation** to identify the optimal price points that balance revenue and customer satisfaction.

The project utilises machine learning models to analyse historical data, forecast demand, and suggest the best pricing strategies.

---


## Data Sources

The primary dataset used in this project is the **retail_price.csv**, which contains detailed information on various product attributes, pricing, and sales performance. This dataset consists of 676 entries, with 42 columns. Each column provides key insights that help analyse product sales, demand forecasting, and price optimisation strategies. Below is a summary of the dataset's structure:

---

## Tools

This project uses several Python libraries for data analysis, machine learning, and visualisation:

- pandas and numpy for data manipulation.

- matplotlib, seaborn, and plotly for data visualization. Plotly is interactive, making it easier to explore the data.

- sklearn for machine learning algorithms (Random Forest) and performance metrics (MAE, R²).

- eli5 and shap for model explainability.

Benefit: These tools allow us to clean, explore, model, and explain the data efficiently.

---

## Data Cleaning and Pre-processing

### Steps Taken:
1. **Loading the Data**: First, the dataset was inspected to identify any missing or erroneous values.
2. **Handling Missing Values**: Missing data was either imputed or rows with critical missing information were dropped.
3. **Feature Engineering**: Created new features to capture seasonal trends, competitor pricing impacts, and price elasticity.
4. **Normalisation**: Scaled numerical features to ensure consistency across the dataset.
5. **Outlier Detection**: Identified and treated extreme values to avoid skewed results.
6. **Data Splitting**: The dataset was split into training and testing sets to assess model performance.

---

## Analysis

The analysis proceeds through these core steps:
1. **Exploratory Data Analysis (EDA)**: Identifying key trends, visualising the relationship between price and sales volume, and understanding the impact of different pricing strategies on demand.
   
   Example Code:
   ```python
   import seaborn as sns
   sns.scatterplot(data=df, x='Price', y='Sales Volume')
