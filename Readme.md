# Data Explorer Pro

## Overview

This project develops an interactive web application using **R Shiny** for end-to-end data analysis. The app allows users to upload datasets, clean and preprocess data, perform feature engineering, conduct exploratory data analysis (EDA), and export results. It is designed to be flexible, user-friendly, and highly interactive, meeting the requirements of Project 2 :contentReference[oaicite:0]{index=0}.


## Main Features

**Data Loading**  
Users can either select built-in datasets (`iris`, `mtcars`, `airquality`) or upload their own data in **CSV, Excel, JSON, or RDS** formats. The app provides a preview, structure, and summary statistics immediately after loading.

**Data Cleaning & Preprocessing**  
The app supports column name standardization, duplicate removal, missing value handling (mean/median/mode or row deletion), outlier treatment (IQR-based), scaling (z-score, min-max), and categorical encoding (label, one-hot). All steps are interactive and provide real-time feedback through summaries and logs.

**Feature Engineering**  
Users can create new features using formulas, apply transformations (log, sqrt, scaling, lag/lead), generate pairwise features, perform binning, compute rolling means, and extract simple text features. A preview function allows users to test formulas before applying them.

**Exploratory Data Analysis (EDA)**  
The app provides interactive summary statistics, variable profiling, distribution plots, relationship plots, missing-value visualization, and correlation analysis. Users can dynamically filter the dataset, and all outputs update automatically.

**Export**  
The final processed dataset can be downloaded as a CSV file.


## Project Structure

- `app.R` — main Shiny application (UI + server + full workflow)

## Required Packages

Install the following packages in R:

```r
install.packages(c(
  "shiny","shinydashboard","shinyWidgets","DT","dplyr",
  "ggplot2","plotly","readxl","jsonlite","tidyr",
  "stringr","scales","reshape2"
))

## How ro run
- Download or clone this repository
- Open the folder in RStudio
- Run: click Run App in RStudio.

## How to Use
First, load a dataset (built-in or uploaded). Then clean and preprocess the data using the provided options. Next, create new features in the Feature Engineering tab. After that, explore the data using interactive visualizations and filters in the EDA tab. Finally, download the processed dataset if needed.

## Supported File Types
- CSV
- Excel (.xlsx, .xls)
- JSON
- RDS

## Deployment
The app can be deployed on shinyapps.io.
http://127.0.0.1:5679

