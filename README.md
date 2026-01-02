# Katangal Grocery Management System

**Goal:** Make Kattangal's Grocery store Profitable using Apriori Algorithm and Clustering of Customers to help the shop owner in making Business decisions and better promotion strategies.

---

## Dataset Overview

| Metric             | Value                         |
| ------------------ | ----------------------------- |
| Total Transactions | **38,765**                    |
| Unique Products    | **167**                       |
| Unique Customers   | **3,898**                     |
| Date Range         | Jan 2014 – Dec 2015 (2 years) |

---

## Deliverables

### 1. Market Basket Analysis (MBA)

**Purpose:** Discover which products are frequently bought together using the **Apriori Algorithm**.

**Business Value:**

- Create bundle offers (e.g., "Buy Whole Milk, get Yogurt at 10% off")
- Optimize shelf placement (place associated items together)
- Prevent lost sales by ensuring "connector" items are always stocked

---

### 2. Exploratory Data Analysis (EDA)

Deep analysis of **What sells, When it sells, and Who buys it**.

---

#### 2.1 Top 10 Best-Selling Items (Bar Chart)

| Rank | Item             | Sales Count |
| ---- | ---------------- | ----------- |
| 1    | **Whole Milk**   | 2,502       |
| 2    | Other Vegetables | 1,898       |
| 3    | Rolls/Buns       | 1,716       |
| 4    | Soda             | 1,514       |
| 5    | Yogurt           | 1,334       |
| 6    | Root Vegetables  | 1,071       |
| 7    | Tropical Fruit   | 1,032       |
| 8    | Bottled Water    | 933         |
| 9    | Sausage          | 924         |
| 10   | Citrus Fruit     | 812         |

**Observations:**

- **Whole Milk dominates** with 2,502 sales (6.5% of all transactions).
- Daily essentials (Milk, Vegetables, Bread) occupy the top 3 spots.
- Beverages (Soda, Water) and fresh produce are consistently popular.

**Conclusion:** These 10 items are **"Must-Stock" products**. Any shortage directly impacts revenue.

---

#### 2.2 Least Sold Items (Dead Stock)

| Item                  | Sales Count |
| --------------------- | ----------- |
| Kitchen Utensil       | 1           |
| Preservation Products | 1           |
| Baby Cosmetics        | 3           |
| Bags                  | 4           |
| Rubbing Alcohol       | 5           |

**Observations:**

- Non-grocery items (utensils, cosmetics) sell extremely poorly.
- These items take up shelf space without generating revenue.

**Conclusion:** Consider **removing or reducing stock** for these items.

---

#### 2.3 Item Diversity

- The store sells **167 unique products**.
- However, the **Top 10 items account for ~35%** of all sales.

**Conclusion:** Focus marketing and inventory on high-performers while maintaining variety.

---

#### 2.4 Sales by Day of Week (Bar Chart)

| Day       | Sales Count         |
| --------- | ------------------- |
| Wednesday | **5,754** (Highest) |
| Tuesday   | 5,663               |
| Saturday  | 5,624               |
| Monday    | 5,524               |
| Thursday  | 5,504               |
| Friday    | 5,397               |
| Sunday    | **5,299** (Lowest)  |

**Observations:**

- **Wednesday is the busiest day** with 5,754 transactions.
- **Sunday is the slowest** with 5,299 transactions.
- The difference between busiest and slowest is only ~8%, indicating **consistent daily demand**.

**Conclusion:** Staff levels can remain relatively stable throughout the week. Consider "Sunday Specials" to boost the slowest day.

---

#### 2.5 Sales by Month (Bar Chart)

| Month     | Sales Count        |
| --------- | ------------------ |
| August    | **3,498** (Peak)   |
| May       | 3,335              |
| January   | 3,333              |
| June      | 3,316              |
| March     | 3,283              |
| November  | 3,273              |
| July      | 3,268              |
| October   | 3,218              |
| April     | 3,172              |
| December  | 3,074              |
| February  | 3,032              |
| September | **2,963** (Lowest) |

**Observations:**

- **August has the highest sales** (3,498 transactions).
- **September is the slowest month** (2,963 transactions).
- Sales are relatively stable year-round (no extreme seasonal drops).

**Conclusion:** Grocery demand is consistent. Planing promotions for September can counter the dip.

---

#### 2.6 Purchase Frequency per Member (Histogram)

| Metric            | Value    |
| ----------------- | -------- |
| Minimum Purchases | 2        |
| Maximum Purchases | **36**   |
| Average (Mean)    | **9.94** |
| Median            | **9**    |

**Observations:**

- Most customers make around **9-10 purchases** over the 2-year period.
- Top customer (**Member 3180**) made **36 purchases** – a true VIP.
- Other VIPs: Members 2051, 3050, 3737 (33 purchases each).

**Conclusion:** The distribution is relatively even. Loyalty programs can convert average customers (9 purchases) into VIPs (30+).

---

#### 2.7 Monthly Sales Comparison: 2014 vs 2015 (Grouped Bar Chart)

| Month     | 2014  | 2015  | Change     |
| --------- | ----- | ----- | ---------- |
| January   | 1,504 | 1,829 | **+21.6%** |
| February  | 1,547 | 1,485 | -4.0%      |
| March     | 1,491 | 1,792 | **+20.2%** |
| April     | 1,506 | 1,666 | +10.6%     |
| May       | 1,625 | 1,710 | +5.2%      |
| June      | 1,525 | 1,791 | **+17.4%** |
| July      | 1,623 | 1,645 | +1.4%      |
| August    | 1,535 | 1,963 | **+27.9%** |
| September | 1,350 | 1,613 | +19.5%     |
| October   | 1,555 | 1,663 | +6.9%      |
| November  | 1,496 | 1,777 | **+18.8%** |
| December  | 1,520 | 1,554 | +2.2%      |

**Observations:**

- **August 2015 showed the highest YoY growth** at +27.9% (from 1,535 to 1,963).
- **February was the only month with negative growth** (-4.0%).
- Overall, 2015 outperformed 2014 in 11 out of 12 months.
- Strong growth months: January (+21.6%), March (+20.2%), November (+18.8%).

**Conclusion:** The store is on a positive growth trajectory. Investigate why February dipped and replicate August's success.

---

#### 2.8 Day vs Month Heatmap (Multivariate)

**What it shows:** A heatmap identifying "hotspot" combinations of specific days and months.

**Top 5 Hotspots (Busiest Cells):**

| Month   | Day       | Transactions |
| ------- | --------- | ------------ |
| April   | Wednesday | **606**      |
| January | Thursday  | 581          |
| May     | Friday    | 578          |
| March   | Sunday    | 564          |
| June    | Monday    | 559          |

**Bottom 5 (Slowest Cells):**

| Month     | Day      | Transactions |
| --------- | -------- | ------------ |
| April     | Monday   | **329**      |
| December  | Saturday | 346          |
| September | Monday   | 358          |
| September | Thursday | 363          |
| May       | Monday   | 364          |

**Observations:**

- **April Wednesdays are the busiest** with 606 transactions.
- **April Mondays are the slowest** with only 329 transactions.
- Mondays appear frequently in the "slowest" list.
- The gap between hottest (606) and coldest (329) is significant (~85% difference).

**Conclusion:** Run flash sales on Mondays. Staff up for April Wednesdays and January Thursdays.

### 3. Customer Segmentation (RFM & K-Means)

Customers are grouped based on:

- **Recency (R):** Days since last purchase
- **Frequency (F):** Number of shopping trips
- **Monetary (In this case, M is the total number of items purchased):** Total items purchased

| Segment                   | Description                   | Strategy                              |
| ------------------------- | ----------------------------- | ------------------------------------- |
| **VIP / Champions**       | Recent, Frequent, High Volume | Loyalty rewards, VIP access           |
| **Occasional / Regulars** | Moderate activity             | Upsell offers, personalized discounts |
| **Lost / At-Risk**        | Haven't shopped recently      | Win-back campaigns, special offers    |

---

## Key Questions Answered

**Q: What are the most frequently sold items?**

**A:** The top 5 items are:

1. Whole Milk (2,502 sales)
2. Other Vegetables (1,898)
3. Rolls/Buns (1,716)
4. Soda (1,514)
5. Yogurt (1,334)

---

**Q: What are the most important items that should always be in the store?**

**A:** The top 5 essential items with their frequently associated products:

| Item                 | Associated Items (Often Bought Together)       |
| -------------------- | ---------------------------------------------- |
| **Whole Milk**       | ['other vegetables', 'rolls/buns', 'sausage', 'soda'] |
| **Other Vegetables** | ['rolls/buns', 'soda', 'tropical fruit', 'whole milk']                 |
| **Rolls/Buns**       | ['other vegetables', 'root vegetables', 'soda', 'tropical fruit']    |
| **Soda**             | ['other vegetables', 'rolls/buns', 'root vegetables', 'sausage']                                      |
| **Yogurt**           | ['citrus fruit', 'other vegetables', 'rolls/buns', 'sausage']                                      |

**Business Insight:** If a customer asks for Sausage and it's out of stock, they may skip buying Yogurt, Soda, whole milk and other vegetables too. These "connector" items prevent basket abandonment.

---

## Tech Stack

- **Python** (Pandas, NumPy)
- **Visualization:** Matplotlib, Seaborn, Plotly
- **MBA:** Mlxtend (Apriori)
- **Clustering:** Scikit-Learn (K-Means)


