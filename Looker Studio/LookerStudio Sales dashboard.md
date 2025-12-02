# **📊 Sales Dashboard (Looker Studio) – ClassicModels Dataset**

## **📘 Overview**

# **This project uses the ClassicModels sample database to build an interactive Sales Dashboard in Looker Studio.**  **The dashboard visualizes key sales metrics, product performance, customer activity, and revenue trends.**

# **I created this dashboard to demonstrate data modeling, SQL skills, and BI dashboard development using a real-world-style dataset.**

# ---

## **🚀 About the Dashboard**

### **📈 Sales Dashboard (Looker Studio)**

# **I designed and built a full Sales Dashboard in Looker Studio, featuring:**

* # **Total Sales & Revenue Analysis** 

* # **Sales Trends Over Time** 

* # **Top Products / Product Lines** 

* # **Top Customers by Revenue** 

* # **Order & Payment Insights** 

* # **Regional Sales (by Office / Customer Country)** 

# **The dashboard is interactive and allows filtering by:**

* # **Date** 

* # **Product Line** 

* # **Customer** 

* # **Order Status** 

# **If you want, I can add a preview image or help write a more detailed dashboard explanation.**

# ---

## **📦 Dataset: ClassicModels**

# **The ClassicModels database includes realistic business tables such as:**

* # **`customers`** 

* # **`employees`** 

* # **`offices`** 

* # **`orders`** 

* # **`orderdetails`** 

* # **`products`** 

* # **`productlines`** 

* # **`payments`** 

# **These tables represent a company selling classic cars globally and are commonly used for SQL and BI training.**

# ---

## **🗂️ Key Metrics Used**

* # **Revenue \= `quantityOrdered * priceEach`** 

* # **Profit \= `(priceEach - buyPrice) * quantityOrdered`** 


## **🎯 Purpose of the Project**

* # **To practice SQL data extraction** 

* # **To build a full BI workflow: data modeling → transformation → visualization** 

* # **To showcase dashboard design skills in Looker Studio** 

* # **To create a portfolio-ready analytics project using a real dataset**

# **📦 ClassicModels Database – README**

## **📘 Overview**

**ClassicModels** is a widely used sample database for practicing SQL queries, data modeling, and business intelligence.  
 It represents a fictional company selling classic cars, with data on customers, orders, payments, employees, and products.

This dataset is ideal for building analytics dashboards and learning relational database concepts.

---

## **🏗️ Database Structure**

### **Main Entities**

| Table | Description |
| ----- | ----- |
| **customers** | Customer contact information, credit limits, and assigned sales reps. |
| **employees** | Employee details with reporting hierarchy and office assignments. |
| **offices** | Regional office locations and contact info. |
| **orders** | Order metadata (dates, status). |
| **orderdetails** | Order line items including quantities and prices. |
| **products** | Product catalog with product lines, buy prices, and MSRP. |
| **productlines** | Categories of products. |
| **payments** | Customer payments and transaction dates. |

---

## **🔄 Entity Relationships**

* **customers → orders**: One customer can place multiple orders.

* **orders → orderdetails**: Orders are composed of many line items.

* **orderdetails → products**: Each order line refers to a specific product.

* **products → productlines**: Products belong to product categories.

* **employees → customers**: Sales representatives manage customers.

* **employees → offices**: Employees are assigned to an office.

---

## **📊 Dashboards & Visualizations**

### **✔️ Looker Studio Dashboard – *Sales***

I have created a full **Sales Dashboard** on **Looker Studio**, based on the ClassicModels database.  
 The dashboard includes visualizations such as:

* Total Sales & Revenue

* Sales by Product Line

* Top Customers

* Order Trends Over Time

* Payments & Collections

* Regional Sales Performance

If you want, I can help write a description or documentation section for each chart.

---

## **💰 Common Metrics**

| Metric | Formula |
| ----- | ----- |
| **Revenue** | `SUM(orderdetails.quantityOrdered * orderdetails.priceEach)` |
| **Profit** | `SUM((orderdetails.priceEach - products.buyPrice) * quantityOrdered)` |
| **Order Count** | `COUNT(DISTINCT orders.orderNumber)` |
| **Average Order Value** | `Revenue / Number of Orders` |

---

## **🧪 Example SQL Queries**

### **Total Revenue**

`SELECT`   
    `SUM(quantityOrdered * priceEach) AS Revenue`  
`FROM orderdetails;`

### **Profit by Product**

`SELECT`   
    `p.productName,`  
    `SUM((od.priceEach - p.buyPrice) * od.quantityOrdered) AS Profit`  
`FROM orderdetails od`  
`JOIN products p ON p.productCode = od.productCode`  
`GROUP BY p.productName;`

---

## **📥 Getting Started**

### **Load into MySQL**

`SOURCE classicmodels.sql;`  
