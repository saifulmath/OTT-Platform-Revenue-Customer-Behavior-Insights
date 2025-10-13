# OTT-Platform-Revenue-Analysis
Python, Pandas, NumPy, Matplotlib, Seaborn

🔍 Project Overview

This project analyzes OTT platform revenue and customer behavior using multi-source transactional and customer datasets.
The analysis focuses on revenue trends, customer segmentation, cohort-based performance, and key revenue drivers such as payment methods, plan types, and geography.

The ultimate goal is to identify opportunities to improve customer retention, increase repeat purchase rates, and optimize revenue growth.

🎯 Objectives

* Consolidate and clean data from multiple sources (Google Sheets / CSVs)

* Analyze revenue trends by time period and country

* Perform cohort and segment analysis on customer behavior

* Identify top revenue drivers (payment methods, plan types, countries)

* Provide data-driven recommendations to improve customer retention and lifetime value (LTV)

🧾 Dataset Overview

The analysis integrates five data sources:

| Dataset               | Description                                                                                              |
| --------------------- | -------------------------------------------------------------------------------------------------------- |
| **Revenue Data**      | Transaction-level details including order ID, payment date, amount, plan ID, payment method, coupon code |
| **Plan Data**         | Subscription plan details (plan ID, name, duration)                                                      |
| **Countries Data**    | Country name and corresponding ID                                                                        |
| **Subscription Data** | Links orders to customers and plans                                                                      |
| **Customers Data**    | Customer details (ID, name, email, country ID)                                                           |

All sources were merged into a single df_merged dataframe for complete analysis.

🧹 Data Cleaning & Preparation

* Standardized column names to lowercase with underscores

* Handled missing values in coupon_code ('No Coupon') and email columns

* Converted payment_date to datetime and amount to numeric

* Verified data integrity through duplicate checks

* Merged five dataframes using left joins on key fields (order_id, plan_id, customer_id, country_id)

* Removed redundant ID columns and ensured key consistency

📊 Analytical Components
1. Cohort Analysis

* Defined two customer cohorts:

    * Cohort A: Non-offer first joiners

    * Cohort B: Offer first joiners

* Metrics calculated:

    * Total and repeat customers per cohort

    * Revenue from first and repeat purchases

    * Repeat Buyer Rate

    * Average revenue (first and repeat purchase)

    * Lifetime Value (LTV) and Repeat Revenue Share

2. Segmentation

* Customers segmented by loyalty and value:

   * High Loyalty & High Value

   * Low Loyalty & High Value

   * High Loyalty & Low Value

   * Low Loyalty & Low Value

🔑 Key Insights

* Revenue Decline: Noticeable drop after Q1 2025, signaling retention issues.

* Top Revenue Drivers:

    * Payment Methods: Credit card, bank transfer, Google Pay

    * Plan Types: 12-month and 6-month plans outperform shorter terms

    * Countries: Martinique, Timor-Leste, and Qatar contribute the most revenue

* Low Repeat Buyer Rate (< 0.5): A major weakness across all regions and cohorts.

* Opportunity Segment: Low Loyalty & High Value group offers high potential for repeat purchase growth.

💡 Recommendations

1. Boost Customer Retention with targeted re-engagement strategies

2. Focus on ‘Low Loyalty & High Value’ customers for personalized offers

3. Investigate Low Repeat Purchase Causes (survey, feedback, usage data)

4. Optimize Payment Experience for top methods (credit card, Google Pay)

5. Promote Long-Term Plans (12-month, 6-month) through marketing incentives

6. Introduce Tiered Loyalty Programs to increase repeat purchases

7. Use Geo-Specific Strategies based on country performance

8. Launch Personalized Email Campaigns for reactivation

9. Offer Incentives for longer-term subscriptions in low-value cohorts

10. Run A/B Tests on initial offers to determine high-LTV customer drivers

🛠️ Tech Stack

* Python 3.10+

* Libraries:
  pandas, numpy, matplotlib, seaborn, datetime

* Environment: Google Colab / Jupyter Notebook

🚀 How to Run

* Clone this repository:
* 
  git clone https://github.com/<your-username>/Data-Assessment-2.git
  cd Data-Assessment-2
  
* Open the notebook:

  jupyter notebook Data_Assessment_2_Code.ipynb

* Run all cells sequentially to reproduce the analysis.

📄 Report Reference

Detailed findings and visuals:

 Data Assessment 2 Report.pdf

