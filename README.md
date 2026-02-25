# POWER-BI-SALES-PROJECT
----

## Table of Contents

* [Project Overview](#Project-overview)

* [Business Problem](#Business-Problem)

* [Technical Objectives](#Technical-Objectives)

* [Dataset Description](#Dataset-Description)

* [Process & Analysis](#Process--Analysis)

* [Dashboard Features](#Dashboard-Features)

* [Dashboard snapshot](#Dashboard-snapshot)

* [Key Insights](#Key-Insights)

* [Tools Used](#Tools-used)

* [Conclusion](#Conclusion)


## Project Overview

This project is an end-to-end Business Intelligence solution built using Microsoft Power BI  It demonstrates advanced data modeling, DAX measures, data transformation using Power Query, and performance-focused dashboard design.

The solution converts raw transactional sales data into a scalable analytical model that supports KPI monitoring, profitability analysis, trend evaluation, and regional performance comparison.

## Business Problem

### Organizations often struggle with:

* Disconnected sales data

* Lack of real-time performance tracking

* Poor visibility into profit drivers

* Limited regional performance insights

This dashboard addresses these challenges through structured modeling and advanced analytics.


## Technical Objectives

* Analyze overall sales performance

* Track revenue, profit, and quantity sold

* Identify top-performing products and categories

* Compare regional sales performance

* Monitor monthly and yearly trends

* Provide actionable business insights through visualization

* Develop dynamic, filter-responsive visualizations

## Dataset Description

### The project integrates three datasets:

1. Customers Dataset:

* Customer ID
* Demographics (Age, Gender, Region, Income)

2. Products Dataset:

* Product ID & Name

* Brand, Category, Weight, Colour

3. Sales Dataset:

* Sales, Customers, Product ID

* Sales Amount, Unit cost, Quantity

* Sales Date

## Process & Analysis

1. Data Import

Loaded all datasets into Power BI Power Query.

2. Data Cleaning & Transformation

* Removed duplicates and standardized formats.
* Creating calculated columns:


    a. Total Customers
 
    b. Total Sales (Revenue), Total Cost, Profit.
   
    c. Sales Date Hierarchy(Year, Quater, Month, Day).
    
3. Data Modeling

* Built relationships with Data Modelling

 Products (Product ID) ↔ Sales (CProduct ID)

 Sales (Customers ID) ↔ Customers (CustomerID)

 One-to-many relationships

 Primary keys to Foreign keys

 Proper cardinality configuration

4. DAX Measures

* Total Sales(Revenue) = SUMX(  Sales, Sales[Quantity] * Sales[SalesAmount]

* Total Cost = SUMX( Sales, Sales[Quantity] * Sales[Unit Cost]

* Profit = Total Sales (Revenue) -  Total Cost

* Total Customers = DISTINCTCOUNT(Sales[CustomerID])

## Dashboard Features

### The Excel dashboard is divided into two main views:

1. Overview

* KPI Cards (Total Sales (Revenue), Total cost, Profit, Total Customers).

* Year-over-year comparison

* Regional performance comparison

2. Product Analysis

* Top  Products (Dynamic ranking)

* Profit by Income level

* Total Sales (Revenue)  by color

* Brand by Profit


### Interactive Filters (Slicers)

* Gender filter

* Region filter

* Dynamic dashboard interaction

### Dashboard Snapshot
<img width="879" height="495" alt="Screenshot 2026-02-24 232608" src="https://github.com/user-attachments/assets/8685f661-e85d-4028-bb3c-073f33386a8a" />


## Key Insights 

* Business generated Total Revenue: ₦3.1M, Total Cost: ₦2.17M, Total Profit: ₦931,905 across 250 Customers

* Observed seasonal spikes in sales (2020, 2021, 2022)

* Apple made the highest (₦197k) profit in brand while Dell made the least (₦126k)

* Medium Income leve earners generated the most profit by ₦347k, then High income level earners by ₦302k and low income level earners by ₦283k.

* Discovered region-specific profitability gaps

 |Region | Total Customers | Total sales(Rev) | Profit | Total Cost |
 |-------|-----------------|------------------|----------|----------|
 |North  | 81 | ₦963,300 | ₦288,990| ₦674,310|
 |East  | 63 | ₦796,700 | ₦239,010| ₦557,690|
 |South | 55 | ₦703,000| ₦210,900| ₦492,100|
 |West  | 51 | ₦643,350| ₦193,005 | ₦450,345|


## Tools Used

* Microsoft Power BI 

* Power Query 

* DAX Measures

* Data Modeling Techniques


## Conclusion

### This project demonstrates how organizations can leverage structured data modeling, DAX-driven analytics, and interactive dashboards to monitor and optimize overall sales performance.

* By identifying high-performing products and regions, businesses can refine pricing strategies and inventory planning.

* By analyzing profit margins alongside revenue, decision-makers can prioritize profitability over volume.

* By tracking time-based trends, leadership can detect seasonality patterns and measure growth accurately.

Overall, this dashboard provides a scalable, performance-optimized BI solution that empowers stakeholders to make informed, data-driven decisions that support sustainable revenue growth and operational efficiency.



