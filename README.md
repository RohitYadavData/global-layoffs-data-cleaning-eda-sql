# Global Layoffs: Data Cleaning and EDA using SQL

## Overview
Data cleaning and exploratory data analysis (EDA) of a global layoffs dataset using MySQL. The raw data was cleaned in a staging table, then analyzed by country, year, stage and company.

## Tools Used
- MySQL
- MySQL Workbench

## Data Cleaning Steps
1. Created staging tables to keep the raw data safe
2. Removed duplicates using ROW_NUMBER() and CTE
3. Standardized data (TRIM, fixing industry and country names, converting date text to DATE type using STR_TO_DATE)
4. Handled NULL and blank values (filled missing industry values using a self join)
5. Removed rows with no layoff data and dropped helper column

## EDA Performed
- Layoffs by country, year and stage
- Companies with the highest layoffs
- Monthly layoffs with rolling total (window function)
- Top 5 companies by layoffs for each year (DENSE_RANK)

## SQL Concepts Used
CTE, window functions (ROW_NUMBER, DENSE_RANK, SUM OVER), self join, GROUP BY, STR_TO_DATE, ALTER TABLE, UPDATE and DELETE

## Files
- `layoffs_cleaning_and_eda.sql`: all cleaning and analysis queries
