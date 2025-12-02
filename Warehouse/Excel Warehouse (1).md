# **📦 Warehouse Management – Excel Project**

## **📘 Overview**

This project is an Excel-based **Warehouse Management System** that I created to track inventory levels, product movement, and stock performance.  
 The file provides a structured and easy-to-use solution for monitoring warehouse operations without requiring a database or external tools.

---

## **🗂️ Key Features**

* **Inventory Tracking**  
   Monitor available stock for each product in real time.

* **In/Out Stock Register**  
   Record incoming and outgoing quantities with dates and transaction types.

* **Automatic Calculations**  
   Excel formulas calculate total stock, remaining inventory, shortages, and overages.

* **Product Catalog**  
   A structured table for item codes, product names, categories, and descriptions.

* **Dashboard (Optional)**  
   If included, it may contain charts such as:

  * Stock levels

  * Incoming vs outgoing trends

  * Top product movement

  * Low-stock alerts

---

## **🏗️ File Structure**

Typical worksheet layout:

* **Products** – Master list of items

* **Stock In** – Records of incoming inventory

* **Stock Out** – Records of outgoing items

* **Inventory Summary** – Calculated stock levels

---

## **🔧 Formulas Used (Examples)**

* **Current Stock:**  
   `=SUMIF(StockIn!A:A, A2, StockIn!C:C) - SUMIF(StockOut!A:A, A2, StockOut!C:C)`

* **Low Stock Indicator:**  
   `=IF(CurrentStock < ReorderLevel, "Low", "OK")`

If you want, I can rewrite the formulas based on how your file actually works—just share screenshots or columns.

---

## **🎯 Purpose of the Project**

* Track warehouse inventory efficiently

* Reduce manual errors

* Improve reporting and management decisions

* Create a practical Excel-based solution for real warehouse workflows

* Demonstrate Excel skills: formulas, pivot tables, data validation, dashboard design

---

## **📄 Requirements**

* Excel 2016 or newer

* No external dependencies

