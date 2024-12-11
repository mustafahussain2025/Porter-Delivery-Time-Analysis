**Problem Statement**

Porter, India's largest marketplace for intra-city logistics, collaborates with various restaurants to ensure timely delivery of orders to customers. Accurate delivery time estimation is critical to improving customer satisfaction and optimizing operational efficiency. The objective of this project is to predict the delivery time for each order based on multiple attributes, such as restaurant type, items ordered, and the availability of delivery partners.

**Dataset Description and Dictionary**

The dataset provides information about each order with the following columns:

1. **market_id**: ID for the market where the restaurant is located.
2. **created_at**: Timestamp of order placement.
3. **actual_delivery_time**: Timestamp of order delivery.
4. **store_primary_category**: Restaurant category.
5. **order_protocol**: Integer code for the order process (e.g., through Porter, restaurant call, etc.).
6. **total_items**: Total items in the order.
7. **subtotal**: Final price of the order.
8. **num_distinct_items**: Number of unique items in the order.
9. **min_item_price**: Price of the cheapest item.
10. **max_item_price**: Price of the most expensive item.
11. **total_onshift_partners**: Delivery partners available at order time.
12. **total_busy_partners**: Delivery partners busy at order time.
13. **total_outstanding_orders**: Total pending orders at order time.

Dataset: [Download Dataset](https://drive.google.com/file/d/1SzTmeY9FZEnfLchM819C8JD_tI-LwIYx/view?usp=sharing)

**Approach**

1. **Defining the Problem Statement and Data Understanding**
   - Clearly defined the goal to predict delivery times.
   - Imported the dataset and analyzed its structure, shape, and data types.
   - Identified missing values and performed statistical summaries.

2. **Data Preprocessing and Feature Engineering**
   - Cleaned the data by addressing missing values.
   - Created a new target variable: **TimeTakenForDelivery** (difference between `actual_delivery_time` and `created_at`).
   - Extracted features such as hour of the day and day of the week from timestamps.
   - Encoded categorical columns like `store_primary_category` and `order_protocol` using one-hot encoding.
   - Engineered new features like the ratio of `total_busy_partners` to `total_onshift_partners`.

3. **Exploratory Data Analysis (EDA)**
   - Visualized distributions of continuous variables (`subtotal`, `total_items`, etc.) and categorical variables (`store_primary_category`, `order_protocol`).
   - Detected and removed outliers to improve data quality.
   - Plotted correlation heatmaps and pair plots to understand feature relationships.

4. **Advanced Feature Engineering and Statistical Analysis**
   - Analyzed interactions between categorical variables, such as `store_primary_category` and `order_protocol`, on delivery time.
   - Performed statistical tests to identify significant differences in delivery times between groups.

5. **Power BI Report**
   - Created an interactive Power BI dashboard with:
     - Visualizations of order volume trends.
     - Insights on average delivery times by market and restaurant category.
     - Performance metrics for delivery partner availability and order protocols.

**Conclusion**

The project provided actionable insights into factors affecting delivery times:

- **Key Findings**:
  - High delivery times were associated with busy markets, fewer available delivery partners, and complex orders.
  - Restaurant category and order protocol significantly influenced delivery times.

- **Recommendations**:
  - Optimize delivery partner allocation by improving availability during peak hours.
  - Prioritize orders with higher complexity for faster processing.
  - Collaborate with restaurants to streamline order preparation processes.

The integration of predictive modeling with business intelligence tools like Power BI can help Porter enhance its logistics operations and improve customer satisfaction.

