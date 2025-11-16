# FinalProjects1 – Power BI Project

## 📊 Overview
**FinalProjects1.pbix** is an end-to-end Power BI project designed to analyze key business metrics, visualize trends, and support data-driven decision-making.

---

## 📁 Project Contents
| File | Description |
|------|-------------|
| **FinalProjects1.pbix** | Main Power BI report file containing dashboards, measures, visuals, and data model |

---

## 🧱 Data Model
This project contains a structured Power BI data model including:

- **Fact tables** (sales, transactions, or project-specific data)
- **Dimension tables** (date, customer, product, category, etc.)
- **Star-schema relationships** using:
  - 1-to-many relationships
  - Active/inactive relationships where required  
- Common key fields used for relationships:
  - `Date`
  - `CustomerID`
  - `ProductID`
  - `CategoryID`

---

## 🛠 Transformations (Power Query)
Data cleaning and transformation steps include:

- Removing duplicates and nulls  
- Standardizing date formats (`DD/MM/YYYY`, `MM/DD/YYYY`, `YYYY-MM-DD`)  
- Creating computed/conditional columns  
- Merging queries to improve the model  
- Cleaning numeric fields (amount, cost, quantity)

---

## 📐 DAX Measures Used
Some example DAX measures used in this project:

```DAX
Total Sales = SUM(FactSales[SalesAmount])

Total Quantity = SUM(FactSales[Quantity])

Average Order Value = DIVIDE([Total Sales], [Total Orders])

Default Rate =
DIVIDE(
    CALCULATE(COUNTROWS('loan_default'), 'loan_default'[Default] = TRUE),
    COUNTROWS('loan_default')
)

```

## 📈 Dashboards / Visuals Included

### Sales Dashboard

-   Total Sales
-   Sales by Category / Region
-   Monthly Trend
-   Top Customers & Products

### Financial Dashboard

-   Revenue vs Expenses
-   Profitability KPIs

### Operational Dashboard

-   Order volumes
-   Delivery metrics

### Risk / Default Dashboard

-   Default rate by year
-   Default by employment type

## ▶️ How to Run the Project

1.  Install **Power BI Desktop**
2.  Open **FinalProjects1.pbix**
3.  Update data source credentials
4.  Refresh the report

## 📌 Requirements

-   Power BI Desktop
-   Data source access

## 🤝 Contribution

You can enhance the model, add visuals, or build new dashboards.

## 📧 Support

For help or improvements, ask anytime!
