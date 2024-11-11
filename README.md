# Price Optimisation

## Table of Contents

- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools](#tools)
- [Data Cleaning and Pre-processing](#data-cleaning-and-pre-processing)
- [Analysis](#analysis)
- [Findings](#findings)
- [Conclusion](#conclusion)
- [Recommendations](#recommendation)
- [Limitations](#limitations)


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

They allow us to clean, explore, model, and explain data efficiently.

---

## Data Cleaning and Pre-processing



## Analysis

The analysis proceeds through these core steps:
1. **Exploratory Data Analysis (EDA)**: Identifying key trends, visualising the relationship between price and sales volume, and understanding the impact of different pricing strategies on demand.
   
   Example Code: To understand customers buying patterns and tailor pricing strategies accordingly.

``` python
   
customer_data = df[['qty', 'total_price', 'customers']]
kmeans = KMeans(n_clusters=3, random_state=42)
df['customer_segment'] = kmeans.fit_predict(customer_data)
print(kmeans.cluster_centers_)

```

<img width="986" alt="Segment" src="https://github.com/user-attachments/assets/b637b081-77f2-4c62-a98f-254301194733">

### Cluster 0:
Customers in this cluster tend to buy a moderate amount of items (8.6) and spend a moderate amount (£602). This group might represent "casual" customers.

### Cluster 1: 
Customers here make relatively larger purchases in terms of both quantity (24.78 items) and total spending (£2704). They might be classified as "high-value" customers.

### Cluster 2:
This cluster includes customers who buy the most items (49.71) and spend the most money (£7165). These customers could be considered as "premium" customers.


Machine learning models, such as regression analysis, were used to explore the relationships between product prices, sales quantities, and customer segments. A pricing strategy optimisation model was developed to predict how price changes impact sales volume and revenue. The model also factored in competitor pricing data and historical sales trends to determine the most effective pricing adjustments.

## Findings

### Simulated Sales Increase After Price Reduction:
The impact of a 5% price reduction on select product categories has shown a significant simulated sales increase of 15%. This indicates a strong price elasticity of demand, where customers are more likely to purchase when prices are slightly lower. The results from the simulation suggest that lowering prices by a small margin can trigger a noticeable uptick in sales volume, especially in categories that are more responsive to pricing changes.

The overall sales volume boost, driven by the 15% increase for products with adjusted prices, resulted in a better uplift in monthly revenue. This success was due to a strategic price reduction in specific categories, combined with insights from competitor pricing. By analyzing these insights, adjustments were made in a way that maximized the sales volume increase, thereby improving the overall revenue performance.


### Boost in Projected Monthly Revenue:

Following the 5% price reduction, projected monthly revenue increased from £961,421 to £1,050,352, representing a 9% revenue boost. This demonstrates how even a modest price cut, when paired with an increase in sales volume, can generate significant revenue growth. The increase in sales volume more than compensates for the slight reduction in unit prices.

In the second scenario, where a 15% sales volume increase was applied to products with adjusted prices, revenue surged even further. The baseline revenue of £961,421 grew to £1,113,405, resulting in a revenue boost of £15.8%. 

This clearly illustrates that targetted adjustment has a powerful effect on overall revenue,*outperforming* simple price reductions alone. By focusing on categories that are more responsive to price changes, and taking into account average volume sold, businesses can optimize businesses can optimize their pricing strategy to generate even greater revenue growth.

### Impact on High-Volume Products:

For categories with already high sales volumes, such as garden_tools, the price reduction had a measurable effect on unit sales. However, even without changing the sales strategy for high-volume products, the overall revenue still increased substantially due to targeted adjustments in lower-volume categories. These products, which are more price-sensitive, responded well to the price reduction and the sales volume increase, driving the overall revenue up without needing to focus on high-volume items alone.

High-volume products often contribute significantly to revenue, but this analysis highlights the importance of targeting price-sensitive categories to drive additional revenue growth.


### Key Insights:

###Price Reduction Effect:

targetted price reduction of 5% in the first scenario and up to 15%  in the second scenario lead to a higher overall revenue. This highlights the power of strategic price reductions in responsive categories.


###Price Increase Effect: While price increases were only directly applied in the second scenario, it has shown how price increases contributes tooverall revenue growth. A higher price might indicate better quality, and adjusting prices based on competitor pricing has the ability to increase revenue.

###Customer Demand Sensitivity:

Price sensitivity varies by category. Certain products show strong demand responses to price changes, suggesting that these categories are more price-elastic. Recognising these categories allows businesses to adjust prices in a way that maximizes revenue.



### Simulated Sales Increase After Price Reduction:
The impact of a 5% price reduction on select product categories has shown a significant simulated sales increase of 15%. This indicates a strong price elasticity of demand, where customers are more likely to purchase when prices are slightly lower. The results from the simulation suggest that lowering prices by a small margin can trigger a noticeable uptick in sales volume, especially in categories that are more responsive to pricing changes.

The overall sales volume boost, driven by the 15% increase for products with adjusted prices, resulted in a better uplift in monthly revenue. This success was due to a strategic price reduction in specific categories, combined with insights from competitor pricing. By analyzing these insights, adjustments were made in a way that maximized the sales volume increase, thereby improving the overall revenue performance.


### Boost in Projected Monthly Revenue:

Following the 5% price reduction, projected monthly revenue increased from £961,421 to £1,050,352, representing a 9% revenue boost. This demonstrates how even a modest price cut, when paired with an increase in sales volume, can generate significant revenue growth. The increase in sales volume more than compensates for the slight reduction in unit prices.

In the second scenario, where a 15% sales volume increase was applied to products with adjusted prices, revenue surged even further. The baseline revenue of £961,421 grew to £1,113,405, resulting in a revenue boost of £15.8%. 

This clearly illustrates that targetted adjustment has a powerful effect on overall revenue,*outperforming* simple price reductions alone. By focusing on categories that are more responsive to price changes, and taking into account average volume sold, businesses can optimize businesses can optimize their pricing strategy to generate even greater revenue growth.

### Impact on High-Volume Products:

For categories with already high sales volumes, such as garden_tools, the price reduction had a measurable effect on unit sales. However, even without changing the sales strategy for high-volume products, the overall revenue still increased substantially due to targeted adjustments in lower-volume categories. These products, which are more price-sensitive, responded well to the price reduction and the sales volume increase, driving the overall revenue up without needing to focus on high-volume items alone.

High-volume products often contribute significantly to revenue, but this analysis highlights the importance of targeting price-sensitive categories to drive additional revenue growth.


### Key Insights:

###Price Reduction Effect:

targetted price reduction of 5% in the first scenario and up to 15%  in the second scenario lead to a higher overall revenue. This highlights the power of strategic price reductions in responsive categories.


###Price Increase Effect: While price increases were only directly applied in the second scenario, it has shown how price increases contributes tooverall revenue growth. A higher price might indicate better quality, and adjusting prices based on competitor pricing has the ability to increase revenue.

###Customer Demand Sensitivity:

Price sensitivity varies by category. Certain products show strong demand responses to price changes, suggesting that these categories are more price-elastic. Recognising these categories allows businesses to adjust prices in a way that maximizes revenue.



## Conclusion
This analysis demonstrates the value of machine learning in optimizing pricing by understanding price elasticity the relationship between price changes and customer purchasing behavior. By using historical data, machine learning models help estimate demand responses,enabling Hope Freight to make informed pricing decisions that will drive the greatest revenue growth. Through strategic price adjustments and sales volume , businesses can fine-tune their pricing strategies to enhance profitability, even in the face of slightly reduced margins.



## Recommendation
Based on the analysis, it is recommended that Hope Freight implement targeted price reductions in price-sensitive product categories. By adjusting prices for products with higher elasticity, overall sales volume and revenue can be maximised. Additionally, keeping a close watch on competitor pricing and incorporating it into the pricing strategy will further optimise revenue generation.

## Limitations
The analysis was limited by the assumptions made regarding the impact of price changes on demand, which may vary across different customer segments and product categories. Furthermore, the machine learning models used could be improved by incorporating more advanced techniques, such as deep learning or reinforcement learning, to better capture complex customer behaviour patterns.
