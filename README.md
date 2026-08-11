# 📊 Flipkart E-Commerce Sales, Customers & Returns Analysis #
 📝 Project Overview

Flipkart E-Commerce Sales, Customers & Returns Analysis is an end-to-end Data Analytics and Business Intelligence mini project developed using Excel, Power Query, Power BI, and DAX.

The project analyses e-commerce transaction data across orders, customers, products, and returns to evaluate sales performance, customer behaviour, product contribution, profitability, geographical performance, and return patterns.

The project follows a structured analytical workflow:

* Data Collection → Data Cleaning → Data Transformation → Data Modelling → DAX Development → Dashboard Design → Business Analysis

# 🎯 Problem Statement

Analyse retail and e-commerce data to identify sales trends, customer behaviour, product performance, profitability, and return patterns by cleaning and integrating multiple datasets to generate actionable business insights.

# 🎯 Project Objectives

* Analyse overall sales, profit, orders, and customer performance.

* Evaluate product, category, sub-category, and brand performance.

* Understand customer segment and geographical purchasing behaviour.

* Analyse sales trends and profitability over time.

* Identify return patterns, return reasons, and refund exposure.

* Evaluate the financial impact of returns on profitability.

# 🗃️ Dataset Overview

The project uses multiple interconnected datasets representing different aspects of the e-commerce business.

# 📌 01. Orders Dataset 

Contains transaction-level information used for sales, order, delivery, and profitability analysis.

Key Fields:

* Order ID
* Order Date
* Customer ID
* Product ID
* Sales
* Quantity
* Profit
* Delivery Days
* Customer Segment
* State
* City

# 📌 02. Products Dataset

Contains product master information used for product-level analysis.

Key Fields:

* Product ID
* Product Name
* Category
* Sub-Category
* Brand

# 📌 03. Customers Dataset

Contains customer information used for customer and geographical analysis.

Key Fields:

* Customer ID
* Customer Name
* Customer Segment
* State
* City

 # 📌 04. Returns Dataset

Contains information related to returned orders and refunds.

Key Fields:

* Order ID
* Return Status
* Return Reason
* Refund Amount

# 📌 05. Date Table

A dedicated calendar table was created in Power BI to support time-based analysis.

Key Fields:

* Date
* Day
* Month
* Month Name
* Quarter
* Year

# 🧹 Data Cleaning & Preparation

Data preparation was performed using Excel and Power Query before loading the data into Power BI.

# Key Data Quality Activities
* Removed duplicate records.
* Handled missing and null values.
* Standardised date formats.
* Cleaned inconsistent text and categorical values.
* Corrected State, City, Category, and Brand inconsistencies.
* Validated Customer ID, Product ID, and Order ID fields.
* Handled missing Profit, Delivery Days, Customer ID, and Refund Amount values.
* Standardised column data types.
* Prepared datasets for integration and modelling.

# 🔄 Data Transformation

Power Query was used to transform the raw datasets into analysis-ready tables.

* Transformation Process

Raw CSV Files

↓

Data Profiling & Quality Checks

↓

Duplicate & Null Handling

↓

Data Type Standardisation

↓

Text & Category Standardisation

↓

Data Validation

↓

Derived Fields & Calculations

↓

Final Clean Tables

↓

Power BI Data Model

# 🧩 Data Model

A structured relational data model was implemented in Power BI to ensure consistent filtering, aggregation, and cross-table analysis.

 Model Architecture
 
                    ┌───────────────┐
                    │   Customers   │
                    
                    └───────┬───────┘
                    
                            │
                            │
                    ┌───────▼───────┐
                    
                    │    Orders     │
                    └───┬───────┬───┘
                        │       │
                        
                        │       │
                ┌───────▼───┐ ┌─▼──────────┐
                
                │ Products  │ │  Returns   │
                └───────────┘ └────────────┘
                        │
                        
                  ┌─────▼─────┐
                  │    Date   │
                  └───────────┘

# 📐 DAX Measures & Calculations

DAX was used to develop dynamic measures and calculated logic required for business analysis.

# 💰 Sales & Performance Measures
* Total Sales
* Total Profit
* Order Count
* Customer Count
* Average Order Value
* Profit Margin %
# 🔄 Return & Financial Measures
* Return Count
* Return Rate %
* Total Refund
* Average Refund Amount
* Profit After Refund
* Loss-Making Orders

The measures are designed to respond dynamically to Power BI slicers, filters, and visual interactions.

# ⚙️ Modelling Approach

The data model was designed to support:

* Consistent filtering across dashboards.
* Cross-table analytical relationships.
* Time-based analysis.
* Customer and product segmentation.
* Category and sub-category analysis.
* Geographical analysis.
* Return and refund analysis.
* Dynamic DAX calculations.
* Interactive Power BI reporting.

# 📸 Data Model Preview

The Power BI model establishes relationships between the Orders, Customers, Products, Returns, and Date tables.

<img width="655" height="341" alt="image" src="https://github.com/user-attachments/assets/afbb8dd1-aa1a-4fdf-a2ae-26495f5c97dd" />

# 📸 Dashboard Preview

📊 Dashboard 01 — Sales & Customer Analysis

<img width="629" height="342" alt="image" src="https://github.com/user-attachments/assets/47046db5-e353-48ba-85be-c979211a8ab6" />

The first dashboard provides a consolidated view of sales performance, product contribution, customer performance, brand performance, and geographical sales distribution.



🔹 KPI Layer
* Total Sales
* Total Profit
* Total Orders
* Customers Count
* Average Order Value
* Profit Margin %
🔹 Product Analysis

Top 10 Products by Sales

* Identifies the products contributing the highest sales and supports product-level performance evaluation.

🔹 Category Analysis

Category vs Sales & Profit

* Compares revenue and profit across categories to evaluate both sales contribution and profitability.

🔹 Geographical Analysis

Sales by State

* Provides state-level sales distribution to identify geographical performance differences.

🔹 Time Analysis

Monthly Sales Trend

* Tracks monthly sales performance and supports period-based performance evaluation.

🔹 Customer Analysis

Customer Segment Performance

* Compares performance across customer segments.

🔹 Brand Analysis

Brand Performance by Sales

* Uses a treemap to compare brand-level sales contribution.

# 📊 Dashboard 02 — Profitability & Returns Analysis

<img width="632" height="344" alt="image" src="https://github.com/user-attachments/assets/de1e424f-7e0d-462e-a750-944738fd464d" />

The second dashboard focuses on returns, refunds, profitability, loss-making transactions, and return-related financial exposure.

🔹 KPI Layer
* Return Count
* Return Rate %
* Total Refund
* Average Refund
* Profit After Refund
* Loss-Making Orders
🔹 Return Analysis

Return Reason Distribution

* Shows the distribution of customer return reasons.

Return Analysis by Category

* Compares return volumes across product categories.

Top Returned Products

* Identifies products with comparatively high return activity.

🔹 Financial Analysis

Refund vs Profit by Category

* Compares refund exposure against category-level profitability.

🔹 Geographical Analysis

State-wise Return Activity & Refund Impact

* Evaluates geographical variation in return activity and refund exposure.

🔹 Detailed Analysis

Detailed Transaction Table

* Provides transaction-level information for deeper investigation across orders, customers, products, and returns.

# 🎛️ Dashboard Functionality

The Power BI report provides interactive functionality through:

* Slicers
* Cross-filtering
* Drill-down analysis
* KPI cards
* Dynamic DAX measures
* Interactive charts
* Geographical visualisation
* Product-level analysis
* Transaction-level filtering

The dashboards allow users to move from overall KPI-level analysis to detailed business dimensions without changing the underlying dataset.


# 📁 Project Structure

Flipkart-Ecommerce-Analytics/

│

├── 📂 Data/


│   ├── Orders.csv


│   ├── Products.csv


│   ├── Customers.csv


│   └── Returns.csv

│

├── 📂 PowerBI/

│   └── Flipkart_E-commerce_Analysis_Dashboards.pbix

│

├── 📂 Documentation/

│   └── Project_Documentation.pdf

│

├── 📂 Dashboard/

│   └── Dashboard_Screenshots/

│

└── 📄 README.md

# 🛠️ Tools & Technologies

 Technology	Purpose

📗 Microsoft Excel	Data inspection, validation, and preliminary analysis

🔄 Power Query	Data cleaning, transformation, and integration

📊 Power BI	Data modelling, visualization, and dashboard development

📐 DAX	Measures, KPIs, and analytical calculations

🐙 GitHub	Project versioning and documentation

# 🧠 Technical Skills Demonstrated
* Data Cleaning
* Data Transformation
* Data Integration
* Data Modelling
* Data Validation
* Exploratory Data Analysis
* DAX
* Power BI
* Power Query
* Excel
* KPI Development
* Sales Analysis
* Customer Analysis
* Product Analysis
* Profitability Analysis
* Return Analysis
* Refund Analysis
* Geographical Analysis
* Interactive Dashboard Development

# 📈 Dashboard Insights

The dashboards provide the following analytical observations and decision-support areas:

* Sales concentration: The Top 10 Products visual identifies the products contributing most strongly to overall sales.

* Revenue vs profitability: Category-level Sales and Profit comparison highlights whether high-revenue categories also deliver strong  profitability.

* Regional performance: State-level sales and return maps help identify geographical differences in business performance.

* Customer contribution: Customer Segment Performance enables comparison of revenue contribution across different customer groups.

* Return concentration: Category and product return analysis helps identify areas with comparatively higher return activity.

* Financial exposure: Refund vs Profit analysis highlights categories where returns may place greater pressure on profitability.


# 💼 Business Impact

• Improves visibility into overall sales and profitability performance.

• Helps identify high-performing products, categories, brands, and customer segments.

• Supports evaluation of state-wise sales and return performance.

• Helps monitor refund exposure and return-related financial impact.

• Enables identification of loss-making and high-return areas requiring investigation.

• Provides management with an interactive analytical platform for data-driven decision-making.

# 💡 Business Recommendations

• Prioritise high-performing products and categories while reviewing low-profit product groups.

• Investigate products and categories with consistently high return volumes.

• Review return reasons to identify potential product, packaging, delivery, or expectation-related issues.

• Monitor refund exposure alongside profitability rather than evaluating sales independently.

• Develop targeted strategies for high-value customer segments and strong-performing regions.

• Use the Power BI dashboard regularly to monitor changes in sales, profitability, and returns.


# 📦 Project Deliverables

📊 Power BI Report

* Interactive Power BI dashboards covering sales, customers, products, profitability, returns, refunds, and geographical performance.

🗂️ Cleaned Data

* Prepared and transformed datasets used for analytical modelling.

🔗 Data Model

* Integrated Power BI model connecting transactional, master, return, and date information.

📑 Documentation

* Project documentation covering requirements, data preparation, modelling, analysis, and dashboard development.

📖 GitHub Repository

* Centralised repository containing project files, datasets, dashboard screenshots, documentation, and README.

# 📌 Project Information

Project Title: Flipkart E-Commerce Sales, Customers & Returns Analysis

Project Type: Data Analytics / Business Intelligence Mini Project

Domain: E-Commerce & Retail Analytics

Analysis Period: 2025

Primary Tool: Microsoft Power BI

Supporting Tools: Microsoft Excel, Power Query & DAX

# 🏁 Conclusion

The 2025 Flipkart E-Commerce analysis consolidates sales, customer, product, profitability, and return data into an interactive Power BI reporting solution. The report enables dynamic evaluation of sales performance, customer contribution, product performance, and return-related financial impact through KPI-driven dashboards and detailed transaction analysis.

# 👨‍💻 About the Author

Sri Hari

Aspiring Data Analyst | Power BI | Excel | SQL | Data Visualization

Interested in transforming raw datasets into structured analytical solutions using data cleaning, data modelling, DAX, visualization, and business intelligence techniques.

This project represents practical application of Power BI and Data Analytics concepts to an E-Commerce business use case.

Core Areas:

Data Analytics · Power BI · Excel · Power Query · DAX · Data Modelling · Data Visualization · Business Intelligence







