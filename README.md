# UPI Transactions Analytics Dashboard

### Dashboard Link

https://app.powerbi.com/groups/c15fac95-bb71-416f-88a5-2647314e67e9/reports/fffe4765-f55b-41c7-9b52-72c057779eec/d57e165cb08332b61808?experience=power-bi&bookmarkGuid=63d958c08a2a50c0c5b8

---

## Problem Statement

The purpose of this Power BI dashboard is to analyze UPI transaction activity and provide useful insights into customer payment behavior, transaction trends, banking activity, and merchant performance.

With the increasing adoption of digital payments, financial institutions and payment service providers need to understand how customers are using UPI across different banks, cities, devices, payment methods, transaction types, and merchant categories. This dashboard helps stakeholders monitor transaction amount, remaining balance movement, and user behavior patterns over time.

The report allows users to filter transactions by customer, banking, payment, and merchant-related attributes, making it easier to identify transaction trends and compare payment activity across different segments.

---

## Dataset Overview

The dataset used for this dashboard contains UPI transaction records with details related to transaction amount, transaction date, customer profile, banking information, device usage, payment method, transaction purpose, and merchant activity.

Key fields used in the report include:

- Transaction Date
- Amount
- Remaining Balance
- Currency
- City
- Gender
- Age Groups
- Device Type
- Transaction Type
- Purpose
- Payment Method
- Merchant Name
- Bank Name Sent
- Bank Name Received

---

## Steps Followed

### Step 1: Data Loading

The UPI Transactions dataset was loaded into Power BI Desktop for data preparation and visualization.

### Step 2: Data Profiling

Power Query Editor was used to inspect the dataset. Column quality, column distribution, and column profile options were enabled to check the structure and quality of the data.

### Step 3: Data Cleaning and Validation

The dataset was reviewed for missing values, duplicate records, incorrect data types, and invalid transaction entries. Date, numeric, and categorical fields were formatted correctly for analysis.

### Step 4: Data Transformation

Transaction date fields were converted into proper date format, while amount and remaining balance fields were formatted as numerical values to support aggregation and trend analysis.

### Step 5: Age Group Creation

A calculated column was created to group customers by age range. This makes it easier to analyze customer behavior by demographic segment.

```DAX
Age Groups =
SWITCH(
    TRUE(),
    'UPI Transactions'[Age] <= 25, "18-25",
    'UPI Transactions'[Age] <= 40, "26-40",
    'UPI Transactions'[Age] <= 60, "41-60",
    "60+"
)
```

### Step 6: Report Design

A custom report theme was applied to improve visual consistency and make the dashboard easier to read.

### Step 7: Interactive Slicers

Slicers were added to allow users to filter the report dynamically. The dashboard includes slicers for:

- Bank Name Sent
- Bank Name Received
- City
- Device Type
- Gender
- Transaction Type
- Purpose
- Payment Method
- Merchant Name
- Age Groups

### Step 8: Trend Visualizations

The first report page focuses on monthly transaction trends and balance movement. The visuals include:

- Remaining Balance by Month using a line chart
- Transaction Amount by Month using a column chart
- Transaction Amount by Month using a line chart
- Remaining Balance by Month using a column chart

### Step 9: Detailed Transaction Table

The second report page contains a detailed table/matrix view for transaction-level analysis. It includes fields such as:

- Amount
- Remaining Balance
- City
- Currency

This page supports deeper exploration of transaction records using the same slicers available on the main report page.

### Step 10: Report Publishing

After building and formatting the report, the dashboard was published to Power BI Service for sharing and online access.

---

## Dashboard Pages

### Page 1: UPI Transaction Trend Analysis
<img width="1114" height="603" alt="Image" src="https://github.com/user-attachments/assets/ed214f06-b3a7-48e7-8501-4432c8bb7691" />

This page presents the main transaction trend analysis. It helps users understand how transaction amount and remaining balance change over time.

The page includes monthly line and column charts for transaction amount and remaining balance, making it easier to compare transaction performance across different months.

### Page 2: Transaction Details
<img width="1099" height="592" alt="Image" src="https://github.com/user-attachments/assets/478cd97d-5c95-41a7-8ab1-dbe475800611" />

This page provides a more detailed tabular view of the transaction data. It allows users to inspect transaction values, remaining balances, city information, and currency details after applying filters.

---

## Dashboard Features

### Transaction Analysis

- Tracks total transaction amount trends over time
- Shows monthly transaction amount movement
- Compares transaction value across months
- Supports filtering by payment and customer attributes

### Balance Analysis

- Analyzes remaining balance trends by month
- Compares balance movement using both line and column visuals
- Helps identify periods with higher or lower remaining balances

### Customer Segmentation

- Allows filtering by gender and age group
- Helps compare UPI usage across customer demographic groups
- Supports city-wise customer behavior analysis

### Payment Behavior Analysis

- Allows filtering by payment method
- Allows filtering by device type
- Allows filtering by transaction type and transaction purpose
- Helps identify customer preferences in UPI payments

### Banking Analysis

- Allows analysis by sending bank
- Allows analysis by receiving bank
- Helps compare bank participation in UPI transactions

### Merchant Analysis

- Allows filtering by merchant name
- Helps review merchant-related transaction activity
- Supports merchant-level transaction exploration

---

## Key Insights

### 1. Transaction Amount Trends

The dashboard helps identify how UPI transaction values change over time. Monthly transaction amount visuals make it easier to observe periods of higher and lower transaction activity.

### 2. Remaining Balance Patterns

The remaining balance visuals show how customer balances vary across months. This can help analysts understand balance movement after UPI transactions.

### 3. Customer Payment Behavior

Using filters such as gender, age group, city, device type, payment method, and transaction type, users can analyze how different customer groups interact with UPI payment services.

### 4. Banking Activity

The sending bank and receiving bank slicers allow users to compare transaction activity across banks and understand how different banks participate in UPI transfers.

### 5. Merchant Activity

The merchant slicer enables merchant-level filtering, making it possible to examine transactions connected to specific merchants.

---

## Business Benefits

This dashboard can help financial institutions, payment service providers, and business analysts to:

- Monitor UPI transaction trends
- Understand customer payment behavior
- Compare transaction activity by bank, city, device, and payment method
- Analyze monthly transaction amount and remaining balance movement
- Identify customer and merchant transaction patterns
- Support data-driven decision-making in digital payment services
- Improve customer experience through better understanding of payment preferences

---

## Tools Used

- Power BI Desktop
- Power Query
- DAX
- Power BI Service
- Data Visualization

---

## Author

**Feranmi Timi-Zacchaeus**  
Data Analyst | Power BI Developer | SQL | Data Visualization
