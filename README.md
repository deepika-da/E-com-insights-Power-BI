The goal of this project is to analyze:

Delivery speed and delay patterns

Customer satisfaction and rating behavior

Refund trends and operational issues

Customer feedback using sentiment analysis

Platform and product category performance

The dashboard answers key business questions:
✔ Which platform delivers faster?
✔ What causes refunds?
✔ How do delays impact ratings?
✔ What are customers talking about in feedback?
✔ Which categories perform best?

🛠️ Data Cleaning & Processing (Python)
✔ Handled inconsistent datetime formats

Converted mixed date formats into a single standardized datetime field.

✔ Cleaned customer feedback text

Lowercasing

Removing special characters

Stripping extra spaces

Generating cleaned text column

✔ Polarity & Sentiment Extraction

Applied sentiment scoring to generate:

Polarity (numeric)

Sentiment Label (Positive / Negative / Neutral)

✔ Word Cloud generation

Created a word cloud from customer feedback for text insights.

📊 **Power BI Dashboard Structure**
📄 **Page 1 – Delivery Performance**

Total Orders

Total Sales

Average Delivery Time

Delay Rate %

Delivery Time by Platform

Category-wise Sales

On-Time vs Delayed distribution

Clean navigation sidebar with platform logos

Insight: Delivery times are consistent across platforms (~29–30 mins). Delays occur in ~14% of orders.

📄 **Page 2 – Customer Satisfaction**

Average Rating (with custom star rating visual)

5-Star Ratings count

On-Time vs Delayed Orders

Rating by Platform

Category-wise Rating (Treemap)

Delay Impact on Rating

Delayed Delivery Trends

Insight: Ratings remain stable at ~3.24 across platforms. Delayed orders show only a slight drop in rating.

📄 **Page 3 – Refund & Feedback Analysis**

Total Refund Requests

Positive vs Negative Feedback %

Platform Refund Rate %

Category Refund Rate %

Delay vs Refund Flag

Customer Feedback Word Cloud

Negative/Positive sentiment distribution

Insight: Refunds strongly correlate with delayed deliveries. Dairy & Snacks show higher refund proportion.

🧮 **Key DAX Measures Used**
Delivery Metrics
Avg Delivery Time = AVERAGE('Ecommerce_Delivery'[Delivery Time (Minutes)])
Delay Rate % = DIVIDE([Delayed Orders], [Total Orders])

Rating Metrics
Avg Rating = AVERAGE('Ecommerce_Delivery'[Service Rating])
Avg Rating On-Time = CALCULATE([Avg Rating], 'Ecommerce_Delivery'[Delay_Flag] = 0)
Avg Rating Delayed = CALCULATE([Avg Rating], 'Ecommerce_Delivery'[Delay_Flag] = 1)

Refund Metrics
Refund Rate % = DIVIDE([Total Refunds], [Total Orders])

Sentiment
Positive Feedback % = DIVIDE([Positive Count], [Total Feedback])

📁 Files Included

Ecommerce_Delivery_Dashboard.pbix – Power BI Dashboard

Ecommerce_Delivery_Analytics_New.csv – Dataset

data_cleaning.ipynb – Python Text Cleaning & Sentiment Notebook

Word Cloud PNG

Custom logo used in the dashboard

README.md (this file)

💡 Insights Summary

Delivery delays have the biggest impact on refunds.

Customer ratings are consistent across platforms, showing stable satisfaction levels.

Word cloud highlights common themes like packaging, delivery time, product quality.

Snacks, Fruits, and Dairy are high-volume categories driving orders.

🧑‍💼 Author

Deepika K
Data Analyst | Power BI | Python | SQL | Dashboard Development
