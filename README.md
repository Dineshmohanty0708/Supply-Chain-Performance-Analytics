Supply Chain Performance & Delivery Optimization Analytics

Academic Internship Project --- IBM SkillsBuild Data Analytics with
AI
Submitted by: Dinesh Mohanty | B.Tech -- Computer Science
Engineering

📌 Project Overview

This project analyzes the DataCo SMART Supply Chain dataset to
understand supply chain performance, delivery efficiency, sales,
profitability, product performance, customer segments, and geographical
patterns.

The analysis is performed using Python in Jupyter Notebook, with the
results structured for business reporting and a planned Power BI
dashboard.

The project focuses on identifying delivery delays, comparing shipping
modes, understanding regional and product-level performance, studying
discounts and profitability, and tracking changes over time.

🎯 Project Objectives

The main objectives of this project are to:

Analyze overall supply chain delivery performance.

Compare late-delivery rates across different shipping modes.

Identify regions, markets, and countries with delivery issues.

Analyze sales and profitability across products and categories.

Identify product categories associated with higher delivery risk.

Examine the relationship between discounts, sales, and
profitability.

Compare sales and profitability across regions and customer
segments.

Understand the contribution of different customer segments.

Analyze monthly changes in sales, profit, and delivery performance.

Identify areas that may require further management attention.

❓ Business Questions

The analysis addresses the following business questions:

Delivery & Supply Chain

What is the overall delivery performance?

Which shipping modes have the highest late-delivery rate?

Which regions, markets, and countries experience more delivery
problems?

Product & Operations

Which product categories and products have the highest sales and
profitability?

Which product categories have higher delivery-delay rates?

Sales & Profitability

How does discount rate relate to sales and profitability?

Which regions and customer segments generate the most sales and
profit?

Customer & Time Analysis

Which customer segments contribute most to overall business
performance?

How does supply chain performance change over time?

Management Analysis

Which areas require further operational investigation?

📊 Dataset

The project uses the DataCo SMART Supply Chain dataset.

Attribute            Details

Dataset              DataCoSupplyChainDataset.csv
Records              180,519
Columns              53
Unique Orders        65,752
Unique Customers     20,652
Unique Products      118
Product Categories   50
Shipping Modes       4
Data Period          2015--2018
Data Granularity     Order-item / line-item level

Important Data Consideration

The dataset is stored at order-item level, meaning one Order Id
can appear across multiple rows.

Therefore:

Raw row counts should not automatically be treated as order counts.

Order-level KPIs should use distinct Order Id counts where
appropriate.

Delivery rates calculated directly from rows represent
line-item-level results.

🛠️ Technologies & Tools

Technology                          Purpose

Python                          Data preprocessing, analysis,
feature engineering and
visualization

Pandas                          Data loading, cleaning,
transformation and grouping

NumPy                           Numerical operations

Matplotlib                      Data visualization

Seaborn                         Exploratory and statistical
visualizations

Jupyter Notebook                Project development and
reproducible analysis

🔄 Project Methodology

The project follows a structured data analytics workflow:

Business Problem
       ↓
Dataset Understanding
       ↓
Data Quality Assessment
       ↓
Data Cleaning & Preprocessing
       ↓
Feature Engineering
       ↓
Exploratory Data Analysis
       ↓
Business Analysis
       ↓
Key Findings & Recommendations
       ↓
Power BI Reporting Layer

🧹 Data Cleaning & Preprocessing

The notebook performs the following preprocessing activities:

Loads the CSV dataset using latin1 encoding.

Checks dataset shape, columns, data types and summary statistics.

Performs missing-value analysis.

Checks for duplicate records.

Reviews the order-item structure.

Removes completely empty Product Description.

Removes Order Zipcode because of substantial missing values.

Removes customer detail fields that are not required for business
analysis, including:

Customer Email

Customer Password

Customer Fname

Customer Lname

Customer Street

Customer Zipcode

Removes Product Image because it is not required for analytical
reporting.

Converts order and shipping date fields to datetime format.

Validates the cleaned dataset before analysis.

No completely duplicated rows were found in the notebook.

Sensitive or unnecessary customer-level fields are excluded from the
analytical workflow to keep the analysis focused on business metrics and
reduce unnecessary exposure of personal information.

⚙️ Feature Engineering

The project creates analytical fields to support business analysis:

Order Month

The order date is converted into a monthly period to analyze:

Monthly sales

Monthly profit

Monthly delivery performance

Late Delivery Rate

Late_delivery_risk is aggregated as a percentage to compare delivery
performance across:

Shipping modes

Regions

Markets

Product categories

Time periods

Average Items per Order

The notebook calculates the average number of line items per unique
order to better understand the order-item structure.

📈 Exploratory & Business Analysis

The notebook contains analysis across several business dimensions.

1. Delivery Performance

The overall delivery-status distribution is analyzed using counts and
percentages.

Key result:

Late delivery: 54.83%

Advance shipping: 23.04%

Shipping on time: 17.84%

Shipping canceled: 4.30%

These percentages are based on dataset records/line items, not unique
orders.

2. Shipping Mode Analysis

Late-delivery rates are compared across shipping modes using the
Late_delivery_risk indicator.

The notebook calculates rates rather than relying only on raw delayed
counts, making comparisons more meaningful when transaction volumes
differ.

3. Regional & Market Analysis

Delivery performance is analyzed across:

Order Region

Market

Country-level data available in the dataset

This helps identify geographical differences in delivery performance.

4. Product & Category Analysis

The project analyzes:

Sales by product category

Profit by product category

Top 10 products by sales

Top 10 products by profit

Late-delivery rate by product category

This helps distinguish commercial performance from delivery performance.

5. Discount Analysis

The notebook examines:

Discount-rate distribution

Average sales by discount rate

Average profit by discount rate

Correlation between discount, sales and profit

The relationship is interpreted as an association, not proof of a
causal relationship.

6. Customer & Regional Performance

Sales and profit are analyzed across:

Order Region

Customer Segment

This provides a view of where business value is concentrated.

7. Time-Based Analysis

The project analyzes monthly:

Sales

Profit

Late-delivery rate

This provides a time-based view of commercial and supply-chain
performance.

📌 Key Project Metrics

The notebook produces the following management-level metrics:

Metric                           Result

Total Sales                      36.78M
Total Profit                      3.97M
Late Delivery Rate               54.83%
Average Discount Rate            10.17%
Unique Orders                    65,752
Unique Customers                 20,652
Unique Products                     118
Average Line Items per Order       2.75

Values are based on the analysis performed in the supplied Jupyter
Notebook.

🔍 Key Findings

Delivery Performance

Late delivery is the largest delivery-status category in the
analyzed records, at 54.83%.

Delivery performance differs across shipping modes, regions, markets
and product categories.

Delivery performance is therefore an important area for further
operational investigation.

Product & Profitability

Product categories differ in both sales and profitability.

Products with high sales are not necessarily the same products with
the highest profitability.

Product-level analysis helps identify where commercial and
operational performance differ.

Discount Analysis

Discount levels show measurable relationships with sales and
profitability.

These relationships should be treated as associations rather than
evidence that discounts directly cause changes in profit.

Customer & Geography

Sales and profitability vary across regions and customer segments.

Segmenting performance provides additional context beyond overall
business totals.

Time-Based Performance

Monthly sales, profit and late-delivery rates change over the
analyzed period.

Time-based analysis can help identify periods that require
additional operational investigation.

💡 Business Recommendations

Based on the analysis, the project recommends:

Monitor late-delivery rate as a core supply-chain KPI.

Review delivery performance regularly by shipping mode and
geography.

Investigate regions and markets with comparatively higher
late-delivery rates.

Compare shipping-mode performance using both delivery rates and
business volume.

Review product categories with higher delivery risk, particularly
where sales volume is meaningful.

Track sales and profitability separately instead of assuming
high revenue means high profitability.

Monitor discounts together with profitability rather than evaluating
sales growth alone.

Use monthly trends to identify periods requiring additional
operational investigation.

📊 Power BI Dashboard

The Python analysis is structured to support an interactive Power BI
reporting layer.

The proposed dashboard contains four business views:

Executive Overview

Total Sales

Total Profit

Total Orders

Total Customers

Average Order Value

Late-Delivery Rate

Time Trends

Delivery & Logistics

Late-Delivery Rate

Shipping Performance

Region/Market Comparisons

Delivery Trends

Sales & Profitability

Sales

Profit

Profit Margin

Discounts

Categories

Products

Customer Segments

Customer & Geography

Market

Region

Country

Customer Segment

Sales

Profit

Delivery Performance

Note: The supplied notebook prepares the analysis for the Power BI
reporting layer. The project report describes the Power BI dashboard
structure as the next reporting stage.

📁 Project Structure

Supply Chain Project/
│
├── DataCoSupplyChainDataset.csv
├── DineshMohanty_SupplyChainPerformanceAnalytics.ipynb
├── requirements.txt
├── DineshMohanty_ProjectReport.docx
└── README.md

File Description

File                                                    Description

DataCoSupplyChainDataset.csv                          Supply chain transaction dataset

DineshMohanty_SupplyChainPerformanceAnalytics.ipynb   Complete Python analysis notebook

requirements.txt                                      Python dependencies

DineshMohanty_ProjectReport.docx                      Detailed project documentation

▶️ How to Run the Project

1. Clone the repository

git clone <your-github-repository-url>
cd <your-project-folder>

2. Install the required libraries

pip install -r requirements.txt

3. Place the dataset

Make sure:

DataCoSupplyChainDataset.csv

is available in the same working directory as the Jupyter Notebook.

4. Open the notebook

jupyter notebook

Then open:

DineshMohanty_SupplyChainPerformanceAnalytics.ipynb

5. Run the notebook

Run the cells sequentially to reproduce:

Data loading

Data-quality checks

Data preprocessing

Feature engineering

Exploratory analysis

Business analysis

Visualizations

Management summary

⚠️ Limitations

The dataset represents historical transactions from 2015--2018
and may not reflect current operational conditions.

The dataset is at order-item level, so row-based metrics can differ
from order-level metrics.

Late_delivery_risk is an existing source-data field and should not
be interpreted as an independently derived causal outcome.

Correlation or association between discounts and profitability does
not prove that discounts cause changes in profit.

The analysis identifies patterns and areas for investigation;
operational causes require additional business information for
validation.

🚀 Future Scope

Potential extensions include:

Develop an interactive Power BI dashboard with drill-down and
filtering.

Build predictive models for late-delivery risk using information
available before the delivery outcome.

Add transportation and fulfillment cost data.

Incorporate supplier, warehouse, inventory and carrier information.

Create automated KPI monitoring and alerts.

Extend the analysis with customer retention and repeat-purchase
metrics.

📚 Dataset & References

The project report identifies the following sources:

DataCo SMART Supply Chain for Big Data Analysis --- Kaggle

DataCo Global Supply Chain --- Kaggle competition documentation

The dataset used in the notebook is:

DataCoSupplyChainDataset.csv

👤 Author

Dinesh Mohanty
B.Tech -- Computer Science Engineering

Project: Supply Chain Performance & Delivery Optimization Analytics
Program: IBM SkillsBuild Data Analytics with AI
Type: Academic Internship Project

📄 Project Note

This project demonstrates an end-to-end analytics workflow covering
data understanding, preprocessing, exploratory analysis, business
analysis, visualization, KPI development and reporting preparation.

The analysis is intended to provide a structured, data-driven view of
supply chain performance and identify areas that may require further
operational investigation.
