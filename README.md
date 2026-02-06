# Power BI Assessment Case Study (1 Hour)

## Dataset
**File name:** `sales_AI_Copilot.xlsx`  
**Tool:** Power BI Desktop  
**Time Allocation:** 60 minutes  
**Visualization:** ❌ Not required  
**Submission:** `.pbix` file only

---

## 1. Business Scenario

You are a **Data Analyst** supporting a retail company operating across multiple regions.  
Management requires a clean and reliable **analytical data model** to evaluate:

- Sales performance  
- Profitability  
- Discount impact  
- Customer and product contribution  

Your task is to **prepare, model, and analyze the dataset using Power BI**, focusing on **Power Query and DAX**, without building any visualizations.

---

## 2. Dataset Description

The dataset contains transactional sales data with the following information:

- Order details (Order ID, Order Date, Ship Mode)
- Customer details (Customer ID, Customer Name, Segment, Region, City, State)
- Product details (Category, Sub-Category, Product Name)
- Metrics (Sales, Quantity, Discount, Profit)

---

## 3. Assessment Instructions

- Import the dataset into **Power BI Desktop**
- Perform **data cleaning and transformation** using **Power Query**
- Build a **proper data model**
- Create required **DAX measures**
- No charts, tables, or dashboards are required
- The `.pbix` file must be clean and well-structured

---

## 4. Section A: Data Preparation (Power Query)

### A1. Data Type Validation
Ensure the following columns use the correct data types:

| Column | Data Type |
|------|----------|
| Order Date | Date |
| Sales | Decimal Number |
| Profit | Decimal Number |
| Discount | Decimal Number |
| Quantity | Whole Number |
| Postal Code | Text |

---

### A2. Data Cleaning
1. Identify **null or blank values** in:
   - Sales  
   - Profit  
   - Quantity  
2. Remove rows containing invalid values
3. Trim and clean text columns:
   - Customer Name  
   - Product Name  
   - City  
   - State  

---

### A3. Create New Columns (Power Query)
Create the following calculated columns:

- **Year**  
  Extracted from `Order Date`

- **Month Name**  
  January, February, etc.

- **Profit Category**
  - `Profit > 0` → `Profitable`
  - `Profit ≤ 0` → `Not Profitable`

---

## 5. Section B: Data Modeling

### B1. Date Table
Create a Date Table with the following fields:

- Date
- Year
- Month Number
- Month Name
- Year-Month (YYYY-MM)

Mark it as a **Date Table** and create a relationship to `Order Date`.

---

### B2. Data Model Design
- Apply **star schema principles**
- Fact table: Sales data
- Dimension tables (if separated):
  - Date
  - Customer
  - Product
- Ensure relationships are:
  - One-to-many
  - Single direction

---

## 6. Section C: DAX Measures

Create the following DAX measures:

### Core Measures
- **Total Sales**
- **Total Profit**
- **Total Quantity**

---

### Performance Measures
- **Profit Margin (%)**
  - Total Profit ÷ Total Sales

- **Average Discount**
  - Average of Discount

- **Sales per Order**
  - Total Sales ÷ Distinct Order ID

---

### Time Intelligence
- **Sales by Year**
- **Year-to-Date (YTD) Sales**

---

## 7. Section D: Business Analysis Questions

Using your model and measures, be able to determine:

1. Which **region** generates the highest total sales?
2. Which **product category** contributes the most profit?
3. Does a higher discount always result in lower profit?
4. Which **customer segment** is the most profitable?
5. Which **sub-category** records the highest losses?

*(No written answers required in visuals)*

---

## 8. Section E: Analytical Thinking (Optional)

In **Power BI notes or comments**, briefly describe:

1. One potential **data quality issue**
2. One **business insight** discovered from the data

---

## 9. Deliverables

- One `.pbix` file
- Clean data model
- All required transformations and measures
- No visualization pages

---

## 10. Evaluation Criteria

| Area | Weight |
|----|------|
| Power Query & Data Cleaning | 25% |
| Data Modeling | 20% |
| DAX Measures | 35% |
| Analytical Reasoning | 20% |

---

**End of Case Study**
