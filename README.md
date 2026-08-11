# 📊 Superstore Discount Effectiveness Analysis

## Project Overview

An interactive Power BI dashboard designed to evaluate how discounting affects sales and profitability in the Superstore dataset.

The project focuses on identifying whether discounts are supporting profitable growth or simply increasing sales while reducing profit margins.

---

## Business Problem & Objective

Discounting can increase sales volume, but excessive discounts may reduce profitability and create loss-making transactions.

The objective of this project is to evaluate the effectiveness of the current discount strategy and identify the products, locations, and discount levels associated with the greatest profitability risk.

---

## Key Business Questions

The analysis focuses on the following questions:

1. What is the relationship between discount levels and profitability?
2. At what discount level does profitability begin to decline significantly?
3. Which product categories and sub-categories are most negatively affected by discounting?
4. Which states combine relatively high discounts with low or negative profitability?
5. What changes to the discount strategy could have the greatest positive impact on profit?

---

## Tech Stack

The dashboard was built using:

- 📊 **Power BI Desktop** – Dashboard development, data modeling, and interactive data visualization
- 📂 **Power Query** – Data cleaning, transformation, merging, and preparation
- 🧠 **DAX** – Created custom measures including **Profit Margin** and **Show State by Status**, and built a dedicated Date dimension
- 🗂️ **Data Modeling** – Designed and implemented a custom **Star Schema** with fact and dimension tables
- 🗺️ **Power BI Map Visual** – Geographic analysis of discounting and profitability by U.S. state

---

## Data Source

**Source:** Sample Superstore Dataset

Data on nearly **10,000 U.S. retail orders**, including sales, profit, discounts, products, customers, locations, shipping, and returns, along with complementary tables containing return records and regional sales manager information.

The dataset was transformed and modeled into a Star Schema for analysis in Power BI.

---

## Data Preparation & Modeling

The original Superstore data required restructuring before analysis. Data cleaning and transformation were performed in **Power Query**, while the analytical model was built in **Power BI**.

Key preparation and modeling steps included:

- Removed duplicate records and corrected data types
- Normalized the original dataset into separate **Customer, Product, and Location** dimension tables
- Merged the **Returns** table with the Fact_Sales to simplify analysis
- Converted return values from **Yes/No** to **1/0**
- Merged the **People** table into the DIM_Location
- Renamed the relevant field to **Sales Manager** for better readability
- Replaced missing postal codes with `0000`
- Created a **Location Key** and added it to the order table as a foreign key
- Created a dedicated **Date dimension using DAX**
- Configured an **active relationship** with Order Date and an **inactive relationship** with Ship Date
- Organized the final model into a **Star Schema** with a central fact table and supporting dimension tables

---

## Walkthrough of Key Visuals

- **Key KPIs**  
  Displays **Total Sales, Total Profit, Profit Margin, and Average Discount** for a quick overview of business performance.

- **Discount vs. Profitability by Sub-Category (Scatter Plot)**  
  Compares average discount with profit margin across sub-categories to identify products with weak profitability.

- **Profitability by Sub-Category (Bar Chart)**  
  Highlights low-performing and loss-making sub-categories.

- **Profit Margin by Discount Band (Column Chart)**  
  Shows how profitability changes across different discount ranges.

- **Sub-Category Performance Table**  
  Compares sales and profit margin across product sub-categories.

- **Discount & Profitability by State (Map)**  
  Uses bubble size for average discount and color for profit margin to identify high-discount, low-profit states.

- **Top Loss-Making States (Table)**  
  Highlights states with negative margins alongside sales and discount levels.

- **Profitability Status Filter**  
  Allows users to switch between **All States, Loss-Making States, and Profitable States**.

- **Profit Margin by Discount Band and Category (Grouped Column Chart)**  
  Compares discount sensitivity across **Furniture, Office Supplies, and Technology**.

---

## Key Insights

- Higher discounts are generally associated with lower profit margins
- Profitability risk increases noticeably above **20% discount**
- **Furniture** contains several of the weakest-performing sub-categories
- **Texas, Illinois, and Pennsylvania** combine strong sales with negative margins

---

## Recommendations

- Review discounts above **20%**
- Apply category-specific discount limits
- Focus on high-sales, loss-making states
- Reassess discounting for low-margin sub-categories such as **Tables, Bookcases, and Supplies**

---

## Dashboard Preview

### Discount Effectiveness Overview

![Discount Effectiveness Overview]([images/Overview.png](https://github.com/MaryamKazzemi/superstore-discount-profitability-analysis/blob/main/Overview.png))

### Product Analysis

![Product Analysis](images/Product_Analysis.png)

### Geographic Analysis

![Geographic Analysis](images/Geographic_Analysis.png)

### Discount Threshold Analysis

![Discount Threshold Analysis](images/Discount_Threshold.png)

---
