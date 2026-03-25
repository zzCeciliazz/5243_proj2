# Data Explorer

## Overview

This project develops an interactive web application using **R Shiny** for end-to-end data analysis. The app allows users to upload datasets, clean and preprocess data, perform feature engineering, conduct exploratory data analysis (EDA), and export results. It is designed to be flexible, user-friendly, and highly interactive.

## Main Features

**Data Loading**  
Users can either select built-in datasets (`iris`, `mtcars`, `airquality`) or upload their own data in **CSV, Excel, JSON, or RDS** formats. The app provides a preview, structure, and summary statistics immediately after loading.

**Data Cleaning & Preprocessing**  
The app supports column name standardization, duplicate removal, missing value handling (mean/median/mode or row deletion), outlier treatment (IQR-based), scaling (z-score, min-max), and categorical encoding (label, one-hot). All steps are interactive and provide real-time feedback through summaries and logs.

**Feature Engineering**  
Engineering works on the table produced by cleaning and preprocessing. Users add new columns with row-wise **formulas** (with an optional dry-run preview), **single-column** numeric transforms (powers, logs, centering, z-score, min–max, rank, reciprocal, lag and lead by row order), **two-column** arithmetic (multiply, add, subtract, ratio with safe handling of zero divisors), **binning** (equal-width or quantile cuts), **rolling means** over a chosen window along row order, and simple **text** metrics (string length and word count). Column names are normalized automatically. Distribution plots and a profile table help compare new and existing columns; a step log and table preview record what was added. **Reset** reloads from the latest cleaned data and drops engineered columns. The same engineered table is what EDA and CSV export use next.

**Exploratory Data Analysis (EDA)**  
The EDA module provides interactive tools for exploring the processed dataset. Users can filter the data dynamically and visualize distributions, relationships, and correlations. All plots and tables update automatically based on user selections. The module includes distribution plots, relationship plots, missing-value visualization, and correlation analysis (heatmap and top correlations). A selected variable profile panel displays summary statistics for numeric variables and frequency tables for categorical variables. These interactive components help users quickly understand patterns, relationships, and data quality before exporting the final dataset.

**Export**  
The final processed dataset can be downloaded as a CSV file.


## Project Structure

- `R_Shiny_Team23.Rmd` — main Shiny application (UI + server + full workflow)

## Required Packages

Install the following packages in R:

```r
install.packages(c(
  "shiny","shinydashboard","shinyWidgets","DT","dplyr",
  "ggplot2","plotly","readxl","jsonlite","tidyr",
  "stringr","scales","reshape2"
))
```

## How ro run
- Download or clone this repository
- Open the folder in RStudio
- Run: click Run App in RStudio.

## How to Use

First, load a dataset (built-in or uploaded). Then clean and preprocess the data using the provided options. Next, create new features in the **Feature Engineering** tab. After that, explore the data using interactive visualizations and filters in the EDA tab. Finally, download the processed dataset if needed.

## Supported File Types

- CSV  
- Excel (.xlsx, .xls)  
- JSON  
- RDS  

## Deployment

The app can be deployed on shinyapps.io.  
https://1194414751lkx.shinyapps.io/r_shiny_project/
