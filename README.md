# Retail Performance Overview | Power BI Dashboard

An interactive Power BI dashboard created to analyse retail sales performance across time, product categories, customer segments, and geographical locations.

The project transforms raw retail-order data into a business intelligence report that helps users monitor revenue, profit, sales trends, customer behaviour, and product performance.

## Business Objective

The objective of this project was to create a self-service Power BI dashboard that enables business users to answer questions such as:

- How is retail performance changing over time?
- Which product categories generate the most revenue?
- Which customer segments contribute most to sales and profit?
- How does performance vary by year and state?
- Which areas may require further investigation or operational action?

## Dashboard Overview

The **Retail Performance Overview** dashboard presents key business performance indicators for the period from **2013 to 2017**.

It includes:

- KPI cards for total revenue and profit
- Revenue trend by month
- Customer-segment analysis
- Product-category analysis
- Interactive slicers for year and state
- Visuals that allow users to compare performance across different time periods and locations

## Key Features

- Interactive KPI summary cards
- Monthly revenue trend analysis
- Product-category performance visuals
- Customer-segment comparison
- Year and state slicers for self-service filtering
- Clear executive-style dashboard layout
- Star-schema data-modelling approach using fact and dimension tables

## Data Preparation

The dataset was prepared in Power Query before visualisation.

Key preparation activities included:

- Reviewing and cleaning source data
- Checking column data types
- Creating supporting dimension tables
- Organising data into a star-schema structure
- Preparing fields for time, location, product, and customer analysis
- Creating calculated measures using DAX

## Data Model

The project applies a star-schema design to support reporting performance and analytical clarity.

### Fact Table

- **Orders / Sales Fact Table**  
  Contains transactional information such as order records, sales, revenue, profit, quantity, and discount.

### Dimension Tables

- **Date Dimension**  
  Supports analysis by year, month, and time period.

- **Customer Dimension**  
  Supports customer and customer-segment analysis.

- **Product Dimension**  
  Supports product and category analysis.

- **Geography Dimension**  
  Supports state and location analysis.

> The data model was created as part of an academic business intelligence assignment. Further development would include validating and creating active relationships between the fact table and each dimension table.

## Tools Used

- Power BI Desktop
- Power Query
- DAX
- Data Modelling
- Microsoft Excel / CSV data source
- GitHub

## Dashboard Pages

### 1. Retail Performance Overview

This page provides a high-level summary of retail performance with KPI cards, monthly revenue trends, customer segments, product categories, and interactive year and state filters.

## Example Measures

> Update the measure names below to match your PBIX file exactly.

```DAX
Total Revenue = SUM(Orders[Sales])
```

```DAX
Total Profit = SUM(Orders[Profit])
```

```DAX
Total Orders = DISTINCTCOUNT(Orders[Order ID])
```

```DAX
Average Order Value = DIVIDE([Total Revenue], [Total Orders], 0)
```

## Key Insights

The dashboard enables users to identify:

- Revenue and profit performance over time
- Seasonal patterns in monthly revenue
- High-performing product categories
- Differences in performance across customer segments
- Sales and revenue variation by state
- Areas where further analysis could support business decisions

> Replace this section with 3 to 5 findings from your actual dashboard after reviewing your visuals. Do not include findings that are not supported by the report data.


## How to View the Dashboard

1. Download or clone this repository.

```bash
git clone [https://github.com/](https://github.com/)[your-github-username]/retail-performance-powerbi-dashboard.git
```

2. Open the `.pbix` file using **Power BI Desktop**.

3. Select the report page from the bottom navigation bar.

4. Use the **Year** and **State** slicers to explore changes in retail performance.

> Power BI Desktop is required to open and interact with the `.pbix` report file.

## Repository Structure

```text
retail-performance-powerbi-dashboard/
│
├── data/
│   └── [source-data-file].xlsx
│
├── dashboard/
│   └── Retail Performance Overview.pbix
│
├── screenshots/
│   └── retail-performance-overview.png
│
├── documentation/
│   └── data-model.png
│
└── README.md
```

## Future Improvements

- Create and validate relationships between all fact and dimension tables
- Add more DAX measures, including profit margin and year-over-year growth
- Add drill-through pages for category, product, customer, and location detail
- Include a Top 10 products visual
- Add forecasting for future revenue trends
- Publish the dashboard to Power BI Service for browser-based viewing

## Disclaimer

This dashboard was created for educational and portfolio purposes using an academic retail dataset.
