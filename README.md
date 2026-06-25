# NYC-Yellow-Taxi-2023-
Big Data Analytics and Fare Prediction Project


# Project Overview

This project aims to build an end-to-end Big Data analytics pipeline using Databricks, PySpark, Spark SQL, Delta Lake, and Machine Learning.

The dataset will contain NYC Yellow Taxi trip records for the full year 2023, with more than 38 million raw records stored in Parquet format.

The project will process the raw taxi data through several stages, including data ingestion, data understanding, data cleaning, feature engineering, SQL analysis, Gold Layer table creation, visualization, and machine learning.

The analysis will focus on taxi demand patterns, passenger charge behavior, trip distance and duration, airport trips, tipping behavior, trip speed, pickup and dropoff activity, and financial data quality.

A machine learning model will also be developed to predict the base taxi fare amount using cleaned and engineered trip features.

---

## Business Problem and Project Objective

## Business Problem

Taxi companies, transportation agencies, and city planners need to understand how taxi services operate across different times, locations, and trip types.

However, raw taxi trip data is very large and may contain data quality issues 

Stakeholders need answers to questions such as:

- When is taxi demand highest?
- Which months, days, and hours have the most trips?
- Which pickup and dropoff locations are most active?
- How do trip distance and duration affect passenger charges?
- How do airport trips differ from normal city trips?
- How do passengers tip on credit card trips?
- Can trip features be used to predict the base taxi fare amount?

---

## Project Objective

The objective of this project is to design and implement a scalable Big Data pipeline that ingests, cleans, transforms, analyzes, visualizes, and models NYC Yellow Taxi 2023 trip data.


# Project Architecture

## Medallion Architecture

This project follows the Medallion Architecture:

### Bronze Layer

The Bronze layer stores the raw taxi trip data exactly as received.

- Raw Parquet files
- No cleaning
- No transformation
- Used as the original source of truth

### Silver Layer

The Silver layer stores cleaned and validated trip data.

- Invalid records removed
- Missing values handled
- Data types fixed
- Outliers filtered using business rules

### Gold Layer

The Gold layer stores business-ready analytical tables.

Examples:

- Hourly demand
- Monthly trends
- Zone-based revenue
- Tip behavior
- Efficiency metrics
