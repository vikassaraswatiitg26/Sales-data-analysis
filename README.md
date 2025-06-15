# Sales-data-analysis

# 🧪 Data Exploration and Visualization Using Python (Pandas, Matplotlib, Seaborn)

![Logo](https://www.google.com/search?sca_esv=3bb0e53af8618b52&sxsrf=AE3TifMobUhHHoWQCNx4dMjBiVYzXNygEg:1750010566988&q=sales+data+%5C&udm=2&fbs=AIIjpHxU7SXXniUZfeShr2fp4giZ1Y6MJ25_tmWITc7uy4KIeqDdErwP5rACeJAty2zADJgeXKnD4z7v_UXM32TmNnj1pwmxcNrkVFnLviTtK6Qh7QZ7ETFlEgKlZQoYAcoHbKmDKAfYNUEMhfvG0vewyj1B9BkfFQuXSJJhEq7h3D79qA9HleJCADxibAJ86Hzb9y79KeCvwxr0X3BByyRHSIq1O5WjVA&sa=X&ved=2ahUKEwjOg8uxgfSNAxX4nGMGHS0lHa4QtKgLegQIFRAB&biw=1536&bih=730&dpr=1.25#vhid=koH1t6GneLa_JM&vssid=mosaic)

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

```python
from itertools import combinations
from collections import Counter

count = Counter()
for row in df['grouped']:
    row_list = row.split(',')
    count.update(Counter(combinations(row_list, 3)))

