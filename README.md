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

The **Price Optimisation** project aims to assist Hope Freight in determining the most effective pricing strategies to maximise revenue while ensuring customer satisfaction. By leveraging historical sales data, competitor pricing insights, and machine learning-based demand forecasting techniques, the project aims to identify price points that both maximise profitability and cater to customer demand better than competitors.
<img width="1040" alt="Product category per business" src="https://github.com/user-attachments/assets/9fee1496-629c-4bc0-9dd4-b0a06adbd03a">
### Key Focus Areas:
- **Exploratory Data Analysis (EDA)** to uncover trends and relationships between price changes and sales volume.
- **Data Visualisation** to better understand the relationships between price and demand.
- **Competitor Pricing** to predict better prices based on competitor data.
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



## Analysis

The analysis proceeds through these core steps:
1. **Exploratory Data Analysis (EDA)**: Identifying key trends, visualising the relationship between price and sales volume, and understanding the impact of different pricing strategies on demand.
   
   Example Code:
   ```python
   
customer_data = df[['qty', 'total_price', 'customers']]
kmeans = KMeans(n_clusters=3, random_state=42)
df['customer_segment'] = kmeans.fit_predict(customer_data)
print(kmeans.cluster_centers_)```

Machine learning models, such as regression analysis, were used to explore the relationships between product prices, sales quantities, and customer segments. A pricing strategy optimisation model was developed to predict how price changes impact sales volume and revenue. The model also factored in competitor pricing data and historical sales trends to determine the most effective pricing adjustments.
<img width="986" alt="Segment" src="https://github.com/user-attachments/assets/b637b081-77f2-4c62-a98f-254301194733">

## Results/Findings
The analysis showed that small price reductions (e.g., 5%) in select product categories resulted in significant increases in sales volume (up to 15%). This confirmed the presence of price elasticity, where a lower price drives more demand. As a result, revenue was projected to increase by 9% when considering the price reduction. In more detailed simulations, optimising prices further, especially in lower-volume categories, led to a more substantial 15.8% increase in revenue.

## Recommendation
Based on the analysis, it is recommended that Hope Freight implement targeted price reductions in price-sensitive product categories. By adjusting prices for products with higher elasticity, overall sales volume and revenue can be maximised. Additionally, keeping a close watch on competitor pricing and incorporating it into the pricing strategy will further optimise revenue generation.

## Limitations
The analysis was limited by the assumptions made regarding the impact of price changes on demand, which may vary across different customer segments and product categories. Furthermore, the machine learning models used could be improved by incorporating more advanced techniques, such as deep learning or reinforcement learning, to better capture complex customer behaviour patterns.
