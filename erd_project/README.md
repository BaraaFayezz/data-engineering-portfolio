# 🗄️ Entity Relationship Diagram (ERD) – Retail Database

## 📘 Overview
This project represents a **Retail Database** design created using an **Entity Relationship Diagram (ERD)**.  
The ERD models the relationships between key business entities such as **Orders**, **Customers**, **Products**, **Employees**, **Suppliers**, and **Shippers**.  
It serves as the foundation for data analysis, reporting, and building an end-to-end data pipeline.

---

## 📊 Entities & Relationships

The database includes the following main entities:

1. **Customers**  
   - Stores customer information such as name, address, and contact details.  
   - Linked to the **Orders** table through `customer_id`.

2. **Employees**  
   - Contains information about company employees who handle customer orders.  
   - Linked to **Orders** through `employee_id`.

3. **Shippers**  
   - Represents shipping companies responsible for delivering orders.  
   - Linked to **Orders** via `shipper_id`.

4. **Orders**  
   - Central table connecting customers, employees, and shippers.  
   - Linked to **Order_Details** for item-level transactions.

5. **Order_Details**  
   - Line-item level table that records the products within each order.  
   - Linked to **Orders** and **Products** using `order_id` and `product_id`.

6. **Products**  
   - Holds details about each product, including name, category, supplier, and price.  
   - Linked to **Suppliers** and **Categories**.

7. **Suppliers**  
   - Stores supplier details providing products to the store.  
   - Linked to **Products** through `supplier_id`.

8. **Categories**  
   - Groups products into different types (e.g., electronics, food, clothing).  
   - Linked to **Products** via `category_id`.

---

## 🔗 Relationships Summary

| Relationship | Type | Description |
|---------------|------|-------------|
| Customers → Orders | One-to-Many | Each customer can place multiple orders. |
| Employees → Orders | One-to-Many | Each employee can manage multiple orders. |
| Shippers → Orders | One-to-Many | Each shipper can deliver multiple orders. |
| Orders → Order_Details | One-to-Many | Each order can include multiple products. |
| Products → Order_Details | One-to-Many | Each product can appear in multiple order details. |
| Suppliers → Products | One-to-Many | Each supplier can supply multiple products. |
| Categories → Products | One-to-Many | Each category can include multiple products. |

---

## 🧠 Use Case
This ERD is part of a **data engineering learning project** and is used to:
- Build and normalize relational databases.
- Understand data modeling best practices.
- Serve as a source schema for ETL and analytical data pipelines.

---

## 📎 Files Included
- `Data Model Assignment.PNG` → The ERD image file (uploaded)
- `README.md` → This documentation file

