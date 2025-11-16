# FinalProjects1 – Power BI Project

## 📌 Problem Statement

Organizations often struggle to make data-driven decisions due to scattered datasets, inconsistent formats, and lack of real-time reporting.  
The goal of this project is to build an **interactive Power BI dashboard** that consolidates data from multiple sources, cleans and transforms it, and presents meaningful insights across:

- Sales performance  
- Financial metrics  
- Operational KPIs  
- Risk / loan default analytics (if applicable)

This project aims to convert raw data into an efficient, visually appealing analytical solution that helps decision-makers understand trends, detect issues, and identify opportunities for improvement.

---

## 📊 Overview

**FinalProjects1.pbix** is an end-to-end Power BI report that includes:
- A structured data model  
- Cleaned and transformed datasets  
- DAX measures for KPIs  
- Multiple interactive dashboards

---

## 📁 Project Contents

| File | Description |
|------|-------------|
| **FinalProjects1.pbix** | Main Power BI report containing dashboards, visuals, DAX measures, and data model |

---

## 🧱 Data Model

The project is structured following a **Star Schema**, consisting of:

### **Fact Tables**
- Transaction / Sales / Loan data (depending on the dataset)

### **Dimension Tables**
- Date  
- Customer  
- Product  
- Category  
- Region or other categorical fields

### **Relationships**
- 1-to-many relationships between dimensions and facts  
- Active/inactive relationships where required  
- Common key fields:
  - `Date`
  - `CustomerID`
  - `ProductID`
  - `CategoryID`

---

## 🛠 Data Cleaning & Transformation (Power Query)

Transformations done in Power Query include:

- Removing nulls and duplicates  
- Fixing inconsistent date formats (`DD/MM/YYYY`, `MM/DD/YYYY`, `YYYY-MM-DD`)  
- Splitting and merging columns  
- Creating calculated columns  
- Converting data types  
- Cleaning numeric fields  
- Standardizing category names  
- Removing unnecessary columns  
- Merging datasets for dimensional modeling  

---

## 📐 DAX Measures

Some sample DAX measures used in the project:

```DAX
Total Sales = SUM(FactSales[SalesAmount])

Total Quantity = SUM(FactSales[Quantity])

Average Order Value = DIVIDE([Total Sales], [Total Orders])

Default Rate =
DIVIDE(
    CALCULATE(COUNTROWS('loan_default'), 'loan_default'[Default] = TRUE),
    COUNTROWS('loan_default')
)





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
