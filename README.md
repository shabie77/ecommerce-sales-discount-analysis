# 🛒 E-Commerce Sales, Margin & Discount Analysis (2025)

An end-to-end exploratory data analysis (EDA) investigating transactional behavior, promotional discount incidence, category unit economics, fulfillment velocity, and customer loyalty across **50,000 order records totaling $20.06M in recorded gross merchandise value (GMV)**.

---

## 📌 Project Overview & Core Objectives

1. **Promotional Discount Impact:** Evaluate whether checkout discounts drive incremental basket value or erode gross margin across customer tiers.
2. **Category Unit Economics:** Compare median order values against profit margins to assess the true drivers of platform profitability.
3. **Fulfillment Velocity vs. Customer Reviews:** Test the operational hypothesis that delivery transit delays directly degrade customer review ratings.
4. **Payment Gateway Performance:** Measure transaction volume and gross revenue distributions across checkout payment channels.
5. **Customer Tier Spend Behavior:** Determine whether higher-tier loyalty segments (Premium, VIP) demonstrate higher average order spend compared to Regular buyers.

---

## 🛠️ Tech Stack & Analytical Methods

* **Language & Core Libraries:** Python 3.10+, Pandas, NumPy
* **Data Visualization:** Matplotlib, Seaborn (Histograms, KDE distributions, multi-variable subplots, categorical bar charts)
* **Statistical & Analytical Techniques:**
  * Representative sampling estimation and distributional comparison (50k sample vs. 500k population baseline)
  * Robust central tendency evaluation (reporting Medians alongside Means for right-skewed revenue/profit)
  * Categorical aggregation, cohort analysis, and rate-share derivations
  * Data hygiene: contextual imputation of operational nulls (`return_reason`, `coupon_code`, `customer_feedback`)

---

## 📊 Key Findings & Business Insights

| Business Area | Quantitative Finding | Commercial / Operational Takeaway |
| :--- | :--- | :--- |
| **Promotional Discounting** | Flat **~70% discount incidence** across all customer tiers (Regular: 69.99%, Premium: 69.77%, VIP: 69.95%) at an identical ~8.5% average markdown. | Promotional discounts are applied indiscriminately across the customer base. Subsidizing 70% of inelastic VIP orders dilutes gross margin without driving incremental conversion. |
| **Category Unit Economics** | Profit margin remains flat at **~37%** across all 5 categories (Clothing: 36.6%, Electronics: 37.5%, Health: 37.7%, Home: 37.5%, Sports: 37.2%). | No category offers superior margin efficiency. Higher absolute cash contribution is driven purely by higher ticket size (Electronics: $199.50 median profit on $531.47 order vs. Clothing: $67.65 on $184.82). |
| **Delivery vs. Ratings** | Average customer review rating remains virtually flat at **~3.0 stars** across all delivery durations (1 day: 3.02 to 14 days: 3.00) over 37,604 delivered orders. | Operational shipping speed does not drive customer satisfaction within the 1–14 day window. High-cost expedited logistics do not protect customer ratings. |
| **Payment Gateway Adoption** | Order volume (exactly ~20% each) and gross revenue (~$4.0M each) are evenly distributed across all 5 payment options (Apple Pay, Bank Transfer, Credit Card, Debit Card, PayPal). | No single checkout channel dominates platform revenue. Checkout operations do not need channel-specific promotions or gateway steering. |
| **Loyalty Tier Spend** | Median order values are practically identical across tiers: **Regular ($288.18)**, **Premium ($288.31)**, and **VIP ($286.44)**. | Loyalty tiers do not buy more expensive products per visit. Regular customers drive 60% of total revenue ($12.11M) purely due to customer headcount (30,032 orders vs. 4,888 VIP orders). |

---

## 📂 Repository Contents

* `EDA_Project_Ecommerce_2025.ipynb`: Fully executed Jupyter Notebook containing data ingestion, cleaning pipelines, summary tables, statistical commentary, and Seaborn visual outputs.
* `requirements.txt`: Python package dependency specifications.
* `README.md`: Executive summary and strategic business recommendations.

---

## 🚀 How to Run the Notebook

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/shabie77/ecommerce-sales-discount-analysis.git](https://github.com/shabie77/ecommerce-sales-discount-analysis.git)
   cd ecommerce-sales-discount-analysis