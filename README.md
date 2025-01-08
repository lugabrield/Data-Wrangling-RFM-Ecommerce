# Data Wrangling and RFM Analysis for E-Commerce

This project is focused on preparing and analyzing a dataset for an e-commerce company, aiming to calculate the **RFM (Recency, Frequency, Monetary)** metrics for its customers. The dataset provided contains transaction records for various products, and the objective is to clean, process, and generate insights based on customer behavior.

## Overview

In this challenge, the following key steps were carried out:

- **Data Cleaning & Wrangling**: The dataset was pre-processed by handling missing values, removing duplicates, correcting data types, and removing outliers.
- **Data Analysis**: Key metrics such as Recency, Frequency, and Monetary (RFM) were calculated to segment the customers based on their purchasing behaviors.
- **Visualization**: Various insights were visualized through bar plots and line charts, including sales trends by country and top-selling products.

### RFM Metrics

- **Recency (R)**: The time since the customer's last purchase, in days.
- **Frequency (F)**: The total number of purchases made by the customer.
- **Monetary (M)**: The total amount spent by the customer.

## Steps Involved

### 1. Data Cleaning
- Removed rows with missing or invalid data (such as negative or zero values for prices and quantities).
- Dropped duplicates to ensure unique transaction entries.
- Converted data types for `CustomerID` and `InvoiceDate` to the correct formats.

### 2. Outlier Removal
- Identified and removed extreme outliers in quantities and unit prices that were deemed unrealistic (e.g., quantities above 10,000 or prices above 5,000).

### 3. Feature Engineering
- Calculated the **Total Purchase Value** for each transaction by multiplying `Quantity` and `UnitPrice`.
- Calculated **Recency**, **Frequency**, and **Monetary** metrics for each customer.
- Computed the **Average Ticket** (Monetary / Frequency) for each customer.

### 4. Data Visualization
- Created visualizations to identify:
  - **Top 10 Countries** with the highest sales.
  - **Top 10 Products** with the highest sales volume.
  - **Sales trends over time**.
  - **Sales by country** for the top 10 performing countries.

## Files

- **`data.csv`**: The raw dataset containing transaction records.
- **`RID166710_Desafio05.ipynb`**: The Jupyter notebook containing the complete analysis and code.

## Libraries Used
- `pandas`: For data manipulation and analysis.
- `matplotlib` & `seaborn`: For data visualization.

## Getting Started

To get started with this project, follow these steps:

1. Clone this repository to your local machine:

   ```bash
   git clone https://github.com/lugabrield/Data-Wrangling-RFM-Ecommerce.git

### 2. Outlier Removal
Outliers were identified and removed to ensure the analysis only included realistic data. The following criteria were applied:
- **Quantity**: Any purchase with a quantity greater than 10,000 was considered an outlier and removed.
- **Unit Price**: Any product with a price greater than 5,000 was also flagged as an outlier and removed.

This step ensured that extreme values did not distort the analysis.

### 3. Feature Engineering
In this step, new features were created to better analyze customer behavior:
- **Total Purchase Value**: A new column called `Total` was created by multiplying the `Quantity` by the `UnitPrice` for each transaction.
- **RFM Metrics**: The following metrics were calculated:
  - **Recency**: The number of days since the customer’s most recent purchase.
  - **Frequency**: The number of unique purchases made by the customer.
  - **Monetary**: The total value of all purchases made by the customer.
- **Average Ticket**: The `AverageTicket` column was created by dividing the `Monetary` value by `Frequency`.

These new features were essential for customer segmentation based on purchasing patterns.

### 4. Data Visualization
Several insightful visualizations were generated:
- **Top 10 Countries with the Highest Sales**: A bar chart was created showing the top 10 countries where the most sales occurred, based on total sales value.
- **Top 10 Products with the Highest Sales Volume**: Another bar chart was plotted for the top 10 products based on the quantity sold.
- **Sales Trends Over Time**: A bar chart was generated to show the total sales per month, allowing us to observe trends in the data.
- **Sales by Country for the Top 10 Countries**: A line chart was plotted to show the total sales per month for the top 10 countries, offering a comparison of sales performance over time for these regions.

These visualizations provided valuable insights into the business performance by product, country, and time period.

## Conclusion

This project demonstrates the importance of data cleaning, feature engineering, and data visualization in transforming raw transactional data into actionable insights. By calculating RFM metrics, we were able to segment customers based on their purchasing behavior, which is critical for any e-commerce business aiming to optimize marketing strategies and customer retention.

The visualizations created help the business understand key trends, including the countries and products driving the most sales. The steps taken in this analysis are essential in the data science pipeline and can serve as a foundation for further analysis and modeling.
