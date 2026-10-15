# Power BI — 20 Beginner Practice Questions

A beginner-friendly Power BI project for practising data cleaning, basic calculations, visualisations, filtering, introductory DAX, and dashboard development using a raw sales dataset.

## Project Structure

```text
power-bi-20-practice-questions/
├── dataset/
│   └── sales-raw-data.csv
└── README.md
```

## Dataset Overview

The project uses `dataset/sales-raw-data.csv`, a sales dataset with the following columns:

| Column          | Description              |
| --------------- | ------------------------ |
| `OrderID`       | Unique order number      |
| `OrderDate`     | Date of order            |
| `CustomerName`  | Customer name            |
| `City`          | Customer city            |
| `Category`      | Product category         |
| `Product`       | Product name             |
| `Quantity`      | Number of units sold     |
| `UnitPrice`     | Price per unit           |
| `Sales`         | Total sales              |
| `Profit`        | Profit generated         |
| `PaymentMethod` | Payment method           |
| `Salesperson`   | Person who made the sale |

The dataset is intentionally raw and includes missing values and duplicate records for data-cleaning practice. Inspect the data before deciding how to handle these issues.

## Practice Questions

### Level 1 — Power BI Basics

- [ ] **1. Import the data:** Load the CSV into Power BI Desktop, inspect its columns and data types, and identify any incorrect data types.
- [ ] **2. Check for missing values:** Find columns containing null values, count the missing values, and decide how to handle them.
- [ ] **3. Remove duplicate orders:** Check for duplicate records and duplicate `OrderID` values. Investigate them and remove duplicates where appropriate.
- [ ] **4. Total sales card:** Create a Card visual showing total sales. What is the total revenue?
- [ ] **5. Total profit card:** Create a Card visual showing total profit.
- [ ] **6. Total quantity card:** Create a Card visual showing the total number of units sold.
- [ ] **7. Total orders card:** Create a Card visual showing the number of unique orders using `OrderID`.
- [ ] **8. Average order value:** Calculate the average amount spent per order.

### Level 2 — Basic Visualisations

- [ ] **9. Sales by category:** Create a column chart of sales by `Category`. Which category generates the highest sales?
- [ ] **10. Profit by category:** Create a bar chart of profit by `Category`. Which category is the most profitable?
- [ ] **11. Sales by city:** Create a chart of total sales by `City`. Which city generates the most revenue?
- [ ] **12. Sales by payment method:** Create a donut chart showing sales distribution by `PaymentMethod`. Analyse either order count or total sales, and identify the most popular payment method.
- [ ] **13. Top 5 products by sales:** Use a visual and a Top N filter to display the five products with the highest sales.
- [ ] **14. Salesperson performance:** Create a table with `Salesperson`, total sales, total profit, and number of orders. Which salesperson generated the highest revenue?

### Level 3 — Dates and Filtering

- [ ] **15. Monthly sales trend:** Create a line chart with `OrderDate` on the X-axis and sales on the Y-axis. How do sales change month to month?
- [ ] **16. Monthly profit trend:** Create a line chart showing profit by month. Which month generated the highest profit?
- [ ] **17. Date slicer:** Add an `OrderDate` slicer that allows users to select a date range. Check how total sales, profit, and orders respond.
- [ ] **18. Category slicer:** Add a `Category` slicer and verify that the report visuals respond to the selected category.

### Level 4 — Beginner DAX

- [ ] **19. Profit margin measure:** Create a DAX measure for profit margin using total profit divided by total sales. Use `DIVIDE` to handle division safely, then format the measure as a percentage.

Example measure pattern:

```dax
Profit Margin =
DIVIDE(
    [Total Profit],
    [Total Sales]
)
```

This assumes you have already created `[Total Profit]` and `[Total Sales]` measures.

### Final Challenge — Build a Sales Dashboard

- [ ] **20. Build a one-page sales dashboard** that brings together the measures, visuals, and filters from the previous exercises.

#### KPI Cards

- Total Sales
- Total Profit
- Total Orders
- Total Quantity
- Profit Margin

#### Charts

- Sales by Category
- Profit by Category
- Sales by City
- Monthly Sales Trend
- Top 5 Products by Sales

#### Slicers

- Order Date
- Category
- City
- Salesperson
- Payment Method

#### Questions to Answer with the Dashboard

1. What is the company's total revenue?
2. What is the total profit?
3. What is the profit margin?
4. Which category generates the most revenue?
5. Which category generates the most profit?
6. Which city performs best?
7. Who is the top salesperson?
8. What are the top five products by sales?
9. Which month had the highest sales?
10. Which payment method is most popular?

## Suggested Workflow

Work through the questions in order rather than starting with the final dashboard:

1. **Questions 1–3:** Importing and cleaning data
2. **Questions 4–8:** Cards and basic calculations
3. **Questions 9–14:** Visualisations and comparisons
4. **Questions 15–18:** Date analysis and interactive slicers
5. **Question 19:** Introductory DAX
6. **Question 20:** Combine your work into a dashboard

## Skills Practised

- Importing CSV data into Power BI
- Checking column data types
- Finding and handling missing values
- Identifying and removing duplicates
- Creating Card visuals and basic aggregations
- Building bar, column, donut, line, and table visuals
- Using Top N filters and sorting
- Analysing date hierarchies and monthly trends
- Adding interactive slicers
- Writing a basic DAX measure
- Designing a one-page dashboard and communicating findings

## Tools

- Power BI Desktop
- CSV dataset included in the `dataset/` folder

## Notes

- Keep an untouched copy of the raw CSV so you can compare it with your cleaned data.
- Make and document your own decisions about missing values and duplicates.
- Validate your measures and visuals after applying filters.
- This is a practice project; the findings should come from your analysis of the dataset, not from assumed results.
