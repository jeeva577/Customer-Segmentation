Customer Segmentation using RFM Analysis

📌 Project Overview

This project performs customer segmentation using RFM (Recency, Frequency, Monetary) analysis on retail transaction data.

The goal is to understand customer purchasing behaviour, group customers with similar characteristics, and provide actionable insights that can support customer retention, re-engagement, and marketing strategies.

The project uses Python for data cleaning, RFM analysis, transformation, and clustering, and Power BI for interactive visualization and dashboard reporting.

🎯 Project Objectives

Clean and prepare retail transaction data.

Calculate customer-level RFM metrics.

Analyse the statistical distribution of RFM values.

Handle skewed RFM features using logarithmic transformation.

Standardize RFM features before clustering.

Determine a suitable number of customer clusters using the Elbow Method and Silhouette Score.

Apply K-Means clustering to segment customers.

Convert clusters into meaningful business-oriented customer segments.

Build an interactive Power BI dashboard to communicate the results.

🛠️ Technologies Used

Python

Pandas – data cleaning and manipulation

NumPy – numerical transformations

Matplotlib – data visualization

Scikit-learn – StandardScaler, K-Means, and Silhouette Score

Jupyter Notebook

Power BI – dashboard and business reporting

Git & GitHub – version control and project sharing

📊 Dataset

The project uses retail transaction data containing information such as:

Customer ID

Invoice Number

Invoice Date

Quantity

Unit Price

Transaction information

During data preparation, invalid transaction records were removed based on non-positive Quantity and UnitPrice values.

After cleaning:

3,926,920 transaction rows remained.

4,338 unique customers were used for RFM analysis.

🔍 RFM Analysis

RFM represents three important dimensions of customer behaviour:

Recency

Measures how recently a customer made a purchase.

Lower Recency = more recent purchase = better customer engagement

Frequency

Measures how often a customer purchased.

Higher Frequency = more repeat purchases

Monetary

Measures the total amount spent by a customer.

Higher Monetary = higher customer value

The resulting customer-level dataset contains:

Customer

Recency

Frequency

Monetary

Customer-level records

Days

Purchase count

Total spend

📈 Data Transformation

The RFM distributions were analysed using descriptive statistics, histograms, and skewness.

Because Frequency and Monetary showed strong right-skewness, a logarithmic transformation was applied using:

np.log1p()

The transformed RFM features were then standardized using:

StandardScaler()

This ensures that Recency, Frequency, and Monetary contribute more comparably to the clustering algorithm.

🤖 Customer Clustering

K-Means clustering was applied to the transformed and standardized RFM data.

The number of clusters was evaluated using:

1. Elbow Method

The inertia was calculated for different values of k from 2 to 10.

2. Silhouette Score

Silhouette scores were compared across the same range of k.

Based on the clustering evaluation and business interpretability, 4 customer clusters were selected.

👥 Customer Segments

The four clusters were interpreted into business-oriented customer segments:

Segment

Customers

Avg. Recency

Avg. Frequency

Avg. Monetary

🏆 Champions

713

12.17

13.75

8,088.02

🔄 Regular Customers

1,166

71.64

4.08

1,801.78

🎯 Potential Customers

837

17.70

2.19

557.32

⚠️ At-Risk Customers

1,622

181.51

1.32

341.00

🏆 Champions

Recent, frequent, and high-value customers.

Suggested action: Reward loyalty, provide exclusive benefits, and encourage continued engagement.

🔄 Regular Customers

Consistent customers with moderate purchase activity and value.

Suggested action: Use upselling and cross-selling strategies to increase customer value.

🎯 Potential Customers

Customers who purchased relatively recently but have lower purchase frequency and monetary value.

Suggested action: Encourage repeat purchases through targeted offers and recommendations.

⚠️ At-Risk Customers

Customers with high recency values and low purchase frequency/value, indicating that they have not purchased recently.

Suggested action: Run re-engagement campaigns and targeted offers to encourage them to return.

📊 Power BI Dashboard

The Power BI dashboard provides a visual summary of customer segmentation.

KPI Cards

Total Customers: 4,338

Regular Customers: 1,166

Potential Customers: 837

Champions: 713

At-Risk Customers: 1,622

Dashboard Visuals

Customer Distribution by Segment

Average Monetary Value by Segment

Average Purchase Frequency by Segment

Average Recency by Segment

Segmentation Insights summary

The dashboard is designed to make customer behaviour and segment-level differences easy to understand.

💡 Key Business Insights

Champions represent the highest-value and most frequent customers, making them important for loyalty and retention strategies.

At-Risk Customers form the largest segment, with 1,622 customers and an average recency of 181.51 days.

Potential Customers have relatively recent purchases but low frequency, providing an opportunity to increase repeat purchases.

Regular Customers show consistent purchasing behaviour and can be targeted for upselling and cross-selling.

Monetary value varies substantially between customer segments, demonstrating the usefulness of RFM-based segmentation for targeted marketing.

📁 Project Structure

Customer-Segmentation/
│
├── dashboard/
│   └── Customer_Segmentation.png
│
├── data/
│   └── customer_segmentation.csv
│
├── Notebook/
│   └── clean.ipynb
│
├── powerBi/
│   └── Customer-Segmentation.pbix
│
└── readme.md

🚀 Project Workflow

Raw Transaction Data
        ↓
Data Cleaning
        ↓
Customer-Level RFM Calculation
        ↓
Statistical Analysis
        ↓
Skewness Analysis
        ↓
Log Transformation
        ↓
Standardization
        ↓
K-Means Clustering
        ↓
Elbow + Silhouette Evaluation
        ↓
4 Customer Clusters
        ↓
Business Segment Interpretation
        ↓
Power BI Dashboard

📌 Conclusion

This project demonstrates an end-to-end customer analytics and segmentation workflow, starting from raw transaction data and ending with an interactive business dashboard.

RFM analysis combined with K-Means clustering helps transform transactional data into meaningful customer groups that can support customer retention, re-engagement, loyalty, and targeted marketing decisions.

👤 Author

Jeeva

This project was developed as a data analytics portfolio project using Python, machine learning, and Power BI.
