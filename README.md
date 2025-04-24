# 📊 Retail Sales Analysis

**Database:** `p1_retail_db`  
**Table:** `retail_sales`  
**Skill Level:** Beginner to Intermediate  
**Focus:** SQL for Data Analysis

## 📌 Project Overview

This project demonstrates core SQL skills used by data analysts to explore, clean, and analyze retail sales data. It walks through setting up a relational database, cleaning data, performing exploratory data analysis (EDA), and answering key business questions.

---

## 🎯 Objectives

1. **Database Setup**  
   - Create and structure a retail sales database.
2. **Data Cleaning**  
   - Identify and remove incomplete or missing records.
3. **Exploratory Data Analysis (EDA)**  
   - Understand dataset patterns through summary queries.
4. **Business Insights**  
   - Answer real-world questions using SQL.

---

## 🏗️ Project Structure

### 1. Database Setup

**SQL:**
```sql
CREATE DATABASE p1_retail_db;

CREATE TABLE retail_sales (
    transactions_id INT PRIMARY KEY,
    sale_date DATE,
    sale_time TIME,
    customer_id INT,
    gender VARCHAR(10),
    age INT,
    category VARCHAR(35),
    quantity INT,
    price_per_unit FLOAT,
    cogs FLOAT,
    total_sale FLOAT
);
```

---

### 2. Data Exploration & Cleaning

**Queries:**
```sql
-- Total records
SELECT COUNT(*) FROM retail_sales;

-- Unique customers
SELECT COUNT(DISTINCT customer_id) FROM retail_sales;

-- Unique categories
SELECT DISTINCT category FROM retail_sales;

-- Null value check
SELECT * FROM retail_sales
WHERE 
  sale_date IS NULL OR sale_time IS NULL OR customer_id IS NULL OR 
  gender IS NULL OR age IS NULL OR category IS NULL OR 
  quantity IS NULL OR price_per_unit IS NULL OR cogs IS NULL;

-- Remove null records
DELETE FROM retail_sales
WHERE 
  sale_date IS NULL OR sale_time IS NULL OR customer_id IS NULL OR 
  gender IS NULL OR age IS NULL OR category IS NULL OR 
  quantity IS NULL OR price_per_unit IS NULL OR cogs IS NULL;
```

---

### 3. Data Analysis & Findings


#### 🔍 Key Findings

- **Customer Demographics:** Wide range of age groups, popular in categories like Clothing and Beauty.
- **High-Value Sales:** Multiple transactions over 1000 in total sale value.
- **Sales Trends:** Monthly fluctuations highlight peak shopping periods.
- **Customer Insights:** Identified high-spending customers and top-performing product categories.

---

## 📈 Reports Generated

1. **Sales Summary**  
   Total sales figures, customer profiles, and category-based performance.

2. **Trend Analysis**  
   Monthly and time-shift-based trends in order volume and sales value.

3. **Customer Insights**  
   Top-spending customers, unique buyers per category.

---

## ✅ Conclusion

This project is a hands-on SQL walkthrough for aspiring data analysts. It builds a solid foundation in SQL-based data handling, from setup and cleaning to EDA and insight generation. The insights gained can guide smarter business decisions related to sales, marketing, and inventory planning.

---

