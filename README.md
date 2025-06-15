# Sales-data-analysis

# 🧪 Data Exploration and Visualization Using Python (Pandas, Matplotlib, Seaborn)

![Logo](https://github.com/vikassaraswatiitg26/vikas_portfolio/blob/main/images/Sales.png)

## 🎯 Objective :

This project uses Python (with Pandas and Matplotlib/Seaborn) to analyze and visualize a retail or transaction dataset. The goal is to derive meaningful insights such as popular product combinations, hourly trends, and sales patterns by grouping and analyzing the data.

---

# 📌 Project Overview

## The dataset contains features such as:

- Product ID and name
- Store and region info
- Inventory, sales, and demand metrics
- Temporal data like hour and date

### The notebook explores:

• Popular product combinations using combinations from `itertools`.

• Hourly sales patterns through grouping and plotting.

• Inventory trends and relationships between sales and demand.

• Summarizing metrics per product, region, or store.

---

# 🛠️ Tools & Technologies

• Python (Pandas, Matplotlib, Seaborn, Collections, itertools)

• Jupyter Notebook

• Data Source: Custom synthetic or retail dataset

---

# 🔍 Key Code Snippets

### 1. Counting 3-Item Combinations

```
from itertools import combinations
from collections import Counter

count = Counter()
for row in df['grouped']:
    row_list = row.split(',')
    count.update(Counter(combinations(row_list, 3)))
```
2. Grouping by Hour to Plot Activity

```
hours = [hour for hour, df in all_data.groupby('hour')]
plt.plot(hours, all_data.groupby('hour').count()['Order ID'])
plt.xticks(hours)
plt.grid()
plt.title("Orders per Hour")

```
3. Product Grouping and Sales Summary

   ```
   product_group = all_data.groupby('Product')
   products = [product for product, df in product_group]
   sales = product_group.sum()['Sales']

   ```
📈 Insights & Observations

• Most orders are placed between 11 AM and 7 PM.
• Some product combinations (e.g., phone + charger) appear frequently together.
• Certain products have high volume but low revenue; others have the opposite.

✅ Future Enhancements

• Create an interactive dashboard using Plotly Dash or Streamlit.
• Use ML models to predict product demand or recommend bundles.
• Clean and scale the project with a modular script-based pipeline
