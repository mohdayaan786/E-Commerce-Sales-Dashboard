# E-Commerce Sales Dashboard

An interactive **Power BI dashboard** built using **Orders.csv** and **Details.csv** to analyze e-commerce performance across states, categories, customers, payment modes, and time periods.

---

## 📊 Dashboard Preview

### Main Dashboard


<img width="1464" height="799" alt="image" src="https://github.com/user-attachments/assets/81dab12c-e9d4-4dae-944c-83a3cdb1741a" />


### Details.csv Sample

<img width="805" height="689" alt="image" src="https://github.com/user-attachments/assets/d21fe2e7-9783-4e52-aec9-569c743b29b0" />


### Orders.csv Sample

<img width="824" height="696" alt="image" src="https://github.com/user-attachments/assets/8b35f6a0-6858-44b0-a63d-77fde22c7383" />


---

## 📦 Project Overview

This Power BI project visualizes and analyzes e-commerce sales data. It combines order-level information (Orders.csv) with product and transaction-level metrics (Details.csv) to derive meaningful insights such as:

* Total sales amount
* Total profit
* Total quantity sold
* Average order value (AOV)
* Profit trends by month
* State-wise contribution
* Customer performance
* Category & sub-category breakdowns
* Payment mode distributions

The dashboard supports interactive filtering by **Quarter** and **State**.

---

## 🗂️ Data Sources

### **1. Orders.csv**

Contains order-level information.

**Columns:**

* Order ID
* Order Date
* Customer Name
* State
* City

### **2. Details.csv**

Contains transaction/product-level details.

**Columns:**

* Order ID
* Amount
* Profit
* Quantity
* Category
* Sub-Category
* Payment Mode

Both datasets are joined using **Order ID** as the primary key.

---

## 📐 Data Model

**Relationship:**

```
Orders[Order ID] 1 ----- ∞ Details[Order ID]
```

This one-to-many relationship enables filtering across tables.

---

## ⭐ Key Insights

### **KPIs**

* **438K** — Total Sales Amount
* **37K** — Total Profit
* **5615** — Total Quantity Sold
* **121K** — Average Order Value (AOV)

### **Visual Highlights**

* **Profit by Month:** Shows seasonality and monthly profit fluctuations.
* **Sales by State:** Maharashtra and Madhya Pradesh contribute the most.
* **Category Quantity Split:** Clothing dominates with 63% share.
* **Payment Mode Split:** COD is the most used payment method.
* **Customer Contributions:** Top buyers like Harivansh and Madhav drive significant revenue.
* **Sub-Category Profit:** Printers are the highest profit-generating sub-category.

---

## 🔧 Power BI Transformations

### **Data Cleaning Steps:**

* Converted Order Date to Date format
* Handled negative profit values
* Trimmed and cleaned text fields
* Created calculated metrics such as AOV

### **Measures Used:**

```DAX
Total Amount = SUM(Details[Amount])
Total Profit = SUM(Details[Profit])
Total Quantity = SUM(Details[Quantity])
AOV = DIVIDE([Total Amount], DISTINCTCOUNT(Details[Order ID]))
```

---

## 🚀 How to Use

1. Open **Power BI Desktop**
2. Load **Orders.csv** and **Details.csv**
3. Create relationship on **Order ID**
4. Add the measures listed above
5. Recreate visuals using the dashboard previews
6. Add filters for **Quarter** and **State**

---

## 🎯 Insights & Business Recommendations

* **Focus more marketing in Maharashtra** — largest revenue contributor.
* **Boost inventory for Clothing and Electronics** — high demand categories.
* **Encourage digital payments** by offering cashback (COD usage is high).
* **Retarget top customers** using loyalty programs.
* **Optimize sub-category strategy** — low performers can be redesigned or promoted.

---
* A GitHub repository structure
* A PPT case study for placement portfolio
