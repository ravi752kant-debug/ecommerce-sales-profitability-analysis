# E-commerce Sales & Profitability Analysis 

## Project Overview

This is my **first data analysis portfolio project**, focused on analyzing an e-commerce dataset to understand sales performance, profitability, product and category performance, regional trends, discount behavior, payment methods, and low-margin orders.

The goal of this project was to practice the complete **Exploratory Data Analysis (EDA) workflow** and turn raw business data into meaningful insights and actionable recommendations.

---

## Project Objectives

The analysis aims to answer important business questions such as:

- How do sales and profit change over time?
- Which product categories generate the most sales and profit?
- Which regions perform best?
- Does discount level have an association with profit margin?
- Which products generate high sales and profit?
- How does performance vary across payment methods?
- Are there low-margin orders that should be investigated?
- What business recommendations can be made from the analysis?

##Dataset

The dataset contains:

- **5,000 orders**
- **14 original columns**
- **10 product categories**
- **4 regions**
- **5 payment methods**
- Analysis period: **October 4, 2023 – October 3, 2025**

The dataset contains information related to:

- Order details
- Customers
- Locations
- Categories and products
- Quantity
- Unit price
- Discount
- Sales
- Profit
- Payment method

---

## Technologies & Libraries

- **Python**
- **Pandas** — data manipulation and analysis
- **NumPy** — numerical operations
- **Matplotlib** — data visualization
- **Seaborn** — statistical visualization
- **Jupyter Notebook** — analysis environment

---

## Analysis Workflow

The project follows a structured EDA workflow:

### 1. Data Loading & Understanding

- Loaded the dataset using Pandas
- Checked dataset shape
- Inspected columns and data types
- Reviewed the structure of the dataset
- Examined categorical and numerical variables

### 2. Data Quality Investigation

Checked the dataset for:

- Missing values
- Duplicate records
- Invalid values
- Negative sales, quantity, and profit
- Invalid discount values
- Data-type issues

The `Order Date` column was converted into a proper datetime format for time-based analysis.

### 3. Data Preparation

Created additional features to support the analysis:

- **Month** — for monthly sales and profit analysis
- **Profit Margin %** — calculated as:

`Profit Margin % = Profit / Sales × 100`

### 4. Exploratory Data Analysis

The analysis covers:

- Monthly sales & profit trends
- Category performance
- Regional performance
- Product performance
- Discount vs. profit margin
- Payment method behavior
- Low-margin orders and statistical outliers

---

## Key Findings

### Overall Performance

The dataset contains **5,000 orders** with approximately:

- **₹533.67M** total sales
- **₹79.71M** total profit
- **₹106,733** average order value
- **14.94%** overall profit margin

---

### Monthly Sales & Profit

The analysis identified noticeable monthly variation in sales and profit.

Important high-sales periods include:

- **November**
- **April–May**

Peak monthly sales exceeded approximately **₹25M**.

These periods may be useful for inventory, campaign, and operational planning.

> Note: The dataset alone cannot establish whether these peaks were caused by holidays, promotions, marketing campaigns, or other factors.

---

### Category Performance

There is an important difference between sales leadership and profit leadership.

- **Home Decor** generated the highest total sales at approximately **₹57.23M**.
- **Furniture** generated the highest total profit at approximately **₹8.69M**.
- **Groceries** recorded the lowest total sales at approximately **₹47.88M**.
- **Beauty** had the lowest profit margin at approximately **14.20%**.
- **Electronics** had the highest average order value among categories.

This demonstrates why both **revenue and profitability** should be considered when evaluating category performance.

---

### 🌎 Regional Performance

Regional performance was not identical.

| Region |    Sales |  Profit |
| ------ | -------: | ------: |
| North  | ₹143.58M | ₹21.34M |
| East   | ₹135.81M | ₹20.53M |
| West   | ₹131.05M | ₹19.58M |
| South  | ₹123.23M | ₹18.25M |

**North** was the strongest region in terms of both total sales and total profit.

The analysis also identified differences between categories within regions, providing opportunities for more targeted regional analysis.

---

### Discount & Profit Margin

The analysis examined whether discount percentage was associated with profit margin.

The calculated correlation was approximately:

**-0.003**

This indicates an **almost zero linear relationship** between discount percentage and profit margin in this dataset.

Interestingly, low-margin orders were also found at **0% discount**.

This suggests that discount percentage alone does not explain profitability differences. Product pricing, product costs, supplier costs, category economics, and other factors should be investigated.

> Correlation does not prove causation.

---

### Product Performance

Among the top products by sales:

- **Headphones Accusantium** generated approximately **₹857K sales** and **₹142K profit**.
- **Laptop Similique** and **Accessories Repellendus** were also strong profit contributors.
- **Lamp Veritatis** generated approximately **₹653K sales** but only **₹63K profit**, making it a useful candidate for pricing or cost-structure investigation.

Some products have very small order counts, so their performance should be interpreted cautiously.

---

### Payment Method Analysis

Payment activity was relatively evenly distributed across the five payment methods.

Order volumes ranged from approximately **988 to 1,010 orders**.

**Net Banking** had the highest order count and average order value.

However, the differences between payment methods were relatively modest, suggesting that payment method was not a major performance driver based on this analysis alone.

---

### Low-Margin Orders & Outlier Analysis

The project used an **IQR-based statistical outlier check** to identify extreme profit-margin values.

It also created a separate **bottom 5% profit-margin segment** to identify potentially risky low-margin orders.

This distinction is important because a business-risk order does not necessarily have to be a statistical outlier.

---

## Business Recommendations

Based on the analysis:

### 1. Plan Around High-Demand Periods

Use the recurring November and April–May sales peaks to improve:

- Inventory planning
- Campaign preparation
- Operational capacity

Additional marketing and promotional data should be analyzed before assigning a specific cause to these peaks.

### 2. Focus on Profitable Categories

Maintain strong attention on:

- **Furniture** for profitability
- **Home Decor** for sales performance

Both revenue and profit should be considered when making category-level decisions.

### 3. Investigate Regional Opportunities

Further investigate:

- Lower-performing categories in the South
- Strong Kitchen and Furniture performance in the West
- Category-level opportunities within each region

### 4. Investigate Margin Drivers Beyond Discounts

Since discount percentage showed almost no linear relationship with profit margin, further analysis should examine:

- Product pricing
- Product costs
- Supplier costs
- Category economics
- Promotional activity

### 5. Review Low-Margin Products

Products with high sales but comparatively weak profitability should be reviewed before increasing their promotional exposure.

**Lamp Veritatis** is one example identified by this analysis.

---

## Skills Demonstrated

This project demonstrates my ability to:

- Load and inspect datasets using Python
- Perform data quality checks
- Identify missing, duplicate, and invalid data
- Work with Pandas DataFrames
- Convert and work with datetime data
- Create calculated features
- Perform groupby-based analysis
- Calculate business KPIs
- Analyze sales and profitability
- Perform exploratory data analysis
- Create meaningful visualizations
- Compare categories and regions
- Analyze relationships between variables
- Identify low-margin business segments
- Extract business insights from data
- Convert analysis findings into recommendations
- Communicate analytical results clearly


## Limitations

This analysis is based only on historical order-level data.

The dataset does not contain several potentially important business variables, including:

- Product and supplier costs
- Marketing spend
- Promotional campaign information
- Inventory levels
- Customer acquisition cost
- Customer retention
- Customer lifetime value

Therefore, the findings should be interpreted as **patterns and areas for further investigation rather than causal conclusions**.

---

## Future Improvements

With additional business data, this project could be extended with:

- Customer segmentation
- Customer retention analysis
- Repeat-purchase analysis
- Customer Lifetime Value (CLV)
- Marketing campaign analysis
- Inventory and stock-out analysis
- Product-level cost analysis
- Pricing and discount elasticity
- Sales forecasting
- Machine Learning-based prediction

---

## About This Project

This is my **first portfolio project** as I build my skills in data analysis and work toward becoming an **AI Engineer**.

The purpose of this project is to demonstrate practical ability to take a dataset, investigate its quality, perform exploratory analysis, visualize patterns, identify business insights, and communicate findings clearly.

More projects will build on these skills with **Machine Learning and AI Engineering**.

---

## Project Status

**Completed — Beginner Data Analysis / EDA Portfolio Project**
