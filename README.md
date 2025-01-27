# eCommerce Transactions Analysis and Modeling

This repository contains the analysis and modeling solutions for the eCommerce Transactions dataset, consisting of three CSV files: `Customers.csv`, `Products.csv`, and `Transactions.csv`. The goal of this project is to perform exploratory data analysis (EDA), build predictive models, and derive actionable business insights.

## Dataset Overview

The dataset contains the following files:

1. **Customers.csv**:
   - `CustomerID`: Unique identifier for each customer.
   - `CustomerName`: Name of the customer.
   - `Region`: Continent where the customer resides.
   - `SignupDate`: Date when the customer signed up.

2. **Products.csv**:
   - `ProductID`: Unique identifier for each product.
   - `ProductName`: Name of the product.
   - `Category`: Product category.
   - `Price`: Product price in USD.

3. **Transactions.csv**:
   - `TransactionID`: Unique identifier for each transaction.
   - `CustomerID`: ID of the customer who made the transaction.
   - `ProductID`: ID of the product sold.
   - `TransactionDate`: Date of the transaction.
   - `Quantity`: Quantity of the product purchased.
   - `TotalValue`: Total value of the transaction.
   - `Price`: Price of the product sold.

---

## Task 1: Exploratory Data Analysis (EDA) and Business Insights

**Objective**: Perform an exploratory data analysis (EDA) on the provided dataset and derive actionable business insights.

### EDA Steps:
1. Data Cleaning: Handled missing data, duplicates, and merged relevant datasets.
2. Feature Engineering: Derived important metrics such as total spending per customer, frequency of purchases, etc.
3. Visualization: Used plots like histograms, scatter plots, and bar charts to understand distributions and relationships between features.

### Business Insights:
1. **Customer Region Insights**: Customers from certain regions contribute more to sales than others.
2. **Product Category Analysis**: Certain categories show higher transaction volumes and prices.
3. **Purchase Frequency**: High-value customers tend to make frequent purchases.
4. **Average Spending**: The majority of customers tend to have average or low total spending.
5. **Time Trends**: Peak sales occur during specific months of the year.

---

## Task 2: Lookalike Model

**Objective**: Build a lookalike model to recommend similar customers based on their profile and transaction history.

### Lookalike Model:
1. **Input**: Customer information (profile and transaction history).
2. **Output**: Top 3 most similar customers to each of the first 20 customers in `Customers.csv`, along with similarity scores.

### Methodology:
- Customer profiles were merged with transaction data.
- The similarity score between customers was computed using a distance metric based on transaction behavior (e.g., total spending, frequency).
- Recommendations were made by ranking customers based on similarity scores.

---

## Task 3: Customer Segmentation / Clustering

**Objective**: Perform customer segmentation using clustering techniques, based on customer profiles and transaction information.

### Clustering Approach:
1. **Features Used**: Customer profile data (e.g., region) and transaction data (e.g., total spending, transaction frequency).
2. **Clustering Algorithm**: K-Means clustering was applied to segment customers.
3. **Evaluation Metric**: Davies-Bouldin Index (DB Index) was used to evaluate cluster quality.

### Key Findings:
- The number of clusters formed: 4
- **DB Index**: 1.25, indicating a relatively well-separated clustering solution.
- **Cluster Insights**:
  - High-value customers tend to have more frequent transactions.
  - Certain clusters are characterized by low spending and low frequency.
  

---

