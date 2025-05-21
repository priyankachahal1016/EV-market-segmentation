# EV Market Analysis in India

## Project Overview

This project provides a comprehensive data-driven analysis of the Indian Electric Vehicle (EV) ecosystem, focusing on manufacturer distribution, vehicle category trends, charging infrastructure, and sales growth patterns. Using multiple real-world datasets and machine learning techniques, we identify key market segments, regional disparities, and strategic opportunities for EV adoption and infrastructure investment.

---

## Data Sources

- **EV Maker by Place:** State-wise list of EV manufacturers
- **OperationalPC:** State-wise count of operational public charging stations (PCS)
- **Vehicle Class - All:** National vehicle registration data by class
- **ev_cat_01-24:** Monthly EV registration data by category
- **ev_sales_by_makers_and_cat_15-24:** Annual EV sales by maker and category

---

## EDA Process

**1. Data Collection and Loading:**  
All datasets were loaded using pandas and checked for consistency.

**2. Feature Engineering:**  
- Market share for each state and manufacturer was calculated.
- Year-over-year growth rates and cumulative sales were computed for each vehicle category and state.

**3. Aggregation:**  
Data was grouped by state, vehicle category, and year to facilitate trend analysis and regional comparisons.

**4. Visualization:**  
Key insights were visualized using bar plots, line charts, pie charts, and scatter plots.  
For example, the scatter plot below shows state-wise clustering by number of public charging stations (PCS):

**5. Clustering:**  
K-Means clustering was applied to the PCS data, segmenting states into high, medium, and low infrastructure readiness groups.

---

## Key EDA Insights

- **Manufacturer Landscape:** Maharashtra leads with the highest number of EV makers, followed by Tamil Nadu and Karnataka.
- **Vehicle Category Trends:** Two-wheelers (2W) dominate EV sales, with three-wheelers (3W) as the next largest segment. LMV and MMV remain niche.
- **Charging Infrastructure:** Maharashtra, Delhi, and Karnataka have the most public charging stations. Many states, especially in the Northeast, have very limited infrastructure.
- **Growth Rates:** 2W CAGR (2015–2024) is 93.6%; 3W CAGR is 60.0%.
- **Clustering:** Maharashtra is a clear outlier with exceptional infrastructure; Delhi, Karnataka, and Kerala form a mid-tier; most other states have <500 PCS.

---

## Predictive Modeling

- **ARIMA Model:** Used for time series forecasting of 2W sales. RMSE: 1,068,868 (high due to recent volatility).
- **ETS Model:** Provided a better fit with RMSE: 443,259. Five-year forecast predicts 2W sales will exceed 1 million units by 2029.

---

## Recommendations

- **Market Entry:** Focus on Maharashtra, Tamil Nadu, and Karnataka for initial EV rollout.
- **Product Strategy:** Prioritize 2W and 3W segments for maximum impact.
- **Infrastructure:** Invest in PCS expansion in low-readiness states to unlock new markets.
- **Data-Driven Expansion:** Use clustering and forecasting results to guide phased investment and marketing.

## Dependencies

- Python 3.8+
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- statsmodels
- plotly (for interactive plots)
