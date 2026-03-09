# 📊 Amazon Sales Data Analysis – Power BI Dashboard

---

## 📌 Overview
This project presents an interactive **Amazon Sales Dashboard** built using **Microsoft Power BI**.  

The dashboard transforms raw sales data into meaningful business insights by analyzing sales performance, order status, regional distribution, product categories, and fulfilment types.

The goal of this project is to support data-driven decision-making using visualization and DAX calculations.

---

## 🎯 Objective

- Analyze overall sales performance  
- Track total orders and quantity sold  
- Evaluate order status distribution  
- Identify top-performing product categories  
- Compare B2B and B2C sales  
- Analyze state-wise revenue performance  
- Monitor monthly sales trends  

---

## 🛠 Tools & Technologies Used

- Microsoft Power BI Desktop  
- Power Query (Data Cleaning & Transformation)  
- DAX (Data Analysis Expressions)  
- Data Modeling  
- Interactive Visualizations  

---

## 📂 Dataset Information

The dataset includes:

- Order ID  
- Date  
- Order Status  
- Product Category  
- SKU  
- Quantity (Qty)  
- Sales Amount  
- Fulfilment Type  
- Sales Channel  
- Ship City  
- Ship State  
- Courier Status  
- B2B Indicator  

---

## 🔧 Data Preparation Steps

- Imported dataset into Power BI  
- Cleaned data using Power Query  
- Removed blank and unnecessary columns  
- Corrected data types (Date, Amount, Qty)  
- Loaded cleaned data into the data model  

---

## 📊 DAX Measures Created

```DAX
Total Sales = SUM('Amazon'[Amount])

Total Orders = DISTINCTCOUNT('Amazon'[Order ID])

Total Quantity = SUM('Amazon'[Qty])

Cancelled Orders =
CALCULATE(
    COUNT('Amazon'[Order ID]),
    'Amazon'[Status] = "Cancelled"
)
****
