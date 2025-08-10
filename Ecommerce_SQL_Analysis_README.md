# Task - E-Commerce Data Analysis using SQL

## 📌 Objective
To analyze raw e-commerce dataset using SQL queries and derive structured outputs for business insights.

## 📊 Dataset
- **Tables:** Customers, Categories, Employees, OrderDetails, Orders, Products, Shippers, Suppliers
- **Fields:** Include attributes such as CustomerID, OrderID, ProductName, Quantity, Price, CategoryName, SupplierName, ShipperName, etc.

## 📈 Steps Followed
1. **Understand the Database Schema** – Identify all tables and their relationships.
2. **Inspect Raw Data** – Preview each table using simple `SELECT` queries.
3. **Clean & Standardize Data** – Handle missing values, duplicates, inconsistent formats.
4. **Identify Keys for Joins** – Map primary and foreign keys between tables.
5. **Query Individual Tables** – Extract base data from each table.
6. **Join Tables** – Combine relevant information across tables for richer insights.
7. **Filter, Sort, Aggregate** – Apply conditions, sorting, and group calculations.
8. **Create Final Output Tables** – Match outputs with required business questions.
9. **Document Queries** – Save `.sql` scripts for reproducibility.
10. **Export Results** – Save final query results as CSV or for visualization tools.

## 📌 Example Queries
- Get all customers:
```sql
SELECT * FROM Customers;
```
- Get order details with product names:
```sql
SELECT od.OrderID, p.ProductName, od.Quantity, od.UnitPrice
FROM OrderDetails od
JOIN Products p ON od.ProductID = p.ProductID;
```
- Get orders shipped by "Speedy Express":
```sql
SELECT o.OrderID, c.CustomerName, s.ShipperName
FROM Orders o
JOIN Customers c ON o.CustomerID = c.CustomerID
JOIN Shippers s ON o.ShipperID = s.ShipperID
WHERE s.ShipperName = 'Speedy Express';
```

## 📤 Files to Upload
- SQL scripts (`.sql`)
- Screenshot outputs of each query
- README.md (this file)

## 🛠 Tools Used
- SQL (MySQL / PostgreSQL / SQLite)
- DBMS tool (MySQL Workbench, pgAdmin, etc.)
- CSV Export or Visualization Tool (Excel, Tableau, Power BI)

---
